---
title: "EventModeling Cheat Sheet"
date: 2020-12-09T22:15:58-07:00
description: "Need a cheat sheet for the basic building blocks and how they are being orchestrated in patterns in EventModeling? Use these examples in order to get onboard quickly."
keywords: [Event Modeling, Specification, Patterns, Building Blocks]
author: sbortz
---

![EventModeling Cheat Sheet](cheatsheet.jpg)
<sub>[high res version](cheatsheet.jpg)</sub>

If you start an EventModeling workshop it is important to get everyone quickly. 

on board quickly and not everybody is familiar with EventModeling. Use this cheat sheet in order to quickly get everyone on board and let everyone see the simplicity behind EventModeling.

# Building Blocks
On the left side there are the possible building blocks you can use in your Event Model:

* Trigger: An Interface which can be a UI or a public Rest-API. Or an automated process# Patterns
* Command: Stands for an intention
* View: Stands for Conclusion, Report or ReadModel.
* Event: Stands for a business fact that has been saved to disk

On the right side the possible patterns are shown and how the building blocks are being connected:

# Patterns
Internal Patterns:
![Command and View Pattern](command-view-pattern.jpg)

Patterns that automate and/or do external communication
![Automation and Translation Pattern](automation-translation-pattern.jpg)