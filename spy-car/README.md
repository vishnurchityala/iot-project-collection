# Spy Car – ESP32-CAM + Arduino Uno + Bluetooth Controlled Robot

This project is a wireless spy car that streams real-time video using an ESP32-CAM and is controlled remotely via Bluetooth using an Arduino Uno and HC-05 module. The motors are driven using a motor driver, making it a complete mobile surveillance bot.

Built out of curiosity to explore wireless video streaming and remote robot control using both ESP32 and Arduino in tandem.

---

## Components Used

| Component              | Quantity | Purpose                                    |
|------------------------|----------|--------------------------------------------|
| ESP32-CAM              | 1        | Live video streaming via Wi-Fi             |
| Arduino Uno            | 1        | Handles Bluetooth and motor control        |
| HC-05 Bluetooth Module | 1        | Wireless control from smartphone           |
| L298N Motor Driver     | 1        | Drives the motors                          |
| DC Motors              | 2 or 4   | Robot movement                             |
| Chassis + Wheels       | 1 set    | Robot structure                            |
| 18650 / 9V Battery     | 1        | Power source                               |
| Jumper Wires           | —        | Wiring                                     |
| Bluetooth App          | 1        | Mobile control interface                   |

---

## Wiring Overview

**ESP32-CAM:**
- Runs independently; powered via 5V from battery or separate regulator
- Connects via browser (IP shown in serial monitor)

**HC-05 to Arduino Uno:**
- TX → RX (D0) *(use voltage divider)*
- RX → TX (D1)
- VCC → 5V  
- GND → GND

**L298N Motor Driver:**
- IN1–IN4 → Digital pins (e.g., D5–D8)
- ENA/ENB → Jumper or PWM pins
- VCC → Battery
- GND → Shared ground with Arduino and ESP32

---

## Working Principle

1. ESP32-CAM starts a local web server for real-time video streaming over Wi-Fi. You access it via the IP shown in the Serial Monitor.
2. HC-05 Bluetooth module receives directional commands from a mobile app.
3. Arduino Uno interprets these commands and drives the motors using the L298N motor driver.
4. Together, the car streams video and responds to remote directional input, making it a functional mobile spy bot.

---

## Controlling the Car

- Use any Bluetooth Controller App (e.g., Arduino Bluetooth Controller)
- Common key mappings:
  - `F` → Forward
  - `B` → Backward
  - `L` → Left
  - `R` → Right
  - `S` → Stop

---

## Demo

[Watch the Spy Car in Action](https://youtu.be/8Z6hDPG3GxI?si=jHitm7Pxs45Ynco3)

---

## Notes

- ESP32-CAM may reset or fail if powered from Arduino Uno; use a dedicated 5V supply if needed.
- Ensure your Wi-Fi is connected and the ESP32 is properly configured before accessing the video stream.
- Add delays or speed controls for smoother motor transitions.
