# AgriSentinel IoT Automation System

An ESP32-based multi-channel IoT automation and monitoring platform designed for real-time device control, environmental sensing, and cloud-connected automation workflows.

This project integrates:

* 15-channel relay control
* ESP32 WiFi communication
* Blynk IoT dashboard
* Soil moisture monitoring
* Rain sensing
* Temperature & humidity sensing
* Custom PCB design
* Embedded firmware development

The system was designed as a scalable embedded automation platform capable of remotely controlling and monitoring multiple electrical and sensor-based devices through cloud connectivity.

---

# Features

* ESP32-based IoT controller
* 15 independently controlled relay channels
* Real-time Blynk cloud dashboard integration
* Soil moisture monitoring
* Rain detection system
* Temperature & humidity monitoring using DHT11
* Custom-designed PCB and schematic
* Relay-driver protection using flyback diodes
* LED status indicators for relay outputs
* WiFi-enabled remote monitoring and automation
* Modular screw-terminal device connections
* Scalable embedded architecture for automation systems

---

# Hardware Components

## Microcontroller

* ESP32 DevKit V1

## Sensors

* DHT11 Temperature & Humidity Sensor
* Soil Moisture Sensor
* Rain Sensor

## Power & Relay Circuit

* 15 Relay Channels
* BC547 Relay Driver Circuits
* Flyback Protection Diodes
* HLK-10M05 AC-DC Power Module
* LED Status Indicators

## PCB Design

* Custom KiCad schematic
* Custom PCB routing
* Modular screw-terminal outputs

---

# Software & Firmware

## Technologies Used

* Embedded C++
* Arduino Framework
* ESP32 WiFi
* Blynk IoT Platform

## Functionalities

* Real-time relay control
* Cloud-connected automation
* Sensor telemetry monitoring
* WiFi communication
* Blynk dashboard synchronization
* Timed sensor updates

---

# System Architecture

The ESP32 communicates with the Blynk cloud platform through WiFi while simultaneously monitoring connected sensors and controlling relay-driver circuits through mapped GPIO pins.

Sensor data including:

* Temperature
* Humidity
* Soil moisture
* Rain detection

is continuously transmitted to the Blynk dashboard for remote monitoring.

---

# PCB Design

This project includes a fully custom-designed PCB featuring:

* ESP32 GPIO breakout routing
* 15 relay-driver channels
* Power-distribution section
* Sensor interfacing headers
* Flyback diode protection
* Modular terminal connections

# Future Improvements

* MQTT integration
* Mobile notification alerts
* OTA firmware updates
* Smart scheduling system
* Energy monitoring
* Sensor calibration system
* Local web dashboard

---

# Author

Ninad Lokhande

GitHub:
https://github.com/Ninadlokhande/AgriSentinel-IoT-Automation-System
