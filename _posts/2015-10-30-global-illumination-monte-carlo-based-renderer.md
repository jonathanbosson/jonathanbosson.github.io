---
layout: post
title: "Global Illumination, Monte Carlo Raytracing Renderer"
date: 2015-10-30
---

Well well, where do I start. This was one of the most fun projects I have done to date. In the course Adv. Global Illumination and Rendering, <em>TNCG15</em> we got the task to build a physically based renderer through Monte Carlo Raytracing from the ground up. We developed our own scene graph and used the library GLM for linear algebra algorithms. 

We never managed to implement an Oren-Nayar reflectance model or support for transparent objects. That as well as parallelizing the computations and implementing photon mapping to make the renderer real-time are improvements I hope to do in the future.

<img src="/images/img40rpp10sr.png">

The report can be read [here](/reports/agirRapport.pdf) and the source is available on [github](https://github.com/jonathanbosson/OJGIR).
