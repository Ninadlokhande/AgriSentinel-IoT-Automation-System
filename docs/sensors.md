# Sensor Integration

## DHT11 Temperature & Humidity Sensor

### Purpose

Used for environmental monitoring.

### Parameters Measured

* Temperature
* Humidity

### ESP32 GPIO

GPIO 2

---

## Soil Moisture Sensor

### Purpose

Measures soil moisture levels for smart irrigation and agricultural monitoring applications.

### ESP32 GPIO

GPIO 34

### Output

Analog signal converted to percentage values inside firmware.

---

## Rain Sensor

### Purpose

Detects rainfall intensity and water presence.

### ESP32 GPIO

GPIO 35

### Output

Analog signal converted into rain percentage values.

---

# Sensor Data Processing

The firmware:

* reads analog sensor values
* converts raw ADC readings into percentages
* transmits processed telemetry data to Blynk virtual pins
* updates dashboard values every 2 seconds

---

# Sensor Update Workflow

1. ESP32 reads sensor values
2. Firmware processes raw ADC values
3. Data converted to readable percentages
4. Values transmitted to Blynk dashboard
5. Dashboard updated in real-time
