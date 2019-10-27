+++
showonlyimage = false
draft = false
image = "img/portfolio/vr_lab/thumbnail.jpg"
date = "2019-10-27"
title = "VR Lab Project: Riftblade"
weight = 3
+++

Another university project that was part of my Bachelors degree...

<!--more-->
...this one actually turned out to have some gameplay in the end.
I haven't yet managed to find my screenshot folder of it, but fortunately we submitted small trailer videos for this project and ours got uploaded to the institute's YouTube channel:

{{< youtube M2W5AhV-NEE >}} \

On this project, I wrote my first renderer that actually supported a bunch of features:

* Deferred shading.
* Normal and (somewhat whonky) parallax occlusion mapping.
* Screenspace volumetric lighting.
* HDR + Tonemapping.

I was also responsible for adding VR support to the game, which at the time meant working with the very first Occulus Rift devkit. Due to its incomplete motion tracking, that mostly meant spending a lot of time getting motion sick - an experience that pretty much turned me off VR as a developer and a consumer for quite a while. 
As a team, we also implemented various other features, such as skeletal animations (for which I wrote the GPU code that performed the actual vertex skinning, not the CPU side playback code though), pointlight shadows, a simple component based gameplay framework, movement controllers for AI and player characters using [Bullet](https://github.com/bulletphysics/bullet3) for collision, navmesh-based navigation for AI characters and an improvised motion input system based on two Wii controllers being taped to the player's arm.



