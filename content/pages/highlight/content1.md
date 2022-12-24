---
title: 'PWM PIO Module'
date: 2018-12-06T09:29:16+10:00
weight: 1
background: ''
align: right
image_src: "https://source.unsplash.com/_v-EHHKKW3w/1600x700"
---

The reason why we used the PIO modules to implement the PWM function rather than other functions is straightforward and simple:  
Most I/O functions would be using the PWM modules as vehicles.  
PIO, an independent hardware module on RP2040, would be much more efficient when compared with GPIO to control the I/O stream. 
Music play and instrumental sound generation would be possible using the PIO module without initializing and utilizing more GPIO functions. 
The responsibility of the PIO PWM module, based on our function design and proposal, would be generating the PWM signal to convey our predefined music in game mode and play specific music notes in digital instrument mode.