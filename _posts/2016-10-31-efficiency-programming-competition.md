---
layout: post
title: "Efficiency Programming competition - Consid Solutions"
date: 2016-10-31
---

This autumn I signed up for a programming competition in efficiency hosted by [Consid](http://www.consid.se/).
In Sweden a car's license plate has three letters followed by three numbers, such as `ABC123`. The task was to as quickly as possible answer whether or not a duplicate license plate existed in a given textfile of 6 million entries. I didn't win managed to get pretty close with completion time within 50ms. My solution can be found [here](https://github.com/jonathanbosson/Consid-Find-Regnr), but I wanted to explain my thoughtprocess a bit here.

1. In order to scale the project with multiple cores I wanted to include parallel processing. However, reading and writing to/from a file is done sequentially. So the first thing that is done is to open the given textfile and save it to a dynamically allocated buffer. By doing this can I quickly access different parts (or license plates) from the textfiles in parallel without compromising thread safety. 

2. Since the data can be handled in parallel I needed an efficient way to store information of the status of a license plate number. To do this I created a boolean matrix with `18279` rows and `1000` columns. I then translated the license plate string into a character part, `c`, and number part, `n`. The number part corresponded for what column in the matrix the license plate belonged to and the character part to the row. However, since the character part contained letters I needed to convert this to a unique ID. This was done by converting `c` to base-26 index, letting `A = 1, B = 2, ..., BA = 2 * 26 + 1`.

3. Now can the license plate number be converted to a unique cell in the boolean matrix with id `[c][n]`. That location is then set to store `true`. `c` and `n` are private variables for each working thread and there's no discontinuity in the shared matrix variable. Once all of the data has been read through can a parallel loop with a reduction clause be used to find the number of stored `true`-variables in the matrix. If this value differs from the number of read license plates, then a duplicate exists. (`lSize` is the number of characters in the data, `lSize/8` is used to count number of license plates in the file).