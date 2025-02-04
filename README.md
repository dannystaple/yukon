# Pimoroni Yukon <!-- omit in toc -->

This repository is home to the MicroPython build, library, and examples for Pimoroni Yukon.

[![Build Status](https://img.shields.io/github/actions/workflow/status/pimoroni/yukon/micropython.yml?branch=main&label=MicroPython)](https://github.com/pimoroni/yukon/actions/workflows/micropython.yml)
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/pimoroni/yukon)](https://github.com/pimoroni/picovision/releases/latest/)

- [Introduction](#introduction)
- [Download MicroPython](#download-micropython)
  - [Firmware Only](#firmware-only)
  - [With Filesystem](#with-filesystem)
- [Flashing the Firmware](#flashing-the-firmware)
- [Examples](#examples)
- [Documentation](#documentation)


## Introduction

Yukon is a high-power modular robotics and engineering platform, able to drive your most ambitious of robots, props or contraptions!

Powered by the RP2040, Yukon leverages the chip's unique pin capabilities to offer six slots for attaching a range of interchangeable hardware modules for driving high-powered devices. This lets you control motors, servos, steppers, speakers, LED strips, and more, all from a single board!

Customise Yukon to suit almost any project, or start with a few modules and expand as a project grows. There is also a proto module for adding more features! Each module is screwed down to ensure a solid mechanical and electrical connection.

* :link: [Buy a Yukon here](https://shop.pimoroni.com/products/yukon)

## Download MicroPython

Grab the latest release from [https://github.com/pimoroni/yukon/releases/latest](https://github.com/pimoroni/yukon/releases/latest)

There are two .uf2 files to pick from:

### Firmware Only

* `pimoroni-yukon-vX.X.X-micropython.uf2`

This build includes only the firmware needed for Yukon to function. You will need to manually update the `lib/pimoroni_yukon` library afterwards to get the latest features and bug fixes.


### With Filesystem

:warning: **This option will overwrite the entire contents of your Yukon! Be sure to back up files to your PC before installing!**

* `pimoroni-yukon-vX.X.X-micropython-with-filesystem.uf2 `

This build contains both the firmware for Yukon and the library files needed to take full advantage of the hardware.

## Flashing the Firmware

1. Connect Yukon to your computer using a USB A to C cable.

2. Turn off your board by pressing the PWR button. The green light should turn off.

3. Put your board into bootloader mode by holding the BOOT/USER button whilst pressing the PWR button to turn the board on. The green light should turn on, and the lights next to the A and B buttons should have a dim glow.

4. Drag and drop one of the `pimoroni-yukon-vX.X.X...` .uf2 files to the "RPI-RP2" drive that appears.

5. After the copy completes your board should reset and, if you used the `with-filesystem` variant, should start playing a flashing pattern on the A and B LEDs.

:information_source: **Overwriting Yukon's filesystem can take multiple minutes to complete.**


## Examples

There are many examples to get you started with Yukon, located in the examples folder of this repository. Details about what each one does can be found in their respective sections:

* [Examples: Board](/examples/board/README.md)
* [Examples: Modules](/examples/modules/README.md)
* [Examples: Showcase](/examples/showcase/README.md)


## Documentation

To take Yukon further, the full API is described in the [documentation readme](/docs/README.md)
