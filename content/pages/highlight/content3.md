---
title: 'Multicore Function'
weight: 3
date: 2018-12-06T09:29:16+10:00
background: ''
align: right
---

  Considering the essence of the music game is the music played in the background, we would like to play the music when interacting with gamers in the game. Fortunately, RP2040 has two cores, which means it can handle two tasks at the same time. We adopt the multicore function in the SDK and use two threads to implement our music game.
