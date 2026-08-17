# Automated Plant Watering System 🌿💧

## Overview
This project is a smart, automated watering system designed to monitor soil moisture levels and automatically trigger a water pump when the plant needs water. It ensures plants receive the optimal amount of hydration without manual intervention.

## Features
*   **Real-time Monitoring:** Continuously reads soil moisture data.
*   **Automated Watering:** Activates a 5V/12V water pump via a relay module when moisture drops below a defined threshold.
*   **Wireless Connectivity (Optional):** Connects to Wi-Fi to log data or provide remote status updates.
*   **Resource Efficient:** Utilizes deep sleep or task scheduling to minimize power consumption.

## Hardware Components
*   ESP32 or Arduino Uno microcontroller
*   Capacitive Soil Moisture Sensor (v1.2 or similar)
*   Water Pump (5V DC)
*   Single-Channel Relay Module (5V)
*   Power supply/Lithium-ion battery module
*   Jumper wires & Breadboard
*   Water tubing

## Software & Libraries
*   [Arduino IDE](https://www.arduino.cc/en/software) or PlatformIO
*   (List any specific libraries here, e.g., FreeRTOS for task management or Wi-Fi libraries)

## Wiring Configuration
| Component | Microcontroller Pin |
| :--- | :--- |
| Moisture Sensor (AOUT) | Analog Pin (e.g., GPIO32) |
| Relay Module (IN) | Digital Pin (e.g., GPIO26) |
| Pump (VCC) | Connected via Relay to Power Source |
| All Components (GND) | Common GND |

## Installation & Setup
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/watering-system.git](https://github.com/yourusername/watering-system.git)
