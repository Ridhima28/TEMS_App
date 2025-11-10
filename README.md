# TEMS Control App

A Flutter-based mobile application for wireless control of a TEMS (Transcutaneous Electrical Muscle Stimulation) device over Bluetooth. The app connects to the device’s onboard BLE microcontroller and allows users to configure output parameters such as stimulation mode, intensity, and frequency. Designed for real-time control, safety, and smooth parameter adjustment.


### Features

* **Bluetooth Low Energy (BLE) Connection**

  * Scan, pair, and maintain a live connection to the TEMS device.
* **Real-Time Output Adjustment**

  * Change stimulation mode (e.g., pulse, continuous).
  * Control intensity, duty cycle, and other electrical parameters.
* **Live Device Feedback**

  * Displays device status, output mode, and safety/fault indicators.
* **Safe Control Logic**

  * Optional timeouts, output caps, and fail-safe shutdown behavior.

### Architecture Overview

| Layer                                                 | Responsibility                                  |
| ----------------------------------------------------- | ----------------------------------------------- |
| Flutter UI                                            | User interaction + parameter controls           |
| BLE Client (flutter_blue_plus / flutter_reactive_ble) | Connects and writes/reads BLE characteristics   |
| TEMS Device Firmware (ESP32 / nRF52 etc.)             | Applies output levels and enforces safety logic |

