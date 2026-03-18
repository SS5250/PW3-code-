# Mouse Project – PWM Code

This repository contains the firmware used to control the wire‑guided Mouse Project vehicle.

## What it does
- Detects the 20 kHz track signal using pickup coils and basic filtering
- Calculates how far the mouse is from the centre of the wire and adjusts steering automatically
- Controls two DC motors using PWM through a MOSFET driver
- Reduces speed in corners when the sensors become less reliable at higher speeds

## Structure
- `src/` – Contains all main code for running the mouse, including the control loop, sensor reading, and PWM motor output.
- `include/` – Holds configuration and header files, such as pin assignments and control parameters.
- `docs/` – Stores extra project information, including tuning notes, energy‑usage explanations, and update history.

## Getting started
1. Open the project using an Arduino/ESP32 development environment.
2. Set the PWM frequency, motor pins, and any configurable parameters in `include/config.h`.
3. Build and upload the firmware, then use the serial monitor to view basic system output.

## License
MIT

