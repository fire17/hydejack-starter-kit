---
layout: post
title: GlobalData + XObject
description: >
  Multi-Processing in python done right!
sitemap: true
---
## GlobalData + XObject
## XObject
XObject makes a dynamic expando object in python that is built upon globaldata.
It can hold its own value, and also hold child xobjects.
These xobjects are global accross all processes, autosaved, and super easy to create with xo. generator

>
    from gd import * 
    newX = xo.newX                        # xo.newX is now shared across all processes
    newX.body.head.eyes = "beautiful"

    # xo.newX.show() outputs from any process
    newX = [None]
        body = [None]
            head = [None]
                eyes = ['beautiful']



## GlobalData
GlobalData allowes an easy way to pass data in realtime between processes.
Each process can subscribe to channels; Processes with shared channels can pass data between them.

>
    Every channel has 2 files saved for them (locally):
    .gdd for data – can hold large data
    .gdc for flag counter – just an int flag

Everytime data is updated in the channel, the process updated the flag aswell
and all the other processes will pickup on that change very quickly.
Since this data transfer is done over the filesystem, all of the data is auto saved, 

Each process can access the data whenever it needs to,
or be set to trigger everytime a channel (or xobject is updated)
the trigger function can be set by either process




*[HTML]: HyperText Markup Language
*[CSS]: Cascading Style Sheets
*[JS]: JavaScript
