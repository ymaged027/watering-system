# Automated Plant Watering System 🌿💧

## Overview
This project is a smart, automated watering system designed to monitor soil moisture levels and trigger a water pump when hydration is needed. The repository contains documentation and code for two different build scenarios depending on your hardware availability and need for wireless connectivity.

## Build Scenarios

### Scenario A: Smart Connected System (ESP32)
This setup uses an ESP32 microcontroller to not only water the plant but also connect to Wi-Fi to log moisture data, sync with web dashboards, or send remote status updates. 
*   **Requires:** ESP32, Code execution, Wi-Fi network.
*   **Best for:** Remote monitoring and smart home integration.

### Scenario B: Offline System (Without ESP)
This setup runs entirely locally without any Wi-Fi or network dependencies. It can be built in two ways:
1.  **With an Arduino Uno/Nano:** Uses a simple C++ loop to read analog sensor values and switch a relay.
2.  **Pure Hardware (No Microcontroller):** Bypasses code entirely by wiring the LM393 comparator chip (included on most moisture sensor modules) directly to the relay module to trigger the pump when resistance changes.
*   **Requires:** Arduino Uno OR LM393 module, Relay, Pump.
*   **Best for:** Simple, reliable, and low-power offline operation.

---

## Hardware Components
*   ESP32 **OR** Arduino Uno (Depending on scenario)
*   Capacitive or Resistive Soil Moisture Sensor (with LM393 comparator module)
*   Water Pump (5V/12V DC)
*   Single-Channel Relay Module (5V)
*   Power supply (e.g., Lithium-ion battery module with TP4056 or wall adapter)
*   Jumper wires, breadboard, and water tubing

## Wiring Configuration

### ESP32 / Arduino Wiring
| Component | Microcontroller Pin |
| :--- | :--- |
| Moisture Sensor (AOUT) | Analog Pin (e.g., GPIO32 on ESP, A0 on Arduino) |
| Relay Module (IN) | Digital Pin (e.g., GPIO26 on ESP, D7 on Arduino) |
| Pump (VCC) | Connected via Relay to Power Source |
| All Components (GND) | Common GND |

### Pure Hardware Wiring (No Microcontroller)
| Component | Connection |
| :--- | :--- |
| Moisture Sensor Module (DOUT) | Relay Module (IN) |
| Moisture Sensor Module (VCC & GND) | Power Source (VCC & GND) |
| Relay Module (VCC & GND) | Power Source (VCC & GND) |

---

## Installation & Setup

**For Scenario A (ESP32) and Arduino-based offline builds:**
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/watering-system.git](https://github.com/yourusername/watering-system.git)
