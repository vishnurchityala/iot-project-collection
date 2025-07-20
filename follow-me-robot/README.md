# Follow Me Robot – Arduino + IR & Rotating Ultrasonic Sensor + 4 Motor Drivers

This project is a "Follow Me" robot built using an **Arduino Uno**, **IR sensors**, a **servo-mounted ultrasonic sensor**, and **four motor driver boards**. The robot detects and follows an object while scanning for obstacles in multiple directions and adjusting its path accordingly.

Built purely out of curiosity, this robot combines motion, distance sensing, and dynamic reaction using simple components.

---

## Components Used

| Component                    | Quantity | Purpose                                          |
|-----------------------------|----------|--------------------------------------------------|
| Arduino Uno                 | 1        | Main controller                                  |
| Ultrasonic Sensor (HC-SR04) | 1        | Distance measurement                             |
| Servo Motor                 | 1        | Rotates the ultrasonic sensor for wide scanning  |
| IR Sensors                  | 2–3      | Detect object direction                          |
| L298N Motor Driver Boards   | 4        | Independent control of each motor                |
| DC Motors                   | 4        | Drives the robot                                 |
| Robot Chassis + Wheels      | 1 set    | Structural base and movement                     |
| 18650 or 9V Battery         | 1        | Power supply                                     |
| Jumper Wires                | —        | Component connections                            |
| Breadboard (optional)       | 1        | For easy sensor connections                      |

---

## 🔌 Wiring Overview

- **IR Sensors** → Digital Pins (e.g., D2, D3, D4)
- **Ultrasonic Sensor:**
  - VCC → 5V  
  - GND → GND  
  - TRIG → D9  
  - ECHO → D10
- **Servo Motor (for ultrasonic scan):**
  - Signal → D11  
  - VCC → 5V  
  - GND → GND
- **L298N Motor Drivers (x4):**
  - Control 1 motor each
  - IN1–IN4 → Use available digital pins (e.g., D5–D8, D12, D13)
  - ENA/ENB → PWM pins (or jumpered for full speed)
  - VCC → Battery  
  - GND → Shared ground with Arduino

---

## ⚙️ Working Principle

1. **IR sensors** detect nearby objects or directional signals (like hand movement or reflective tape).
2. A **servo-mounted ultrasonic sensor** rotates to scan surroundings and detect obstacles in multiple directions.
3. The robot uses this sensor data to:
   - Move forward when an object is detected ahead
   - Turn left/right based on IR or sonar input
   - Stop or reverse if obstacles are too close
4. The use of **four motor drivers** gives precise control over each wheel, improving navigation and turning.

---

## 🎥 Demo

▶️ [Watch the Follow Me Robot in Action](https://youtube.com/shorts/im1lc8FQVyM?si=ALLG9lYC44BAbErU)

---
