# E3CNC Motherboard Documentation

Creality _USED_ to do a good job of documenting their products and publishing information to GitHub ([https://github.com/CrealityOfficial](https://github.com/CrealityOfficial)**)** and is one of the reasons why they used to be popular. Now they have closed up and so we typically go with 3rd party solutions like BigTreeTech.

_This is just a summary of what we could find on GitHub of needed configuration information for motherboards that were shipped with the Ender 3 for the E3CNC project._

We will include the CR10 as that is very similar to the old Ender3 models. We will not cover newer printers like the Ender-3 V3 series, K1, etc. and their use of custom boards (GD32-based for V3 SE/KE or the STM32F401 on the s1) because these are not suitable for our purposes. Especially with their cost-saving extrusions no longer being repurposable (another change we don’t like that Creality has made.)  
  
This is focused on the E3CNC project and the mainboards that we can ‘upcycle’ printers that would otherwise be sent to the landfill due to manufacturers no longer supporting them.

### Diffference between klipper on a 3D printer and CNC

The E3CNC uses 2 motors and 2 endstops for the Y axis to make sure the gantry is square.

The X axis runs horizontally along the gantry and Z axis runs vertically.

Since we do not use the Extruder, we rearrange the driver assignments for the dual Y axis.

> “The reason we are swapping the X stepper to the E driver is because on the 4.2.2/4.2.7 boards are bit higher "run_current"/amp than the rest of the drivers by default, and since the X motor is alone on the CNC we want it to get more power. Of course, you can adjust Vref though and put them wherever if you want. Just in case you were wondering why steppers and drivers don’t match up” -Ravenkeeper

This goes for pin assignments as well, in Klipper we can assign the bed thermistor or nozzle thermistor to an binary on/off pin just like the endstops.
