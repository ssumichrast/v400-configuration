
# FLSUN V400 Klipper Configuration

This project is a simple repository for the Klipper configuration I am using on my [FLSUN V400](https://flsun3d.com/pages/v400).
# Documentation

## V400 Basic Information

The V400 uses a [MKS Robin Nano v2](https://github.com/makerbase-mks/MKS-Robin-Nano-V2.X) mainboard to control the stepper motors and extruder. Since these mainboards are very simple, FLSUN elected to use [Klipper](https://www.klipper3d.org) to be the controller. FLSUN shipped their [Speederpad](https://flsun3d.com/pages/speeder-pad) with the V400 to run Klipper on. However, the Speederpad was pretty underpowered, closed source, received next to no updates and required the use of custom Klipper configurations/builds. They also were using repositories that were no longer available.

## My V400 with a Raspberry Pi controller

My V400 is using a [Raspberry Pi 3b](https://www.raspberrypi.com/products/raspberry-pi-3-model-b/) as the Klipper controller instead of the FLSUN Speederpad. While this gives much more control over the Klipper environment, it also means needing to be responsible for owning the printer.cfg and associated files to run the printer.

Using external Klipper means also needing to flash the MKS board with updated Klipper code as it's generated. This is done using [Klipper Install And Update Helper (KIAUH)](https://github.com/dw-0/kiauh). Once complete, the firmware is placed on a micro SD card and the printer rebooted. This then lets the Raspberry Pi with a modern Klipper access the MKS board and control the printer. All functions of the V400 are accessible by using these configuration files.

## Using Input Shaper

I am using a Pico input shaper as well to calibrate the printer as needed.

# Acknowledgements

The configuration built here is based off work from [Guilouz](https://www.github.com/Guilouz).

