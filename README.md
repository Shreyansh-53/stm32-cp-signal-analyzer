# Control Pilot (CP) Signal Analyzer for EV Charging

An EVSE Control Pilot (CP) signal analyzer combining analog signal conditioning, LTspice simulation, and STM32G474 firmware for reliable PWM decoding and charging-state classification.

## Overview

This project implements a complete CP signal processing chain for AC EV charging systems. The analog front-end converts the ±12 V CP waveform into an isolated, logic-level PWM signal suitable for a microcontroller. The conditioned signal is then decoded by an STM32G474 to determine the charging state and available current according to the EVSE PWM duty cycle.

## Features

- Isolated CP signal conditioning using a PC817 optocoupler
- Schmitt-trigger-based waveform shaping
- Integrator-based triangle-wave generation and PWM conversion
- LTspice validation of the analog front-end
- Duty-cycle and frequency measurement using STM32G474 Timer Input Capture
- Hysteresis-based state machine for charging-state and current-limit detection

## Hardware & Tools

- STM32G474
- LTspice
- PC817 Optocoupler
- Analog comparators and passive components

## Project Structure

```text
hardware/    LTspice schematics and analog front-end design files
firmware/    STM32G474 source code
docs/        Documentation, figures, and notes
```

## Future Work

- PCB implementation of the analog front-end
- Enhanced filtering and noise immunity
- Support for additional CP fault and diagnostic states
