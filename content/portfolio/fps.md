+++
showonlyimage = false
draft = false
image = "img/portfolio/fps/thumbnail.png"
date = "2019-10-24"
title = "First Person Shooter Techdemo"
weight = 1
+++

Another attempt at making something with actual gameplay...
<!--more-->
![title][8]

I think the very first game I ever wanted to make was a Doom 3 clone. Not that I would have been able to play Doom 3 at that time, since I was about 13 years old and I think it hadn't come out yet either, but I had read a preview in a popular German PC gaming magazine and somehow that preview launched me into the world of game development.
Ever since then, first person shooters are what I considered to be one of the royal genres of video gaming that always stood at the frontier of technological development.

![cook torrance][2]
*Cook-Torrance makes everything prettier!* \

Naturally, most of my many attempts at making my own game ended up being first person shooters. Now, after a few years of actually knowing how games work under the hood and especially how my former dream game, Doom 3, works internally - after all, the source code is available to everyone now - I thought I'd relaunch my attempts at making a first person shooter. I haven't actually gotten to a point yet where anything is playable of course, since I needed to put this on halt again, but I very much want to pick this project up again at some point in the future.

![textures][3] 
*Every FPS game needs a plcaeholder texture.* \

While I was actively working on it, I focused on not spending a lot of time on generic engine code but instead directly go for more exciting features such as the following:

* First person movement and collision detection using PhysX.
* Hierarchical view system to allow for view-models like guns to be rendered at a different field of view and detail levels.
* DX11 powered forward renderer with support for physically based material rendering (duh), set up for (yet to be implemented) clustered light culling.
* Mesh based decal system (which turned out to probably be too slow) which supports application of decals on any surface including skinned meshes.
* Flat inheritance based object model with a simple property reflection system supporting generic scene (de-)serialization.
* Basic level editing tool making use of the aforementioned object model.

As should be apparent from this list, my main focus when starting this project was to really fast get to a point where I could make levels and have a player run around in them as well as enabling them to interact with the environment in some way (in this case through splatting decals all over the place). 

![decal debug][5]
![decal debug 2][6]
*Proper debugging visualization support is essential to developing visual features such as decals.* 


If I get a chance to pick this project up again, I will probably overwork the object model to be more data driven rather than code driven, replace the mesh based decals (which were a *lot* of work but only delivered very subpar performance on spawning due to the complexity of the mesh generation algorithm) with two distinct solutions - namely some sort of "deferred" decals for static geometry and a more advanced, texture space painting solution for characters - and re-implement the renderer on top of DX12 instead of DX11 in order to get access to bindless texturing (and generally because I prefer the API by now). 
I would also probably try to recover and integrate [my old brush-based level editor](../level_editor), since it's a perfect fit for the kind of game I have in mind.

![ui][1]
*Bare-bones level editor UI* \

As its current state is relatively broken and half-baked, I have not made this project available on github.

[1]: /img/portfolio/fps/editor.png 
[2]: /img/portfolio/fps/lights.png 
[3]: /img/portfolio/fps/textures.png 
[4]: /img/portfolio/fps/colorLights.png 
[5]: /img/portfolio/fps/decalsWIP.png 
[6]: /img/portfolio/fps/decalsWIP2.png 
[7]: /img/portfolio/fps/decals.png 
[8]: /img/portfolio/fps/thumbnail.png