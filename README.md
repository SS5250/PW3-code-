# Mouse Project – PWM Code

This repository contains the firmware used to control the wire‑guided Mouse Project vehicle.

## What it does
- Detects the 20 kHz track signal using pickup coils and basic filtering
- Calculates how far the mouse is from the centre of the wire and adjusts steering automatically
- Controls two DC motors using PWM through a MOSFET motor driver
- Limits speed in corners when sensors become less reliable at higher speeds, preventing drift and jitter

## Structure
- `src/` – Main firmware, including the control loop, sensor processing, and PWM motor output.
- `include/` – Header and configuration files, such as pin assignments and control parameters.
- `docs/` – Additional project information, including tuning notes, energy‑usage explanations, and update history.

## Getting started
1. Open the project in Arduino/ESP32 environment.
2. Set PWM frequency and pins in `include/config.h`.
3. Build and flash; use the serial monitor for basic telemetry.

## Limitations
At higher speeds, the pickup coil readings become less stable, which can cause the mouse to drift or jitter when approaching corners. 
For reliable tracking, the control code automatically reduces motor speed when sensor accuracy decreases. 
Further tuning of the coil sensitivity and signal filtering may improve high‑speed performance in future revisions.
1. Open the project in the Arduino or ESP32 development environment.
2. Set PWM frequency, motor pins, and other configurable parameters in `include/config.h`.
3. Build and upload the firmware to your board.
4. Use the serial monitor to view basic output for tuning and debugging.

## License
MIT
