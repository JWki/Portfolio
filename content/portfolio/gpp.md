+++
date = "2016-11-05T19:41:01+05:30"
title = "Game Programming Lab Project: GPP"
draft = false
image = "img/portfolio/GPP/thumbnail.png"
showonlyimage = false
weight = 1
+++

This project was part of my Bachelors degree in Computer Science. Originally intended as a small game project...  
<!--more-->

...my team very quickly settled on a small, self contained tech demo, considering how that would allow to completely focus on the important bits: The tech. As a team of five, we set ourselves an ambitious goal - a showroom like demo featuring a custom physics engine with support for dynamic deformation, nicely brought to screen by a physically based renderer through an extensive post processing stack. 
Unfortunately, health issues of one member of the team lead to the physics engine having to be cut, however we still managed to get quite an extensive array of features done.

### Features

Here's a few of the graphics features I personally worked on:

* Physically based material rendering, following the UE4 shading model as described in [the 2013 Siggraph course](https://blog.selfshadow.com/publications/s2013-shading-course/karis/s2013_pbs_epic_notes_v2.pdf).
* Global illumination approximation using Image Based Lighting.
* Post processing stack including image based lens flares, HDR bloom + tone mapping and colorization and vignette stylization effects.
* Realtime analytic light sources - point lights, spot lights and directional lights - and fully linear lighting.
* Fully deferred renderer (using clustered light culling as mentioned below).

Besides these, I was also responsible for a lot of the core architecture of both the renderer as well as the entire application and systems tangential to rendering, including the following aspects:

* Node based scene hierarchy system supporting dynamic composition of scene objects through node attachments.
* Optimized GPU memory management for geometry buffers in OpenGL using growable pools of buffer objects.
* Runtime resource management framework supporting easy extension with more resource types as well as request caching at runtime.
* In-engine tooling framework using the fantastic [dear imgui](https://github.com/ocornut/imgui) library.
* In-engine tools for material creation, scene manipulation and object editing.
* In-engine debugging tools with visualization of render pipeline stages, quality settings and lots of exposed variables to tweak.

Other than my personal contributions, our final hand-in of course also featured the contributions of my wonderful team members, which included skeletal animations, GPU particle systems, cascaded shadow maps, compute-based clustered light culling and procedural generation of vegetation and planet geometry.

Unfortunately as this project was part of a uni course, the source code is not publicly available.

### Screenshots

![Character Rendering =250x100][1]
*Basic PBR rendering working suprisingly well on a character even without proper skin shading.* \
![PBR Materials + IBL][2]
*More advanced material showcasing parallax occlusion mapping.* \
![Filmic PostFX][3] 
*Some filmic post processing featuring tonemapping, vignette and image based lens flares with lens dirt filter.* \
![Material Editor][4]
*A glimpse of the material editor allowing new materials to be created on the fly at runtime.* \
![Spotlight][5]
*A simple yet gorgeous spotlight.* 

[1]: /img/portfolio/GPP/characterRendering.png 
[2]: /img/portfolio/GPP/noice.PNG 
[3]: /img/portfolio/GPP/filmic.PNG 
[4]: /img/portfolio/GPP/material_editor.png 
[5]: /img/portfolio/GPP/spotlights.PNG 