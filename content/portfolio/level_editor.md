+++
showonlyimage = true
draft = false
image = "img/portfolio/level_editor/thumbnail.png"
date = "2019-10-24"
title = "Brush Level Editor"
weight = 2
+++

An important part of any engine are the world building tools...
<!--more-->
![A][1] \

...and I've always been a fan of tools that let you quickly iterate on level geometry. The first engine I've used had a brush based CSG editor very much like Valve's Hammer editor or Quake's Radiant. These tools are super useful to create rough level geometry either for whiteboxing, or even for final level layouts that are then augmented with detail meshes and decals.
While I didn't get to implementing CSG operations for this project, I am pretty happy with the workflow that I did get done. 

{{< youtube yL3OKGELraU >}} \

Using a halfedge based mesh representation, I realized quite a few editing features, including the following:

* Different editing modes: Face mode, vertex mode and brush mode, working on different granularities.
* Translation, scale and rotation tools for all modes.
* Face extrusion tool.

I did actually implement a "gameplay mode" into the editor as well, featuring a first person character using PhysX as well as some particle FX in order to have some way of interacting with the level.

With this small set of features, it's already quite intuitive to quickly build coarse level geometry. The editor is well suited for laying out interior spaces such as commonly found in mid-2000s FPS games, which were a big part of the original inspiration for this (and a big inspiration for me to get into games overall).

Writing this was also a good practice for my UX design skills, and I hope to eventually revisit it and merge it into [the FPS project](../fps) I started a while ago.



[1]: /img/portfolio/level_editor/thumbnail.png