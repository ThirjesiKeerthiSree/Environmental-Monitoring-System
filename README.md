# IIoT-Based Environmental Monitoring System

An Industrial Internet of Things (IIoT) based environmental monitoring system that measures **temperature, humidity, and gas concentration** and transmits real-time telemetry to a **cloud monitoring dashboard** using the **MQTT communication protocol**.

The system is built using an **ESP32 microcontroller** and demonstrates a scalable architecture for **industrial safety monitoring and agricultural environmental supervision**.

---

## Overview

Continuous monitoring of environmental parameters is essential in industrial and agricultural environments to ensure operational safety and maintain optimal conditions.

This project implements a **low-cost IoT telemetry system** capable of sensing environmental variables, transmitting data to the cloud, and generating automated alerts when unsafe conditions are detected.

---

## Key Features

- Real-time monitoring of **temperature, humidity, and gas concentration**
- **ESP32-based edge processing**
- **MQTT communication** for efficient telemetry transmission
- Cloud-based **data visualization dashboard**
- **Automated safety alerts** for abnormal environmental conditions
- Scalable architecture suitable for industrial and agricultural applications

---

## System Architecture

The system architecture consists of three primary layers:

### 1. Sensing Layer
Environmental parameters are measured using sensors connected to the microcontroller.

- **DHT22 Sensor** – Measures temperature and humidity
- **Gas Sensor Interface (MQ-2 simulated)** – Detects gas concentration levels

### 2. Edge Processing Layer
The **ESP32 microcontroller** performs local data processing, including:

- Sensor data acquisition
- Analog-to-digital conversion
- Signal scaling and mapping
- Preparation of telemetry packets

### 3. Communication Layer
Processed telemetry data is transmitted to the cloud via:

- **Wi-Fi connectivity**
- **MQTT messaging protocol**

---

## Hardware Components

| Component | Description |
|-----------|-------------|
| ESP32 DevKit V1 | Microcontroller with integrated Wi-Fi |
| DHT22 Sensor | Temperature and humidity sensing |
| MQ-2 Gas Sensor | Gas concentration detection |
| Potentiometer | Used for gas sensor simulation |
| Power Supply | 5V adapter or battery |
| Enclosure | Protective housing for field deployment |

---

## Software and Tools

- **Arduino IDE** – Firmware development
- **Wokwi Simulation Platform** – Hardware simulation and testing
- **Adafruit IO** – Cloud platform for telemetry visualization
- **MQTT Protocol** – Lightweight data communication

---

## Data Flow

### Data Acquisition
Environmental data is collected from the DHT22 sensor and gas sensor interface.

### Edge Processing
The ESP32 processes raw signals using:

- 12-bit ADC conversion (0–4095)
- Sensor value scaling
- Conversion of analog signals into readable telemetry data

### Data Transmission
Sensor readings are published to the cloud **every 10 seconds** using MQTT.

### Cloud Visualization
The Adafruit IO dashboard provides:

- Real-time gauges
- Historical trend charts
- Visual alert indicators

---

## Safety Logic and Alerts

The system includes automated safety monitoring with predefined thresholds.

**Alert Conditions**

- Temperature > **450°C**
- Gas concentration > **200 PPM**

When triggered:

- An automated **email notification** is generated
- Dashboard indicators display warning status
- **Hysteresis delay** prevents repeated alert notifications

---

## Simulation Environment

The system was designed and validated using the **Wokwi simulation platform**, allowing testing of sensor integration, data processing, and MQTT communication without physical hardware.

Simulation Link:  
https://wokwi.com/projects/456594262811280385

---

## Cloud Dashboard

Real-time monitoring dashboard hosted on **Adafruit IO**:

https://io.adafruit.com/thirjesi_keerthi_sree/dashboards/agriculture-monitoring-system

---

## Bill of Materials

| Component | Estimated Cost (INR) |
|-----------|----------------------|
| ESP32 DevKit V1 | 600 |
| DHT22 Sensor | 350 |
| MQ-2 Gas Sensor | 250 |
| IP65 Enclosure | 800 |
| Power Adapter | 300 |
| Wiring and PCB | 200 |

**Estimated Total Cost: ₹2500**

---

## Applications

- Industrial environmental monitoring
- Agricultural climate monitoring
- Warehouse safety monitoring
- Smart farming systems
- Remote telemetry systems

---

## Future Enhancements

- Integration with **LoRa or NB-IoT for long-range communication**
- Multi-node distributed sensor networks
- Mobile application interface
- Data analytics for predictive monitoring
- Integration with industrial monitoring systems

---

## Author

**Thirjesi Keerthi Sree**  
Electronics Engineering Student  

Project focused on **Embedded Systems, IoT Telemetry, and Industrial Monitoring Applications**.

---
