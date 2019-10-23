+++
showonlyimage = false
draft = false
image = "img/portfolio/locust/screenshot004.jpg"
date = "2016-11-05T18:25:22+05:30"
title = "Yet another renderer: Locust"
weight = -1
+++

Another one of those projects that every engine/graphics programming enthusiast has probably filled entire hard drives with...
<!--more-->

This particular renderer / mini-engine originated from a relatively successful attempt to build a graphics API abstraction. Inspired by the quite well made [sokol-gfx](https://github.com/floooh/sokol), I specifically focused on making the sort of graphics API I would like to use, emphasizing convenience and ease of use. The result was a quite capable wrapper over DX11-style graphics APIs. As a matter of fact, it ended up being more of a DX11 wrapper since that was the only backend I wrote for it, however it would have been feasible to write an OpenGL 4.5 backend for it as well.
Using this little API I made for myself, I went to, once again, implement a staple of graphics features, as well as a few systems only tangentially related to graphics:

* Physically based material rendering.
* Image based lighting approximating irradiance and radiance integration via pre-convoluted cube maps.
* Linear lighting pipeline with HDR bloom and final tonemapping stage.
* Flat entities-as-ids object model with dynamic composition, supporting (de-)serialization of scenes to and from disk.
* In-engine scene editing tools featuring an object property editor, 3D-gizmos for scene manipulation, an asset importer dialog with batch import support for meshes and textures.
* Live C++ hot-reload of editor code via .dll hotswapping.
* Custom renderer for [dear imgui](https://github.com/ocornut/imgui) using my custom graphics API abstraction and with added support for "refractive transparency" 

Eventually, as happens with most of these projects, this one lost direction at some point - I began adding a fully custom type system with runtime support that could have ended up becoming the object model for an embedded scripting / game language, and built a few things on top of it like a fancy node editor, however eventually life and other projects overtook this one. I would like to revisit a few elements of it at some point since I feel like this is actually one of the more coherent collection of features in a single codebase that I've produced so far.

### Screenshots

![A][1] \
![B][2] \
![C][3]



[1]: /img/portfolio/locust/screenshot004.jpg
[2]: /img/portfolio/locust/screenshot005.jpg
[3]: /img/portfolio/locust/screenshot002.jpg

