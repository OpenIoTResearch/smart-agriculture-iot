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

## ⚙️ Setup & Usage

Follow these steps to set up and run the project on your hardware:

### 1. Clone the Repository
Run the following commands in your terminal:

```bash
    git clone https://github.com/OpenIoTResearch/smart-agriculture-iot.git 
```

cd smart-agriculture-iot

### 2. Install Arduino IDE / PlatformIO
   - Download and install [Arduino IDE](https://www.arduino.cc/en/software) or [PlatformIO](https://platformio.org/).
   - Add support for ESP32 boards via the Arduino Board Manager (if using ESP32).

### 3. Connect the Hardware
    - ESP32 or Arduino Uno board
    - Soil moisture sensor → connect to A0
    - DHT11 sensor → connect to Digital pin 2
    - Light sensor (LDR) → connect to A1
    - Battery or USB power supply

### 4. Upload the Code
    1. Open the project in Arduino IDE or VS Code (PlatformIO).
    2. Select the correct board (ESP32/Arduino) and COM port.
    3. Compile and upload the sketch to your board.

### 5. Open Serial Monitor
    - After uploading, open the Serial Monitor (`Ctrl + Shift + M` in Arduino IDE).
    - You should see real-time data for:
        - Soil moisture 🌱
        - emperature & humidity 🌡️
        - Light levels ☀️

### 6. Deploy & Use
    - Place the sensors in the soil and environment.
    - Monitor the data via Serial Monitor, IoT dashboard, or mobile/web interface (if configured).
    - Use the collected data to decide on irrigation, crop monitoring, and other farming actions.


## 📜 License

This project is licensed under the **MIT License**.  
You are free to use, modify, and distribute this project for personal or commercial purposes, provided that proper credit is given.  

See the [LICENSE](./LICENSE) file for full details.

