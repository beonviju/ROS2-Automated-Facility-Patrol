# ROS 2 Automated Facility Patrol

## 📌 Overview
A complete Hardware-in-the-Loop (HIL) security and IoT system. An ESP32 microcontroller acts as a sensor, transmitting data over USB Serial to a Ubuntu environment. A ROS 2 node reads the serial stream, applies security logic using Live Parameters (`ros2 param`), and publishes the security status via WebSockets to a live HTML/JS dashboard.

## 🚀 Key Technologies
- **Hardware Bridging:** Integrating an ESP32 with ROS 2 via `pyserial`.
- **Live Parameters:** Dynamically changing the `safe_distance` threshold at runtime.
- **Web UI:** Using `rosbridge_server` and `roslibjs` to subscribe to ROS 2 topics directly from a web browser.

## ⚙️ Architecture
`[ESP32 Hardware] --(Serial)--> [ROS 2 Security Node] --(WebSockets)--> [HTML Dashboard]`
