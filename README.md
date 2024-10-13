# TurtleNeck2.0
![TN2](https://github.com/user-attachments/assets/d13e9ee4-a6a7-497b-9383-50f858e20ab2)
TurtleNeck 2.0 - The smart toolhead buffer.

AT Discord:

[![Join me on Discord](https://discord.com/api/guilds/1229586267671629945/widget.png?style=banner2)](https://discord.gg/armoredturtle)

TurtleNeck 2.0 (TN2) Is a toolhead buffer for klipper printers designed to work with the [AFC Klipper Add-on](https://github.com/ArmoredTurtle/AFC-Klipper-Add-On).
It ustilizes an STM32G0B1 MCU over usb-c to operate. Making it a single cable addition to your klipper machine.

TN2 utilizes two hall effect sensors to dectect movement of the buffer before hitting a hard stop in either direction. Adiddtionally on the PCB are 5 endstops ports that can be utilized for filament combiners or "hubs".
The purpose of a toolhead buffer such as TN2 is to compensate for mismatched rotation distances between a toolheads extruder and a direct drive AFC ("type 2 MMU" if you like calling them that...)
