+++
showonlyimage = false
draft = false
image = "img/portfolio/gpu_skinning/thumbnail.png"
date = "2019-10-24"
title = "Skeletal Animation Playground"
weight = 1
+++

Writing fancy rendering pipelines is fun, but looking at completely static scenes becomes a bit dull after a while...
<!--more-->

...what truly breathes life into video games are animations!
Having worked on [one project](../vr_lab) that featured skeletal animation before, I had only implemented the GPU side of mesh skinning back then, with another team member implementing the actual animation playback. To close this hole in my practical experience, I set up a small self contained project covering the entire pipeline, from FBX file to in-game animation.

{{< youtube HWBRe1VqDPw >}} 

*Non-blended transition between various animation clips with root motion applied* \

As it turns out, the hardest part about skeletal animation is to get the data into your application. Fortunately I already had a simple runtime format for animation clips and skeletons set up. Getting Blender to export to that format was not exactly trivial, mostly due to my inexperience with its Python API, but worked fine until eventually, I ran into issues with files that Blender didn't even import correctly in the first place - so I rewrote the entire suite of exporters (one for mesh data, one for skeleton data and one for animation clips) in C# as Unity editor scripts, since Unity seems to very consistently import FBX *correctly*, and it has a relatively straightforward API to access geometry and animation data via scripts.
Unity was also heavily used during this project to obtain a reference of how things should look like, since with skeletal animations you can make quite a broad variety of mistakes along the pipeline, so being able to verify that your source data is fine is very helpful.
After some initial pains figuring out the best ways to apply all the necessary math required to distort meshes in a meaningful way, I ended up with a little playground for animations that supported the basic set of features you'd expect from an animation system:

* Animation clip playback (duh).
* Linear fades between different animation clips.
* Linear blending between different animation clips playing at the same time (useful for synchronized blends between a run and a walk depending on character speed, for example).
* Basic root motion support (that didn't properly work with looping animations). \
\

{{< youtube uP6nN49SquM >}}

*Linear faded transitions, very nicely visible here with no root motion applied.* \

Like so many others, this project, which was only intended as a small weekend project anyways, shifted away from my attention after a few weeks due to more pressing matters, however I would like to revisit this at some point. There is still a great heap of features that you'd expect from a more mature animation system, such as masked playback (where only selected parts of the skeleton play a specific animation), integration with a physics engine for active ragdolls, an explicit blend tree setup and much more.

{{< youtube UHgLqAKhuRw >}}

*Thrilling, isn't it?* \

I'd also like to write a few visual tools for it, like a blend tree editor, and fix the root motion by having an explicit motion track baked into the animation clip instead of trying to compute the displacement per frame spontaneuously at runtime.

Feel free to check it out in its current bare-bones state on [github](https://github.com/JWki/gpu_skinning).


**All animation clips have been obtained from [Mixamo](https://www.mixamo.com/) under their respective license. The knight model has been obtained from [Sketchfab](https://sketchfab.com/3d-models/knight-armor-b94303a0e7004c20a1a9965fc2d87aa0) under CC Attribution and was rigged using the Mixamo auto-rigging tools.**

