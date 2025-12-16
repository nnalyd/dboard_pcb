# 60% Hall Effect Keyboard PCB (STM32G473)

![Status](https://img.shields.io/badge/Status-Finished-brightgreen)
![License](https://img.shields.io/badge/License-GPLv3-blue)

**DBOARD** is an open-hardware 60% keyboard PCB designed for **Hall Effect (HE) switches**.

## Features

* **Form Factor:** Standard 60%
* **MCU:** STMicroelectronics **STM32G473**
* **Architecture:**
    * **16:1 Analog Multiplexers**
    * Full analog matrix scanning for precise travel distance measurement (0.1mm - 4.0mm).

## Hardware Specifications

| Component | Part | Purpose |
| :--- | :--- | :--- |
| **Microcontroller** | STM32G473CBT6 | Handles ADC, DMA & USB |
| **Multiplexers** | 74HC4067 | Multiplexing 60+ analog signals to limited ADC pins |
| **HE Sensors** | SLSS49E-3 | Linear Hall Effect sensors for switch reading |
| **Regulator** | AMS1117-3.3 | 3.3V Logic & Sensor Power |

## Pinout & Matrix

The board utilizes a multiplexed analog matrix. The STM32 drives the Mux Select lines to cycle through rows/columns and reads the resulting voltage on the ADC lines.

* **Mux Select Pins:** `[PA9]`, `[PA8]`, `[PB14]`, `[PB15]`
* **ADC Input Pins:** `[ADC12_IN1]`, `[ADC12_IN2]`, `[ADC3_IN5]`, `[ADC4_IN3]`

## Repository Structure

* `/hardware`: KiCad project files (Schematics, PCB layout).
* `/production`: Production-ready files for manufacturing.

## License

This project is licensed under the **GNU General Public License v3.0**
