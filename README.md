# Home Intrusion Detection System

## Overview
This project implements a **Home Intrusion Detection System** using an **STM32 microcontroller**, **STM32CubeIDE**, and **NanoEdge AI** for AI-based anomaly detection. The system detects unusual activities, such as unauthorized entry, using sensor data and provides alerts accordingly.

## Features
- **Real-time intrusion detection** using AI-based anomaly detection
- **NanoEdge AI integration** for intelligent decision-making
- **Low-power STM32 microcontroller** for efficient operation
- **Scalable and customizable** for different security needs
- **Alerts via LED/Buzzer/Serial communication**

## Hardware Requirements
- **STM32 Microcontroller** (e.g., STM32L432KC or similar)
- **Sensors** (e.g., PIR Motion Sensor, Sound Sensor, Pressure Sensor, etc.)
- **Buzzer or LED** for alerts
- **USB-UART module** (for serial communication if needed)
- **Power supply (3.3V or 5V)**

## Software Requirements
- **STM32CubeIDE** (for firmware development and debugging)
- **NanoEdge AI Studio** (for AI model training and integration)
- **STM32CubeMX** (for configuring peripherals)
- **Python (optional)** for data preprocessing and testing

## System Architecture
1. **Sensor Data Acquisition:** The system reads data from motion, sound, or pressure sensors.
2. **AI Processing:** The data is processed using a trained AI model from **NanoEdge AI Studio**.
3. **Anomaly Detection:** The system detects unusual activities based on real-time sensor inputs.
4. **Alert Mechanism:** If an anomaly is detected, an alert (LED/Buzzer/UART message) is triggered.

## Installation and Setup
### 1. STM32CubeIDE Setup
1. Install **STM32CubeIDE** and **STM32CubeMX**.
2. Create a new STM32 project and configure peripherals (UART, GPIO, ADC, etc.).
3. Generate initialization code using STM32CubeMX.

### 2. NanoEdge AI Model Integration
1. Collect normal and abnormal sensor data.
2. Use **NanoEdge AI Studio** to train and generate an anomaly detection library.
3. Integrate the generated AI model into the STM32CubeIDE project.

### 3. Firmware Development
1. Implement **sensor data acquisition** using ADC or GPIO.
2. Feed data into the **NanoEdge AI model** for anomaly detection.
3. Define an **alert mechanism** (LED/Buzzer/UART).
4. Continuously monitor and adjust sensitivity as needed.

## Code Structure
```
/home-intrusion-detection
│-- Core/
│   ├── Src/         # Main source files
│   ├── Inc/         # Header files
│-- NanoEdge_AI/     # AI model integration
│-- Drivers/         # STM32 HAL drivers
│-- README.md        # Project documentation
│-- main.c           # Main firmware file
│-- stm32f4xx_it.c   # Interrupt handlers
```

## How to Run the System
1. **Flash the firmware** onto the STM32 microcontroller using STM32CubeIDE.
2. **Connect sensors** to the appropriate STM32 GPIO/ADC pins.
3. **Monitor the system** using UART (optional).
4. **Test by simulating an intrusion event** and verify the alert response.

## Future Improvements
- **Add wireless connectivity (LoRa, Wi-Fi, Bluetooth) for remote alerts.**
- **Enhance AI model with additional training data for better accuracy.**
- **Integrate with IoT platforms like AWS IoT or Firebase.**

