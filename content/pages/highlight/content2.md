---
title: 'Flash Memory Storage'
weight: 2
date: 2018-12-06T09:29:16+10:00
background: 'https://unsplash.com/photos/oYdmb6kqI7w/download?ixid=MnwxMjA3fDB8MXxhbGx8MXx8fHx8fDJ8fDE2NzE4NDg3ODk&force=true'
align: left
---

  Only playing impromptu music is not that exciting. What people really like is long-standing memory. Thus, with the need to store impromptu music playing under the instrument mode, we need to find a storage medium to save these precious records.

  Several options are available to us: using an external storage medium, for example, an SD card, using the integrated memory, for example, the flash memory in RP2040, or saving data to another chip or connected PC. The shortcoming and advantages of these methods are obvious. Using an SD card is convenient, but it takes some extra budget, and more time should be put into the FAT32 driver for SD cards. Using the built-in flash memory would be easy to implement and completely at no cost, while the storage space is strictly limited. Saving data to an external device is also of no cost while also having few limitations of amounts of space, but not profitable.

  The last decision is to use flash memory as the storage medium, which is of no cost. Since the audio data is not as large as images and video, the storage space limitation is not that severe.