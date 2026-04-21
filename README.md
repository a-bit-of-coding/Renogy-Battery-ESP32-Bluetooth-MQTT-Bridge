# ESP32 Renogy Battery Bluetooth to MQTT Bridge

This project allows an **ESP32** to connect to multiple **Renogy Smart Lithium Batteries** simultaneously via **Bluetooth (BLE)**. It fetches real-time battery data and publishes it to an **MQTT Broker** over WiFi, making it easy to integrate your battery bank into smart home systems like Home Assistant, OpenHAB or Node-RED.

## 🚀 Features

* **Multi-Battery Support:** Connects to multiple batteries in your bank.
* **Real-time Monitoring:** Fetches voltage, current, state of charge (SoC), temperature, and cell voltages.
* **Bluetooth Low Energy (BLE):** No physical wiring to the batteries required.
* **MQTT Integration:** Standardized data transmission for easy integration.
* **Auto-Reconnect:** Automatic handling of WiFi and Bluetooth connection drops.

## 📋 Data Points Fetched

The following information is retrieved from each battery:
* Total Voltage & Current
* Remaining Capacity (Ah) and SoC (%)
* Battery Temperature
* Individual Cell Voltages

## 🛠 Prerequisites

* **Hardware:** ESP32 (DevKit V1 or similar).
* **Software:** * Arduino IDE or VS Code/PlatformIO.
  * Libraries: `PubSubClient`, `NimBLE-Arduino` (recommended for better BLE performance).

## ⚙️ Configuration

Before uploading, rename `config.h.example` to `config.h` and fill in your credentials.

* Board: ESP32 Dev Module, Tools > Partition Scheme > Huge App
* Core: 3.3.7
* NimBLE 2.5
* ESPTelnet by Lennart 2.2.3
