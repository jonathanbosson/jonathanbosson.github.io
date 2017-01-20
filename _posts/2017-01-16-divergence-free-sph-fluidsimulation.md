---
layout: post
title: "Divergence-Free SPH for Fluid Simulations in Computer Graphics"
date: 2017-01-16
---

This has been one of my largest projects yet, spanning over an entire semester. It was the main focus in a PhD course (TN1008) of Advanced simulation and visualization of fluids in computer graphics. The task was to recreate the result from Jan Bender et al. [publication](https://animation.rwth-aachen.de/media/papers/2015-SCA-DFSPH.pdf). See what it looks like!

<iframe width="560" height="315" src="https://www.youtube.com/embed/oTdw5cLSVr8" frameborder="0" allowfullscreen></iframe>

The biggest issues we had was to get our pressure solver to work correctly and efficiently. Since the pressure force is dependant on a particle's neighbours velocities and densities is a method of efficient sorting required. The difference with this method compared to other SPH fluid simulation methods is that two distinct solvers are to minimise the divergence and density error whereas most other methods uses only one. This allows for fast convergence which leads to fewer iterations. 


The report discussing the method in depth can be found [here](/reports/tn1008-dfsph-fluidsimulation.pdf) and the code is available on [github](https://github.com/ronjagrosz/DFSPH). There's a released version with a guide on how to compile it, so go on and try it!