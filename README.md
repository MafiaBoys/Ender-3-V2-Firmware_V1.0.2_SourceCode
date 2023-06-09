# Creality Ender 3 v2 Marlin 2.0 Firmware 1.2 

![GitHub](https://img.shields.io/github/license/marlinfirmware/marlin.svg)
![GitHub contributors](https://img.shields.io/github/contributors/marlinfirmware/marlin.svg)
![GitHub Release Date](https://img.shields.io/github/release-date/marlinfirmware/marlin.svg)

<img align="right" width=175 src="buildroot/share/pixmaps/logo/marlin-250.png" />

Additional documentation can be found at the [Marlin Home Page](http://marlinfw.org/).
Please let us know if Marlin misbehaves in any way. Volunteers are standing by!

## Marlin 2.0 for Creality MotherBoard 4.2.2 shipset ARM/STM32F103RCT6

Marlin 2.0 takes this popular RepRap firmware to the next level by adding support for much faster 32-bit and ARM-based boards while improving support for 8-bit AVR boards. Read about Marlin's decision to use a "Hardware Abstraction Layer" below.

Download earlier versions of Marlin on the [Releases page](https://github.com/MarlinFirmware/Marlin/releases).

## build Marlin (PlatformIO with VSCode)
PlatformIO turns VSCode into a complete IDE for compiling and developing Marlin.
![Logo](https://marlinfw.org/assets/images/basics/install_platformio_vscode/platformio_vscode_screenshot.png)


## Install VSCode

Visit the ![Setting up Visual Studio Code]([https://www.google.com](https://code.visualstudio.com/docs/setup/setup-overview)) page to download and install the latest VSCode for your particular platform.
![logo](https://marlinfw.org/assets/images/basics/install_platformio_vscode/install_platformio_vscode.png)
## Install PlatformIO IDE
The first time you open the Marlin project in VSCode it will recommend you install the Auto Build Marlin extension, which will also install PlatformIO IDE. Simply answer “Yes” to install the extensions, or follow the instructions below.

## Open Marlin in VSCode / PlatformIO
Unzip the downloaded archive to your preferred location. (Although modern systems can handle very long paths, it may still help with the build process if the filepath is short without any special characters.)

You can open Marlin in Visual Studio Code in one of several ways:

    1- Drag your downloaded Marlin Firmware folder onto the Visual Studio Code application icon.
    2- Use the Open… command in the VSCode File menu.
    3- Open the PIO Home tab and click the “Open Project” button.






## Used By 0xKnock
Proplems:

- Fixed Build Proplem
- Fixed Z-Axis Endstop Switch


Ender 3 Z-Axis Endstop Switch Problem 

[Watch on Youtube](https://www.youtube.com/watch?v=O4idrobsljs&t=3s&ab_channel=Tombof3DPrintedHorrors).


## Note
The reason for Z-Axis Endstop Switch problem is not from adjusting the angle of the stop button, rather it is from the firmware Configuration. To fix the problem, you must first modify the wires of the stop button in order for it to fit into the end logic :heavy_check_mark:true not :x:false
```Configuration.h```

```
// Mechanical endstop with COM to ground and NC to Signal uses "false" here (most common setup).
#define X_MIN_ENDSTOP_INVERTING false // Set to true to invert the logic of the endstop.
#define Y_MIN_ENDSTOP_INVERTING false // Set to true to invert the logic of the endstop.
#define Z_MIN_ENDSTOP_INVERTING true <====================================================== // Set to true to invert the logic of the endstop.
#define X_MAX_ENDSTOP_INVERTING false // Set to true to invert the logic of the endstop.
#define Y_MAX_ENDSTOP_INVERTING false // Set to true to invert the logic of the endstop.
#define Z_MAX_ENDSTOP_INVERTING false // Set to true to invert the logic of the endstop.
#define Z_MIN_PROBE_ENDSTOP_INVERTING false // Set to true to invert the logic of the probe.
```
