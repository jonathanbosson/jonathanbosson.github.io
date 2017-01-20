---
layout: post
title: "Maya Soft Body Deformer Plugin using Shape Matching"
date: 2016-12-21
---

This project was done in an SFX course (TNCG13) where the aim was to develop your own Autodesk Maya plugin.
We chose to develop an efficient soft body deformer through a shape matching technique proposed by Müller et al. The shape matching method does not require storage of any data about neighbouring vertices and is unconditionally stable. Due to its efficiency in terms of memory and computation complexity it is well suited for interactive applications.

<iframe width="560" height="315" src="https://www.youtube.com/embed/X59WEH4l5QE" frameborder="0" allowfullscreen></iframe>

Our aim was to make something similar to the mainobject in the movie *Flubber* from 1997. To render the final version we used IBL with a HDR image of a public hall in our university to make the flubber-object photo realistic.

Read the [report](/reports/flubber.pdf) or check the source on [github](https://github.com/isabelljansson/flubber). If you're interested in rendering techniques, have a read of a report I wrote in the same course: <a href="/reports/polynomial_jonbo665.pdf">Image Space Adaptive Polynomial Rendering</a>.