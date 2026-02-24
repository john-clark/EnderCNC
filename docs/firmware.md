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
   - Set stepper, endstop, spindle, and belt parameters.  
3. Test all axes manually before enabling motor power.  
4. Configure homing and probe offsets for your spindle.

---

## 3. GRBL Setup

1. Flash your GRBL-compatible board according to manufacturer instructions.  
2. Use the reference configuration for stepper settings, endstops, and spindle control.  
3. Test movement manually before running any G-Code.

---

### Tips

!!! tip
    Keep a backup of working firmware configuration before making major changes.

!!! warning
    Never run motors at full speed during first test — verify wiring and mechanical alignment first.
