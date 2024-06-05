# Troodon-Mini-Pro-Klipper

** REMEMBER TO UPDATE THE SERIAL NUMBER IN THE PRINTER.CFG WITH THE ONE CORRESPONDING TO YOUR PRINTER **
** SSH into the printer (username biqu, password biqu) and send ls /dev/serial/by-id/* **
** Copy the serial number and replace the one currently in the [mcu] section of the config **

A Klipper config for Troodon Mini Pro

This is a custom Klipper config for the Troodon Mini Pro with Stealthburner and Tap. 

It has a variety of optimizations and quality of life features, including:

1. Exclude object
2. Nozzle wipe macro
3. Purge line macro
4. Setup for Mellow USB acceleromter
5. Speed optimizations for homing, meshing, and gantry levelling.
6. Motherboard fan configured to turn on only when printing to reduce noise
7. Exhaust fan configured for either temperature or manual control
8. Optimized PRINT_START macro.

It is recommended to use the built-in OrcaSlicer profile for Troodon 2 - Klipper, but change the printable area to 250 x 250 x 230 and edit the start g-code to remove the "M109 S[nozzle_temperature_initial_layer]" command, so as to avoid uneccesary heating of nozzle before it is cooled back to 150 for probing with tap.

Optionally, import the included filament and profile preset for fast printing and change the bed texture image to the provided one for the Mini. Note that this filament preset has a configured maximum volumetric flow of 20 mm^3/s which is only achievable with a CHT nozzle.
