# Door-Lock-with-Huskylense# 🔐 Face Recognition Smart Lock with HuskyLens and Arduino

This project uses the [HuskyLens AI Camera](https://www.dfrobot.com/product-1922.html) and an Arduino to create a smart lock that unlocks only when it detects an authorized face.

## 📸 Overview

Using face recognition powered by the HuskyLens, this system:
- Unlocks a relay (door/electronic lock) when a known face is detected.
- Automatically locks when the face disappears.
- Implements a cooldown to prevent rapid toggling.

## 🧰 Hardware Requirements

- Arduino Uno / Mega / Nano
- [HuskyLens AI Camera](https://www.dfrobot.com/product-1922.html)
- Relay module (5V)
- Jumper wires
- External power (if controlling a real lock)

## 🧠 Features

- Face recognition using HuskyLens
- I2C communication with Arduino
- Configurable relay control
- Cooldown logic (default: 5 seconds)
- Serial debugging info

## 📷 Setup Instructions

### 1. Configure HuskyLens
- Set to **Face Recognition** mode
- Connect via **I2C** (Settings > Protocol Type > I2C)
- Learn authorized faces (use "Learn" button on device)

### 2. Wiring Diagram

| HuskyLens | Arduino |
|-----------|---------|
| SDA       | A4      |
| SCL       | A5      |
| VCC       | 5V      |
| GND       | GND     |

Relay IN pin goes to **pin 3** on Arduino.

### 3. Arduino Code

Upload the included `face_lock.ino` file to your Arduino.

### 4. Adjust IDs

The code recognizes faces with ID `1` or `2` as authorized:
```cpp
if (result.ID == 1 || result.ID == 2)
