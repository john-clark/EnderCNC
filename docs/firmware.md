# Firmware Setup

This chapter explains firmware options for your Ender 3 PRO CNC conversion.

---

## 1. Options

| Firmware | Notes |
|----------|-------|
| Klipper  | Recommended if using Raspberry Pi or similar |
| GRBL     | Standard CNC option, works with ESP32/32-bit boards |

---

## 2. Klipper Setup

1. Follow standard Klipper installation on your Raspberry Pi or Linux laptop.

2. Copy a reference `printer.cfg` for the Ender CNC:
   * Set stepper, endstop, spindle, and belt parameters for your MCU
   * Make sure all motors are spinning correctly
  
3. Test all axes manually before enabling motor power.

4. Configure homing and probe offsets for your spindle.


### Example configs

* [Version 1.1.x Ender MCU printer.cfg](/klipper/v1.1.x_printer.cfg)
* [Version 4.2.2 Ender MCU printer.cfg](/klipper/v4.2.2_printer.cfg)
* [Version 4.2.7 Ender MCU printer.cfg](/klipper/v4.2.7_printer.cfg)

### How to document your mainboard

Notice in the picture that the processor and motor has documented pins.

![Creality v1 mcu](images/enderv1mcu.png)

---

## 3. GRBL Setup

1. Flash your GRBL-compatible board according to manufacturer instructions.  
2. Use the reference configuration for stepper settings, endstops, and spindle control.  
3. Test movement manually before running any G-Code.

---

### IMPORTANT NOTES

>Don't let the magic smoke out!

!!! tip
    Keep a backup of working firmware configuration before making major changes.

!!! warning
    Never run motors at full speed during first test

!!! warning
    Verify wiring because Creality motors have crossover wires.

 !!! warning
    Y axis has one motor inverted. Test Y motor without belts first.
