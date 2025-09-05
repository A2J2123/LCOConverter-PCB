# LCOConverter-PCB

## Overview

**LCOConverter-PCB** is a compact breakout board designed to convert a +5V power supply to a regulated +3.3V output. This is achieved using a MIC5317-3.3YM5-TR low-dropout (LDO) voltage regulator. The board features standard SM02B-GHS-TB(LF)(SN) connectors for easy integration into your projects and includes all necessary supporting components for stable operation.

---

## Features

- **Input Voltage:** +5V DC
- **Output Voltage:** +3.3V DC (regulated)
- **LDO Regulator:** MIC5317-3.3YM5-TR
- **Connectors:** SM02B-GHS-TB(LF)(SN) headers for input and output
- **Capacitors:** 1uF ceramic capacitors at input/output for noise filtering
- **Compact PCB Design:** Small footprint for easy integration

---

## Schematic

![Schematic](Images/LCOConverter%20Schematic.png)

*Image 3: Schematic Diagram*

- **J1:** +5V input (+5V on pin 1, GND on pin 2)
- **J2:** +3.3V output (+3.3V on pin 1, GND on pin 2)
- **U1:** MIC5317-3.3YM5-TR LDO regulator
- **C1, C2:** 1uF ceramic capacitors

---

## PCB Layout

### Top View

![PCB Top View](Images/LCOConverter%20PCB%202D.png)

*Image 1: Top view of the PCB layout.*

### 3D Render

![3D PCB](Images/LCOConverter%20PCB%203D.png)

*Image 2: 3D render of the assembled PCB.*

---

## How It Works

1. **Power Input:** Apply +5V and GND to connector J1.
2. **Voltage Regulation:** The MIC5317 LDO regulator (U1) drops the input voltage down to +3.3V.
3. **Output:** The regulated +3.3V and GND are available at connector J2.
4. **Decoupling:** C1 and C2 (1uF each) stabilize the voltage and reduce noise on both input and output sides.

---

## Bill of Materials

| Reference | Value      | Description                 | Package         |
|-----------|------------|-----------------------------|-----------------|
| U1        | MIC5317-3.3YM5-TR | LDO Regulator (+5V to +3.3V) | SOT-23-5        |
| J1, J2    | SM02B-GHS-TB(LF)(SN) | 2-pin JST GH connectors       | JST GH (2 pin)  |
| C1, C2    | 1uF        | Ceramic Capacitor           | 0603/0805       |

---

## Usage Instructions

1. Solder all components as per the schematic.
2. Connect +5V DC to J1 (pin 1) and ground to J1 (pin 2).
3. Retrieve +3.3V from J2 (pin 1) and ground from J2 (pin 2).
4. Ensure input voltage does **not exceed** the maximum rating of the regulator.

---

## Applications

- Level shifting for microcontrollers and sensors
- Powering 3.3V logic devices from a 5V rail
- Embedded and IoT projects needing a compact, reliable 3.3V supply

---

## License

This project is open-source under the [MIT License](LICENSE).
