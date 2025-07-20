# Radar System – Arduino Ultrasonic Sensor with Java Swing Visualization

This project is a simple radar-style system that uses an **ultrasonic sensor** mounted on a **servo motor** to scan its surroundings. The distance data is read by an **Arduino Uno**, and then visualized in real-time using a **Java Swing GUI**.

Inspired purely by curiosity, this was an exploration into combining embedded hardware and desktop applications for interactive sensor-based systems.

---

## Components Used

| Component         | Quantity | Purpose                                      |
|------------------|----------|----------------------------------------------|
| Arduino Uno       | 1        | Main controller                              |
| Ultrasonic Sensor (HC-SR04) | 1        | Distance measurement                        |
| Servo Motor       | 1        | Rotates the sensor to scan area             |
| Breadboard        | 1        | Prototyping connection                       |
| Jumper Wires      | ~10      | Connecting components                        |
| USB Cable         | 1        | Arduino-to-PC communication                  |
| Java Swing GUI    | —        | Desktop application for radar visualization |

---

**Wiring Overview**:
- HC-SR04:
  - VCC → 5V
  - GND → GND
  - TRIG → Digital Pin 9
  - ECHO → Digital Pin 10
- Servo:
  - VCC → 5V
  - GND → GND
  - Signal → Digital Pin 11

---

## Working Principle

1. The servo motor sweeps from 0° to 180°, rotating the ultrasonic sensor.
2. At each step, the sensor measures distance and sends it to the Arduino.
3. Arduino sends angle-distance data to the PC via Serial.
4. A **Java Swing application** reads this serial data and plots a radar-like interface showing object positions in real-time.

---

## 🎥 Demo

▶️ [Watch the Radar System in Action](https://youtu.be/rQIPDKQyWzs?si=ofnNJGvp4sb-pkMX)


