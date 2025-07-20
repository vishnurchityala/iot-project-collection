# Smart Dustbin – Arduino Nano + Ultrasonic Sensor + Servo Motor

This project is an automatic smart dustbin that opens its lid when it detects an object (like a hand) nearby using an ultrasonic sensor. The lid is controlled by a servo motor, and the entire system is powered by an Arduino Nano.

Built purely out of curiosity to explore automation using simple sensors and actuators.

---

## Components Used

| Component                    | Quantity | Purpose                                |
|-----------------------------|----------|----------------------------------------|
| Arduino Nano                | 1        | Main controller                        |
| Ultrasonic Sensor (HC-SR04) | 1        | Detects object near the lid            |
| Servo Motor                 | 1        | Opens and closes the dustbin lid       |
| Jumper Wires                | —        | Component connections                  |
| Breadboard (optional)       | 1        | For prototyping                        |
| Power Source (Battery/USB)  | 1        | Powers the Arduino and servo           |
| Dustbin with Hinged Lid     | 1        | Container to automate                  |

---

## Wiring Overview

**Ultrasonic Sensor (HC-SR04):**
- VCC → 5V  
- GND → GND  
- TRIG → Digital Pin 9  
- ECHO → Digital Pin 10  

**Servo Motor:**
- VCC → 5V  
- GND → GND  
- Signal → Digital Pin 11  

Make sure the servo and Arduino share a common ground.

---

## Working Principle

1. The ultrasonic sensor continuously checks for nearby objects.
2. When it detects an object within a certain range (e.g., < 20 cm), it signals the Arduino.
3. Arduino commands the servo to rotate and open the lid.
4. After a short delay, the servo returns to its original position to close the lid.

---

## Demo

[Watch the Smart Dustbin in Action](https://drive.google.com/drive/folders/1J710GbaUW6R9Qe_sFJB79kDiXvptxKxW)

---

## Notes

- You can adjust the detection distance in the Arduino code.
- Use a strong enough power source if the servo motor is not rotating fully.
- The project can be extended with IR sensors, delay control, or even an automatic sanitization system.

