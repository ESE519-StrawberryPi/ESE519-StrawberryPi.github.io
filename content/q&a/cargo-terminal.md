---
title: 'Pressing Sample'
date: 2018-11-18T12:33:46+10:00
draft: false
weight: 3
heroHeading: 'Pressing Sample'
heroSubHeading: 'Sample keypad pressing.'
heroBackground: 'https://unsplash.com/photos/utWyPB8_FU8/download?ixid=MnwxMjA3fDB8MXxzZWFyY2h8OXx8a2V5cGFkfGVufDB8fHx8MTY3MTg1MTU1NA&force=true'
thumbnail: 'https://unsplash.com/photos/utWyPB8_FU8/download?ixid=MnwxMjA3fDB8MXxzZWFyY2h8OXx8a2V5cGFkfGVufDB8fHx8MTY3MTg1MTU1NA&force=true'
---

How to sample the pressing of gamers, whether in the music game mode or digital instrument mode, is a big problem. 

In the initial version of our project, we used the keyboard as input and used the getchar_timeout_us function in pico/stdio.h . The timeout period would be used as the sample period. After switching from the keyboard to the keypad, we had to redesign the sampling method since no input function is built into the SDK for us to deploy for the keypad directly. 

As a solution, we override the original getchar_timeout_us function, which is called get_key_timeout_us, to receive input from the keypad while also having a time limit. We manually set the sample rate of pressing on the keyboard as four times per second by setting the timeout of the keypad input function to 250ms. Doing so could guarantee a stable sample of pressing while not using too much space to store the pressing samples in the flash memory when recording gamers’ own patterns. 