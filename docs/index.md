# Ender 3 CNC Build Manual

Welcome to the Ender 3 CNC build manual. This guide walks you through converting an Ender 3 3D printer into a fully functional CNC machine.

!!! Note
    This guide is a work in progress and may contain errors. If you find any issues with hardware or instructions, please open an issue in [this repository](https://github.com/john-clark/EnderCNC).

!!! Warning
    This is the first version and will be updated quickly

!!! Tip
    Use the sidebar to navigate chapters.

# Overview

![image](images/447669414-df2746be-0fd8-4aa2-b609-81031dc4cfa2.png)
![image](images/447669480-43854a83-0945-4e80-aa53-9ccf8a7e4b0b.png)

Print settings I used: PLA+, 5 wall, 5 top, 5 bottom, 40% gyroid.

## Setup

Im just running the original MCU with Klipper for the control and Fusion360 for CAM (free version) with a klipperized post processor. So far no real issues. You might want to swap to a board with TMC control (skr pico/micro4) if you realy want to push it.  Im using an old laptop with Ubuntu with klipper on as a substitute for a Raspberry pi. 

You can of course go the GRBL route if you want. I just wanted to use klipper since people coming from 3D printers are somewhat familiar with that.

- Reusing as much as possible from the Ender 3 PRO down to the screws.
- Cheaper BOM than the original EnderCNC. BOM is mostly just some screws, 2x linear rails for Z and m3/m5 tnuts.
- Easy to scale up or down to any size if not using Ender 3 Pro frame. 

### Reused Parts

* Frame
* steppers
* wires (might need to extend some)
* leadscrew
* leadscrew nut
* coupler
* mcu
* psu
* most of the nuts and bolts
* vwheels
* alu spacers
* screen if you want

