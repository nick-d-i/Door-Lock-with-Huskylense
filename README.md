# 🔐 Face Recognition Smart Lock with HuskyLens and Arduino

This project is a face recognition-based smart lock system using the [HuskyLens AI Camera](https://www.dfrobot.com/product-1922.html) and Arduino. It recognizes specific faces and unlocks a relay (e.g. door lock) only when authorized users are detected.

---

## 🖼️ Project Images

### 📷 Hardware Setup

<img src="images/IMG_20250529_183928.jpg" width="500" alt="Hardware setup 1">
<img src="images/IMG_20250529_183933.jpg" width="500" alt="Hardware setup 2">
<img src="images/IMG_20250529_183939.jpg" width="500" alt="Hardware setup 3">

---

## 🧰 Hardware Requirements

- Arduino Uno / Nano / Mega
- HuskyLens AI Camera
- Relay Module
- Jumper Wires
- 5V Power Supply
- Optional: Electric door lock or LED for testing

---

## 📷 HuskyLens Configuration

1. Switch to **Face Recognition** mode on HuskyLens.
2. Go to **General Settings > Protocol Type**, set to **I2C**.
3. Use the **learn button** to store authorized face IDs (e.g., ID 1, ID 2).

---

## ⚙️ Circuit Connections

| HuskyLens | Arduino |
|-----------|---------|
| VCC       | 5V      |
| GND       | GND     |
| SDA       | A4      |
| SCL       | A5      |

- **Relay IN** → Arduino **pin 3**

---

## 🧠 Features

- Recognizes multiple faces via I2C using HuskyLens
- Unlocks relay for authorized users
- Automatically re-locks when face disappears
- Built-in cooldown to prevent rapid toggling

---

## 🧾 Cod
