# Bluetooth Car

This project is a simple Bluetooth-controlled car using an **Arduino Uno**, **HC-05 Bluetooth module**, and an **L298N motor driver**. The car is remotely controlled via a smartphone using a Bluetooth controller app.

Inspired purely by curiosity, this was an exploration into wireless communication and basic robotics using Arduino.

---

## Components Used

| Component             | Quantity | Purpose                                  |
|----------------------|----------|------------------------------------------|
| Arduino Uno           | 1        | Main controller                          |
| HC-05 Bluetooth Module| 1        | Wireless communication                   |
| L298N Motor Driver    | 1        | Controls direction and speed of motors   |
| DC Motors             | 2 or 4   | Drive the car                            |
| Wheels                | 2 or 4   | Movement                                 |
| Chassis               | 1        | Base structure                           |
| 9V / 18650 Battery    | 1        | Power supply                             |
| Jumper Wires          | —        | Wiring                                   |
| Bluetooth Controller App | 1    | Sends commands via smartphone            |

---

**Wiring Overview**:
- HC-05:
  - VCC → 5V
  - GND → GND
  - TX → Arduino RX (D0)
  - RX → Arduino TX (D1) *(use voltage divider if needed)*
- L298N:
  - IN1 → D8
  - IN2 → D9
  - IN3 → D10
  - IN4 → D11
  - ENA / ENB → Jumpered or connected to PWM pins
  - VCC → Battery
  - GND → Common ground with Arduino

---

## Working Principle

1. The HC-05 Bluetooth module receives directional commands from a mobile app.
2. Arduino reads those commands over Serial.
3. Based on input (e.g., `F` for forward, `B` for backward), Arduino drives motors using the L298N motor driver.
4. The car responds in real-time to controls sent over Bluetooth.

---

## 🎥 Demo

▶️ [Watch the Bluetooth Car in Action](https://youtu.be/p2hJVAeONRU?si=LmfO1ywOYvmCgf3Z)

---
