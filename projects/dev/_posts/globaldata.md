---
layout: post
title: GlobalData + XObject
description: >
  Highest level environment imaginable 
sitemap: true
---

## GlobalData + XObject
## Multi-Processing in python done right!


GlobalData allowes an easy way to pass data in realtime between processes.
Each process can subscribe to channels; Processes with shared channels can pass data between them.

XObject makes a dynamic expando object in python that is built uppon global data.
These xobjects are global accross multi processes.

> Every channel has 2 files saved for them: |
.gdd for data – can hold large data
.gdc for flag counter – just an int flag

Everytime data is updated in the channel, the process updated the flag aswell
and all the other processes will pickup on that change.

Each process can access the data in a lazy way whenever it needs to,
or be set to trigger everytime a channel (or xobject is updated)



*[HTML]: HyperText Markup Language
*[CSS]: Cascading Style Sheets
*[JS]: JavaScript
