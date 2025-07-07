---
title: "RC Battle Car"
author: "@Irtaza"
description: "A remote-controlled car that can shoot and detect lasers with a custom remote!"
created_at: "2024-07-07"
---

## July 7th: Research + Schematic

Went through multiple open-source mini RC car projects' repos and videos like [Racer](https://github.com/StuckAtPrototype/Racer/) by [StuckAtPrototype](https://github.com/StuckAtPrototype)! After countless hours of searching online, I decided to use the **ESP32WROOM32** devkit as the main MCU. Then I made a list of the features I was planning on adding, and thus made a list of components! This project would require **2 separate PCBs**, one for the car and one for the remote. 

After that, I opened up **KiCAD** and made a project for the car's main board and added all the components required and (hopefully correctly) finished up routing the _battery-management-and-programming USB-C TP4056_ block!

There are a lot of components left unrouted, but will look at them tomorrow!

<img width="980" alt="KiCAD Schematic" src="https://github.com/user-attachments/assets/5eb41caf-4950-458a-a4b6-2d819c1f4786" />

**Total time spent: 4 hours**
