+++
title = "Line Following Robot 🤖➡️"
date = 2019-05-12T00:00:00+01:00
draft = false
summary = "An Arduino-based robot programmed in assembly to autonomously follow a black line path."
technologies = ["AVR Assembly", "Arduino", "Interrupts", "Timers", "Sensor Control"]
+++



## Project Overview

This was one of my earliest robotics projects — a **line-following robot** built using an **Arduino board** and programmed entirely in **AVR assembly language**.

The robot was designed to detect and follow a black line on a white surface using **infrared sensors**, and adjust the motor speeds accordingly to navigate curves and intersections.



---

### 🧠 What It Does

- Detects the position of a line using sensors on the underside.
- Uses **Timer0 and Timer2** interrupts for precise motor control.
- Dynamically adjusts PWM values for both motors to steer left, right, or forward.
- Implements simple logic to keep the robot centered on the path.

---

### 🧰 Technical Highlights

- **Microcontroller:** Atmega328P (Arduino Uno)
- **Language:** Pure AVR Assembly
- **Timers Used:** Timer0 and Timer2 (Compare Match interrupts)
- **Pins Controlled:** Ports B and D
- **Key Features:**
  - Real-time response using hardware interrupts.
  - Independent motor speed adjustment based on sensor feedback.
  - Low-level memory and register operations for tight control.

---
