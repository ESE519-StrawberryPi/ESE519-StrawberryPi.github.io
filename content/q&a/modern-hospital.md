---
title: 'Storage Interrupt'
date: 2018-11-18T12:33:46+10:00
draft: false
weight: 2
heroHeading: 'Storage Interrupt'
heroSubHeading: 'Calling additional API to disable interrupts and recover.'
heroBackground: 'https://unsplash.com/photos/GNyjCePVRs8/download?ixid=MnwxMjA3fDB8MXxzZWFyY2h8Mnx8aGFyZGRyaXZlfGVufDB8fHx8MTY3MTg1MTAxNw&force=true'
thumbnail: 'https://unsplash.com/photos/GNyjCePVRs8/download?ixid=MnwxMjA3fDB8MXxzZWFyY2h8Mnx8aGFyZGRyaXZlfGVufDB8fHx8MTY3MTg1MTAxNw&force=true'
---

Calling additional API `save_and_disable_interrupts` and `restore_interrupts` to disable interrupts and recover them.

When trying to store data in flash memory, we found out that after erasing the flash memory for a certain address range, we are still unable to write it. After checking the Internet, we found out that the interrupts from other read or write requests from the program between these two commands may make the saving or loading data impassible to finish or complete correctly.  Thus, we. add two system functions to avoid the impact from interrupts:

`save_and_disable_interrupts` and `restore_interrupts` . The first function is to disable any potential interrupts and store current situations in storage. The latter function is to recover from the disabled situation and resume normal work. We could then safely read or write flash memory between calling these two functions.