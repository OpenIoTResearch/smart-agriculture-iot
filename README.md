# Affordable IoT-Based Smart Agriculture System for Small-Scale Farmers

## Project purpose
To design and implement an affordable, low-power IoT system that enables farmers to monitor soil and environmental conditions in real-time, and receive actionable insights on crop irrigation and management.

## Features
1. Soil Monitoring
    - Real-time soil moisture tracking
    - Alerts when soil is too dry or over-watered
2. Climate Monitoring
    - Temperature and humidity tracking using DHT11
    - Light intensity monitoring for crop growth conditions
3. Smart Irrigation Control
    - Automatic pump/valve activation when soil moisture is low
    - Manual override via mobile/web app
4. IoT Connectivity
    - ESP32/Arduino sends sensor data to the cloud (MQTT, Firebase, or ThingsBoard)
    - Farmers can view data on a mobile or web dashboard
5. Data Logging & Visualization
    - Store historical data for analysis (growth patterns, weather trends)
    - Simple graphs for farmers to understand
6. Battery-Powered & Affordable
    - Powered by rechargeable battery (with solar charging option in the future)
    - Low-cost, scalable solution for small-scale farmers
7. Open Source & Expandable
    - Open for contributions (e.g., adding fertilizer sensors, AI predictions)
    - Designed to integrate more sensors as needed

## Hardware & software requirements
### 🛠 Hardware Requirements

| Component                          | Purpose                                                                 |
|-----------------------------------|-------------------------------------------------------------------------|
| **ESP32 (or Arduino Uno)**        | Main microcontroller for reading sensors and sending data via WiFi/Bluetooth |
| **Soil Moisture Sensor**          | Detects soil water content                                               |
| **DHT11 Sensor**                  | Measures temperature & humidity                                          |
| **Light Sensor (LDR or BH1750)**  | Monitors sunlight intensity                                              |
| **Water Pump + Relay Module (opt.)** | Automates irrigation based on soil moisture                          |
| **Battery Pack (Li-ion / Li-Po)** | Powers the system in remote farms                                        |
| **(Optional) Solar Panel**        | Sustainable power source for long-term deployment                        |
| **Jumper Wires, Breadboard, PCB** | Prototyping and circuit connections                                      |

---

### 💻 Software Requirements

**Programming Environment**
- [Arduino IDE](https://www.arduino.cc/en/software) / [PlatformIO](https://platformio.org/) → for programming ESP32/Arduino

**Libraries Needed**
- `DHT.h` → for DHT11 sensor  
- `WiFi.h` / `WiFiClient.h` → for ESP32 WiFi connectivity  
- `Adafruit_Sensor.h` → sensor abstraction  
- `PubSubClient.h` → for MQTT communication (if using MQTT broker)  
- `ThingSpeak.h` / `FirebaseESP32.h` (optional cloud libraries)  

**Backend Options (Cloud Storage / IoT Dashboard)**
- [ThingSpeak](https://thingspeak.com/) → free, simple graphs  
- [Firebase](https://firebase.google.com/) → real-time database + mobile app integration  
- [ThingsBoard](https://thingsboard.io/) → open-source IoT dashboard  

**Frontend Options (Farmer Dashboard)**
- Simple mobile/web app built with React, Flutter, or plain HTML dashboard  
- SMS/WhatsApp alerts for low-connectivity areas  

## 🤝 How to Contribute

We welcome contributions from developers, researchers, and IoT enthusiasts!  
Here are some ways you can get involved:

1. **Fork the Repository**  
   - Fork this project to your GitHub account.  
   - Clone your fork locally to start experimenting.  

2. **Pick an Issue or Suggest a Feature**  
   - Check the [Issues](../../issues) tab for tasks, bugs, or feature requests.  
   - Propose new ideas by opening an issue.  

3. **Make Your Changes**  
   - Create a new branch (`git checkout -b feature-new-sensor`).  
   - Write clean, well-documented code.  
   - Add/update documentation if needed (README, diagrams, comments).  

4. **Test Before Submitting**  
   - Test your code on real hardware (ESP32/Arduino + sensors).  
   - Ensure it does not break existing features.  

5. **Submit a Pull Request (PR)**  
   - Push your branch and open a PR against the `main` branch.  
   - Clearly describe what you changed and why.  

### Contribution Ideas
- Add support for new sensors (fertilizer, pH, CO₂, etc.)  
- Improve the mobile/web dashboard for farmers  
- Optimize battery consumption for longer field deployments  
- Localize documentation for non-English-speaking farmers  
- Write blog posts, tutorials, or YouTube demos to help others use this project  

### Code of Conduct
This project follows the [Contributor Covenant](https://www.contributor-covenant.org/).  
Please be respectful, inclusive, and supportive when interacting with the community.  

## 📜 License

This project is licensed under the **MIT License**.  
You are free to use, modify, and distribute this project for personal or commercial purposes, provided that proper credit is given.  

See the [LICENSE](./LICENSE) file for full details.

