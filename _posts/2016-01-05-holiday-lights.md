---
title: Holiday Lights
project: holiday-lights
published: true
---

Speaking of Adafruit Neopixels, let me explain the project I recently used them in. This was an Hour of Code activity inspired by one of Made With Code's previous initiatives.

So I set out to make my own. Being able to program something that's right in front of you is a lot more powerful than just the image of a simulated Christmas tree.
<!--more-->

Here's a video of Made With Code's initiative:

<iframe width="560" height="315" src="https://www.youtube.com/embed/7FlzFH9xOF8" frameborder="0" allowfullscreen></iframe>


At first, I was going to use regular RGB LEDs and an LED driver similar to the one I used in the Star dress, since I've done that before. But I got frustrated with the sheer amount of wires that had to go down the tree for just one strand of lights! I eventually found Neopixels, which provide a way to address each light in series.

I wrote a simple c++ class that extended the Adafruit NeoPixel library (super handy!) including a COLORS enum, though I did leave the RGB functionality in for particularly ambitious kids.

I recruited kids from [The 2nd Law Enforcers](www.farmingtonrobotics.org) to help me assemble the electronics and test the software. A group of about 4 kids with no soldering experience learned to solder and assembled strings of Neopixels connected with sections of ribbon cable. That was a lot of cutting, stripping, tinning, and soldering practice.

Honestly, I would have loved to use the tree in a high school level setting. Many of my recruits loved programming just the 8-LED stick, and could have done some really cool stuff with the entire tree.

There was one piece that I hadn't been able to finish before the Hour of Code: the actual interface that students could use to program! I had installed the Arduino IDE on several of the school MacBook Airs, but due to their student settings they did not have permissions to the USB ports. Eventually (and by that I mean half way through the week) I found a Web app called [codebender.cc](codebender.cc) and it worked like a charm!
