+++
title = "Interview Simulator"
description = "An interview practice tool. Overall winner of the SheHacks+ 7 hackathon!"
weight = 1

[extra]
local_image = "/projects/interviewsim.jpeg"
+++

![A screenshot from an Oculus HMD. A cutout of Henry Henderson from the anime Spy x Family is shown behind a desk, and behind him is the word "irrelevant" in large font.](/projects/interviewsim.jpeg)
*man how am i gonna get operation strix done now*

An interview practice tool made with Unity (and the Oculus SDK), Python (Flask, Co:here's API wrapper), and an Arduino. The Arduino board was used to send IMU movement to a websocket server, and the Unity project received that info to rate your handshake. With help from an API wrapper made in Flask, you could speak your answer to the question "tell me about yourself", and the project transcribes that response and tells you if your answer was mostly positive, mostly negative, or completely irrelevant.

I was responsible for the API wrapper, which I mainly made because there were [too many headers and too many response fields on a single Cohere API request](https://docs.cohere.ai/reference/classify), and I did not want to add and filter all of that in C#. Work smarter, not harder!

This project won first place overall, best ~~actually, only~~ hardware hack, and 3rd place in Co:here's *Best Use of Prompt Engineering* category. ~~It also helped land me an internship the summer of 2023!~~


Here's the [Devpost submission](https://devpost.com/software/interview-simulator-2023). Go check out the [Unity project](https://github.com/mariagarcia466/Interview-Sim), the [Arduino websocket code](https://github.com/EmilyGoose/Interview-Sim-Arduino), and the [API wrapper code](https://github.com/fenreese/Interview-Sim-APIWrapper).
