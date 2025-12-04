+++
showonlyimage = true
draft = false
image = "img/portfolio/dx12_renderer/thumbnail.jpg"
date = "2019-10-24"
title = "D3D12 Renderer"
weight = 0
+++

No better way to learn a new graphics API than to use it!
<!--more-->

![ineditor][1]
*Yep, that's the Qt text editor example hosting a D3D12 renderer.* 

Not a lot to say about this one really - my first real foray into D3D12 after having used D3D11 and OpenGL before that.
Part of a greater vision - as always - this basically ended up being a tiny little D3D12 renderer with physically based material rendering (you gotta have it!) and sunlight shadows (single cascade). I also ended up playing with an out-of-process editor using Qt instead of my beloved [dear imgui](https://github.com/ocornut/imgui) with communication being done over web sockets. 

![moreeditor][2]
*A more proper UI in Qt, running in a separate process to the renderer.* 

Also my first time dealing with GLTF model / scene files - I used a custom binary format for models but wrote an importing pipeline for GLTF this time to see how it is. I am yet undecided how much I like the format, I have a few issues with it but it's fine as an exchange format I guess.


[1]: /img/portfolio/dx12_renderer/texteditor.jpg 
[2]: /img/portfolio/dx12_renderer/editor.png 