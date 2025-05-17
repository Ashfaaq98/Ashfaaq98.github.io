+++
title = 'Autonomous Air Controller 🌡️🏠'
date = 2020-10-29T00:00:00+00:00
draft = false
summary = "An IoT-based system to autonomously control air conditioner settings by monitoring room occupancy, individual body temperatures, and overall room temperature, aiming for enhanced comfort and energy efficiency."
technologies = ["IoT", "Raspberry Pi", "Python", "OpenCV", "AWS DynamoDB", "Arduino", "Sensors (IR Temperature, DHT22)", "Machine Learning (Object Detection)", "IR Blasting"]
+++

## Project Overview

This project addresses the discomfort and energy inefficiency associated with manually controlled air conditioning systems. Traditional air conditioners often lead to suboptimal temperatures in shared spaces, as they don't account for individual comfort levels or room occupancy. The "Autonomous Air Cooling System" is an IoT solution designed to create a thermally comfortable environment by automating AC control based on real-time data.

The system aims to maintain a suitable temperature by monitoring individual body temperatures of occupants, counting the number of people in a room, and assessing the overall room temperature and humidity. It then uses a rule-based algorithm to adjust the air conditioner settings automatically, eliminating the need for manual intervention and potentially reducing electricity consumption by turning off the AC when the room is empty.

---

### 🧠 What It Does

- **Automates AC Control:** Eliminates manual AC adjustments by automatically controlling power and temperature settings based on environmental and occupant data.
- **Monitors Room Occupancy:** Uses a webcam with OpenCV to count the number of people entering and exiting the room. The system turns off the AC if the room is empty.
- **Measures Room Temperature & Humidity:** Employs a DHT22 sensor to continuously monitor the overall room temperature and humidity, storing this data in an AWS DynamoDB database. The `RoomTempDHT22.py` script handles reading from the DHT22 sensor and uploading data to DynamoDB.
- **Reads Individual Body Temperatures:** Utilizes an MLX90614 IR temperature sensor (interfaced with an Arduino Nano) to measure the body temperature of individuals entering the room, without physical contact. This data is also pushed to AWS DynamoDB. If a temperature above 38°C is detected, it triggers an alert.
- **Applies Rule-Based Algorithm:** A Python script on the Raspberry Pi processes data from all sensors (people count, room temperature, average body temperature) to determine the optimal AC settings. The `control_algo.py` script implements this logic, fetching data from DynamoDB and sending commands to the AC.
- **Controls AC via IR Signals:** Generates and transmits IR signals (power on/off, temperature increase/decrease) to the air conditioner using an IR emitter connected to the Raspberry Pi. The `control_algo.py` script contains predefined IR signal codes for various AC commands.

---

### 🔗 Explore the Project

- **GitHub Repository:** [Autonomous_Air_Controller](https://github.com/Ashfaaq98/Autonomous_Air_Controller)
