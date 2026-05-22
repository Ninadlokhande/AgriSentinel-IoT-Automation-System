# System Architecture

The AgriSentinel IoT Automation System is built around the ESP32 DevKit V1 microcontroller and designed as a scalable embedded automation platform.

## Architecture Overview

The system consists of:

* ESP32 microcontroller
* 15 relay-driver channels
* Environmental sensing subsystem
* Blynk cloud communication
* Custom PCB routing and power distribution
* AC-DC isolated power module

---

# Core Functional Blocks

## 1. ESP32 Controller

The ESP32 acts as the central processing unit responsible for:

* WiFi communication
* Blynk cloud synchronization
* Sensor data acquisition
* Relay control
* GPIO management
* Real-time automation workflows

---

## 2. Relay Driver Section

Each relay channel includes:

* BC547 transistor driver
* Flyback protection diode
* LED status indicator
* Relay output terminal

The relay-driver stage isolates the ESP32 GPIO pins from direct relay current requirements.

---

## 3. Sensor Monitoring Section

Integrated sensors:

* DHT11 for temperature & humidity
* Soil moisture sensor
* Rain sensor

Sensor data is periodically sampled and transmitted to the Blynk dashboard.

---

## 4. Power Supply Section

The board uses the HLK-10M05 AC-DC converter module to generate regulated DC power for:

* ESP32
* Relay drivers
* Sensor modules

---

## 5. Cloud Connectivity

The ESP32 connects to the Blynk IoT platform through WiFi for:

* Remote relay control
* Real-time sensor monitoring
* Dashboard visualization
* Mobile app interaction

---

# Design Goals

* Modular relay expansion
* Stable embedded control
* Remote cloud monitoring
* Reliable relay switching
* Compact PCB implementation
* Scalable automation platform
