+++
title = "KikuKaku"
description = "HearWrite in Japanese. A learning tool for non-English handwriting in VR!"
weight = 2

[extra]
local_image = "/projects/kikukaku.jpg"
+++

![A screenshot from an Oculus HMD. A pop-up menu near the top of an image shows the word "bentou" in Japanese, along with buttons to cancel, change the size of a letter, undo the latest letter, and submit the word. Below it is a whiteboard for the user to write a letter on. There is a left hand holding a pen in front of the whiteboard.](/projects/kikukaku.jpg)
*there is a べんとう behind this big writing surface*

My fourth year honors thesis. Written as 聞く書く in Japanese, it is a virtual reality learning application meant to help learners refine their listening and handwriting skills in non-English languages. Made with Unity and the OpenXR toolkit, you are to "own" as much vocabulary objects as possible by correctly writing the word you hear. This was my first solo VR project (the rest were group hackathon projects), so I was responsible for doing *everything*, from the game design to the API behind it. 

I'm particularly proud of the implementation of the writing board/canvas in VR - I took inspiration from the whiteboards in Half-Life: Alyx and got help from [this article](80.lv/articles/recreating-the-drawing-mechanic-from-half-life-alyx-in-unity) with implementing it. Because the process was a bit hacky, though, there were a few problems with needing to clear the canvas after each successful character write. I ended up quickly patching by destroying the object, waiting a bit, and then spawning the object again. 

The character recognition was a simple multilayer perceptron machine learning model, which is pretty much converting an image into pixels and numbers, then having the computer learn what combinations of pixels are associated with which Japanese hiragana character in order to predict them. The model is 99% accurate in its predictions, which shocked even me. It was implemented in Tensorflow with Keras, and deployed as a Flask API. 

Here is [a video](https://youtu.be/ENDjb0ghphA) of some gameplay. Also see: the [source code](https://github.com/vialab/JPHandwriting).
