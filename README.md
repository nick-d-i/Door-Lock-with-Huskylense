# 🔐 Face Recognition Smart Lock with HuskyLens and Arduino

This project is a face recognition-based smart lock system using the [HuskyLens AI Camera](https://www.dfrobot.com/product-1922.html) and Arduino. It recognizes specific faces and unlocks a relay (e.g. door lock) only when authorized users are detected.

---

## 🖼️ Project Images

### 📷 Hardware Setup

![IMG_20250529_183939](https://github.com/user-attachments/assets/64b04b08-6b05-4aa6-bd30-f98015453d13)
![IMG_20250529_183933](https://github.com/user-attachments/assets/b3b27a76-6ace-486f-b10d-32975b485d96)
![IMG_20250529_183928](https://github.com/user-attachments/assets/7839d31a-99d2-4bb4-8633-12f262e1744f)



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
