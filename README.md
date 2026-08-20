# Assistive Rotary Keyboard

A joystick-and-button based assistive typing device built on the Raspberry Pi Pico W, 
inspired by the [Chahor rotary keyboard project](https://github.com/clackups/chahor_rotary_keyboard).

## Overview
Designed for users with limited fine motor control, this device lets someone scroll 
through characters using a joystick and select them with tactile buttons — sending 
real keystrokes to a connected computer via USB HID.

## Features
- Character scrolling via analog joystick (with auto-repeat acceleration)
- 8 tactile buttons: character select, uppercase, space/enter, backspace, layer switch, navigation, SOS
- ST7735 1.8" TFT display for real-time visual feedback
- USB HID keyboard output (CircuitPython `usb_hid`) — types directly into any connected device
- SOS alert: long-press trigger with visual + buzzer alarm
- Custom rechargeable power supply: 2S Li-ion pack, BMS protection, TP4056 USB-C charging, LM2596 step-down regulation

## Hardware
- Raspberry Pi Pico W
- 1.8" ST7735 TFT display (SPI)
- Analog joystick module (KY-023 / HW-504)
- 8x tactile push-buttons
- Piezo buzzer
- 2x 18650 Li-ion cells + BMS + TP4056 + LM2596

## Wiring
See `docs/wiring.md` for the full pinout table.

## Firmware
Built with CircuitPython 10.x. Required libraries (Adafruit CircuitPython Bundle):
- `adafruit_st7735r`
- `adafruit_display_text`
- `adafruit_hid`
- `adafruit_bus_device`

## Status
Actively in development — breadboard-validated, currently being migrated to perfboard.

## Motivation
Built as an accessibility-focused hardware project to explore low-cost, DIY 
alternatives to commercial AAC (augmentative and alternative communication) devices.

## License
MIT
