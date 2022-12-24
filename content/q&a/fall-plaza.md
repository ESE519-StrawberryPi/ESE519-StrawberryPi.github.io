---
title: 'PWM Signal Noise'
date: 2018-11-18T12:33:46+10:00
draft: false
weight: 1
heroHeading: 'PWM Signal Noise'
heroSubHeading: 'Revitalising a public space in Spain.'
heroBackground: 'work/song-before.jpeg'
thumbnail: 'work/song-before.jpeg'
images: ['work/song-before.jpeg', 'work/song-after.jpeg', 'work/1-before.jpeg', 'work/1-after.jpeg', 'work/demo.jpg']
---
Using an additional electric capacity to filter high frequency noise.

We could generate the sounds and send them to the speaker by utilizing the PWM PIO module. We found some apparent loss in the sound quality when listening to the speaker after the amplifier.  By using the oscilloscope in Detkin Lab, we find out there is a very obvious overshooting at the beginning of each PWM signal period.

For both methods we deployed here, i.e., using different clocks and frequencies or using different duty ratios, the overshooting could not be negligible.

We got some advice from Professor Dalton about the loss in audio quality. According to Professor Dalton, a low pass filter would be helpful to filter out those high-frequency noises. With TA Bhagath Cheela, we can filter almost all those high-frequency noises by parallel connecting a 1 nF capacitance with the speaker and amplifier. The filter result is shown as follows:
