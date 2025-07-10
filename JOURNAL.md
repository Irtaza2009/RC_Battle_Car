---
title: "RC Battle Car"
author: "@Irtaza"
description: "A remote-controlled car that can shoot and detect lasers with a custom remote!"
created_at: "2024-07-07"
---

## July 7th: Research + Car Schematic

Went through multiple open-source mini RC car projects' repos and videos like [Racer](https://github.com/StuckAtPrototype/Racer/) by [StuckAtPrototype](https://github.com/StuckAtPrototype)! After countless hours of searching online, I decided to use the **ESP32WROOM32** devkit as the main MCU. Then I made a list of the features I was planning on adding, and thus made a list of components! This project would require **2 separate PCBs**, one for the car and one for the remote. 

After that, I opened up **KiCAD** and made a project for the car's main board and added all the components required and (hopefully correctly) finished up routing the _battery-management-and-programming USB-C TP4056_ block!

There are a lot of components left unrouted, but I will look at them tomorrow!

<img width="980" alt="KiCAD Schematic" src="https://github.com/user-attachments/assets/5eb41caf-4950-458a-a4b6-2d819c1f4786" />

**Total time spent: 4 hours**

## July 8th: Car Schematic Completion

Routed all the parts left from yesterday and then added a laser (2-pin connector) and connected it using an NPN transistor (because I am going to use KY008, which runs on 5V, so it needed a direct connection from LiPo). Then, I added 4 3-pin connectors for the IR sensors and routed them all to the ESP32. I don't actually know right now if I am routing everything to the right pins on the MCU 🫠. Also added 3 LEDs for indicating lives remaining, and a live reset button to, well, reset lives! Also added _ESD protection_ on USB-C (had to look at a few schematics online to figure out how it's done 😅). 

Finally, to make everything actually understandable and readable, I separated each part and placed all the components nicely, and then labelled each part and made a nice rectangle around it! Now it seems more professional!!

And then added an LED to know when the car is turned on!

![KiCAD Schematic Organised](https://github.com/user-attachments/assets/fdb5311f-afa5-4456-bbe2-83e877720bf8)


**Total Time Spent: 4.5 hours**

## July 10th: Remote Schematic

I began working on the remote! It will only have a joystick and one button, and it will operate using an ESP32 WROOM-32, the same as the car. Additionally, it will share the same power system as the car, running off a LiPo battery with TP4056 for battery management. I'm also using the same USB-to-serial wiring as well!

I did have to modify the power logic slightly because, unlike the car, the remote can operate entirely on 3.3V. This means that no component needs a direct connection to the LiPo. Even though I started the schematic from scratch and didn't copy any parts from the car's schematic, it took me much less time to place all the components and wire them for the remote!

![image](https://github.com/user-attachments/assets/a2168d44-2009-4663-9d8a-412d3eda6cfa)

**Total time spent: 2.5 hours**

