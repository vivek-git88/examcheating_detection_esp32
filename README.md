# examcheating_detection_esp32
this system detects wifi and bluetooth of device within a particular enviroment and give alert after processing
#  Smart Wireless Activity Monitoring System
## (WiFi & Bluetooth Detection for Exam Monitoring)


## Overview

The Smart Wireless Activity Monitoring System is intended to detect any malicious wireless activity in a controlled setting such as an examination hall. The system is intended to scan for **Bluetooth Low Energy (BLE) devices** and **WiFi activity** in the surrounding region to detect any misuse of wireless technology.

An **ESP32 microcontroller** is used for real-time scanning and uploading the data to a backend server, where the data is shown on a live monitoring dashboard.


## Objectives

- Scan for nearby Bluetooth devices.
- Scan for surrounding WiFi activity.
- Estimate the proximity of devices using signal strength (RSSI).
- Detect suspicious wireless activity patterns.
- Show real-time alerts on a web-based dashboard.
- Improve exam integrity using non-intrusive monitoring.



## Key Features

### Bluetooth Detection
- Scan for nearby **BLE devices**.
- Calculate signal strength (RSSI).
- Detect the manufacturer (if possible).
- Estimate proximity to the device.
- Record repeated detection (persistence).

### WiFi Monitoring
- Scan for nearby **WiFi networks**.
- Detect high wireless activity.
- Relate WiFi activity to BLE detection.

###  Smart Detection Logic
- Detect strong nearby signals.
- Record persistent device presence.
- Combine BLE & WiFi activity to score risks.
## System Architecture
ESP32 (BLE + WiFi Scan)
Flask Backend Server
Web Dashboard (Live Monitoring)


## Hardware Requirements

- ESP32 Development Board  
- USB cable for programming  
- Computer for backend server  
- WiFi network access  


## Software Requirements

- Arduino IDE  
- ESP32 board package  
- Python 3.x  
- Flask framework  
- Web browser  



##Working Principle

1. ESP32 scans nearby BLE devices.
2. Signal strength (RSSI) is measured.
3. Nearby WiFi networks are counted.
4. Persistence of strong signals is tracked.
5. A risk score is computed.
6. Data is sent to the backend server.
7. Dashboard displays real-time monitoring results.


##Detection Parameters

| Parameter | Purpose |
|----------|--------|
| RSSI | Estimates device proximity |
| Persistence | Detects continuous presence |
| Strong Device Count | Identifies nearby devices |
| WiFi Count | Measures wireless activity |



## Risk Classification

| Status | Meaning |
| SAFE | No suspicious activity |
| SUSPICIOUS | Moderate wireless activity |
| HIGH | Strong & persistent activity |


## Privacy & Ethical Compliance

This system:

- Does **NOT identify users**
- Does **NOT store personal data**
- Uses anonymous wireless signal detection
- Respects BLE privacy mechanisms
- Focuses only on wireless activity patterns


## Limitations

- Cannot identify device owners.
- RSSI provides approximate distance only.
- Devices with Bluetooth OFF cannot be detected.
- Environmental interference may affect readings.
- WiFi scan detects networks, not specific users.
  

##  Future Enhancements

- RF signal detection integration
- Multi-node triangulation
- Machine learning classification
- Alert notification system
- Data logging & analytics



## Applications

- Examination hall monitoring
- Secure testing environments
- Research labs
- Restricted area monitoring
- Wireless activity analysis


## Conclusion

This system provides a privacy-safe solution for detecting suspicious wireless activity using Bluetooth and WiFi scanning. By combining signal strength analysis and persistence tracking, it enhances monitoring reliability while maintaining ethical compliance.

