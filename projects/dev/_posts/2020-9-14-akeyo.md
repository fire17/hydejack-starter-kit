---
layout: post
title: GlobalData + XObject
description: >
  Highest level environment imaginable 
sitemap: true
---

## AkeyO

AkeyO is an app that will let you order anything you want and let the market haggle over you.
You type what you want, for example: akeyo pizza.
All the pizza providers in your area will be notified of your intension to buy,
Sending you their best live offer.


## Alpha To Omega

#### Let the market know what you want






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
