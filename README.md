# Mouse Project – PWM Code

This repository contains the firmware used to control the wire‑guided Mouse Project vehicle.

## What it does
- Reads the 20 kHz track signal via pickup coils and basic filtering
- Computes lateral error and applies closed‑loop steering
- Drives twin DC motors using PWM (MOSFET driver)
- Limits speed in corners when sensor tracking degrades at higher velocity

## Structure
- `src/` – main control loop and PWM drivers
- `include/` – headers and configuration
- `docs/` – notes on tuning, energy usage, and release history

## Getting started
1. Open the project in Arduino/ESP32 environment.
2. Set PWM frequency and pins in `include/config.h`.
3. Build and flash; use the serial monitor for basic telemetry.

## Limitations
At higher speeds, the pickup coil readings become less stable, which can cause the mouse to drift or jitter when approaching corners. 
For reliable tracking, the control code automatically reduces motor speed when sensor accuracy decreases. 
Further tuning of the coil sensitivity and signal filtering may improve high‑speed performance in future revisions.

## License
MIT
