---
layout: post
title: "3D Rigid Body Physics Simulation"
date: 2015-03-13
---

This is a simple physics engine that handles rigid body collisions. Translation as well as rotational movement have been implemented for sphere- or cube-shaped objects colliding with each other or nearby walls. It's working! Well, ish. All but the rotation for the squares are a bit iffy since the collision detection is somewhat prolematic. We use the separating axis theorem (SAT) as well as comparing vertex coordinates in a local basis. Sadly, deadline came too quickly and improving this project has been far down in my backlog of personal projects. We have some real funky rotating cubes though. I'll see what I can do to add a video of the project at a later stage.

<img width="800" height="480" src="/images/balls_2.jpg">

Read the [report](/reports/TNM085_group5.pdf) or check the source on [github](https://github.com/Liljan/AKRS3D).

