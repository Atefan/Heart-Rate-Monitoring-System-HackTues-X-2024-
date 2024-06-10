# Smart School System with Heart Rate Monitoring
Welcome to the GitHub repository for our project from HackTues X 2024! Our project focuses on creating a smart school system that tracks students' heart rates using heartbeat sensors. Through a network of BLE devices, the heart rate values are sent to a backend system where they are processed using a custom-trained AI model. The result is a value between 0 and 9, indicating the level of focus of the users.

# Project Overview
Hardware Implementation
For the hardware part of the project, we utilized the NINA module on the Arduino Nano IoT along with the BLE library. There are two types of devices involved:

* Peripheral Devices:
These devices are placed on the users. They are small, mobile, and contain both the sensors and the IoT module. At the HackTues event, we used a heartbeat module and an Arduino Nano IoT for these peripheral devices. Each peripheral device sends the heart rate value it has read for one minute to the BLE service. After one minute, the central device takes over.

* Central Device:
The central device reads from all the peripheral devices. It then uses a WiFi module to send the data to the backend system.

* External WiFi module:
For the external WiFi module connected to the central device, at the HackTues event, we utilized a WiFi shield due to the limited availability of components. This WiFi shield provided the necessary connectivity for the central device to communicate with the backend system seamlessly. Despite its simplicity, the WiFi shield proved to be reliable and efficient, enabling smooth data transmission from the central device to the backend server.
