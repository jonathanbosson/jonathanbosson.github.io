---
layout: post
title: "Interactive Equation Solver through Neural Network and OCR"
date: 2016-11-03
---

This project done within an AI for Interactive Media course, <em>TNM095</em>. 
Our idea was to use a webcam and computer vision to detect where letters were written in real-time on a piece of white paper. A multilayered perceptron neural network would then classify an image chunk as a character using optical character recognition (OCR), which could then be used in an equation solver. With this solution can a user write close to any expression or equation containing known operators and the application will give an answer.

<img width="300" height="180" src="/images/ocr.PNG">

In short, the process is divided into three parts:

1. **Preprocessing** - Each image in a read dataset contains a character which is converted into
a string of bits by thresholding the image. The image is then cropped and rescaled
before storing the result into a text file and which is used in the following step

2. **Training** - The processed dataset is used as the input for the training of the MLP-neural
network. The result is exported and used in the application.

3. **Application** - The application uses a web camera to register characters. The neural
network guesses the classification of the characters in each frame. If the registered
characters define a valid mathematical expression, the application calculates the
result of the expression and dispose it to the user 

Read the [report](/reports/mlpocr_jonbo665_isaja187.pdf) for a more detailed explanation on our method.


Source code is available on [github](https://github.com/isabelljansson/TNM095).
