---
layout: post
title: GlobalData + XObject
description: >
  Highest level environment imaginable 
sitemap: true
---

## GlobalData + XObject
## Multi-Processing in python done right!

### GlobalData
GlobalData allowes an easy way to pass data in realtime between processes.
Each process can subscribe to channels; Processes with shared channels can pass data between them.

> Every channel has 2 files saved for them (locally):
    .gdd for data – can hold large data
    .gdc for flag counter – just an int flag

Everytime data is updated in the channel, the process updated the flag aswell
and all the other processes will pickup on that change very quickly.
Since this data transfer is done over the filesystem, all of the data is auto saved, 
somedata

### XObject
XObject makes a dynamic expando object in python that is built uppon global data.
These xobjects are global accross multi processes, autosaved, and super easy to create with xo. generator

>
    x = xo.newX # xo.newX is now shared across all processes
    x.body.head.eyes = "beautifull'

Each process can access the data whenever it needs to,
or be set to trigger everytime a channel (or xobject is updated)
the trigger function can be set by either process



*[HTML]: HyperText Markup Language
*[CSS]: Cascading Style Sheets
*[JS]: JavaScript
