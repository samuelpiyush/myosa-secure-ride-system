---
publishDate: 2025-09-15
title: MYOSA Secure Ride System (MSRS)
excerpt: A wireless helmet-based ignition interlock system ensuring two-wheeler safety using dual ESP32 controllers.
image: msrs-cover.jpg
tags:
  - embedded
  - iot
  - safety
  - esp32
---

> Guardian Link: Secure, Wearable Sensor Interlock for Two-Wheeler Safety

---


## Acknowledgements
This project was developed by Team Asterix as part of the MYOSA initiative.

## Overview

The MYOSA Secure Ride System (MSRS) is a safety-focused ignition interlock system designed for two-wheelers. 
The system ensures that the vehicle ignition remains disabled unless the rider is wearing a helmet.

The architecture uses a dual-microcontroller, fully wireless design. A MYOSA ESP32 board acts as the vehicle-mounted controller, while an external ESP32 embedded in the helmet acts as a sensor hub. Helmet wear confirmation is transmitted securely via Bluetooth Low Energy (BLE), after which the ignition relay is activated.

This approach improves rider safety, prevents helmet misuse, and adds anti-theft protection through motion detection and wireless alerts.

### Images

<p align="center">
  <img src="/system-architecture.jpg" width="800"><br/>
  <i>Overall system architecture of the MYOSA Secure Ride System</i>
</p>

### Videos

<video controls width="100%">
  <source src="/msrs-demo.mp4" type="video/mp4">
</video>

## Features (Detailed)

### 1. Wireless Helmet Verification
An ESP32 inside the helmet collects proximity and pressure/temperature data to verify that the helmet is worn.

### 2. Secure BLE Communication
A low-latency, encrypted BLE link transmits the helmet-worn confirmation to the MYOSA board.

### 3. Ignition Interlock System
The MYOSA ESP32 activates a relay through a MOSFET only after successful helmet verification.

### 4. Anti-Theft Detection
The onboard MPU6050 detects unauthorized movement and triggers alerts via Wi-Fi.

### 5. Real-Time Status Display
An OLED screen displays system states such as “Helmet Required”, “Ready”, and “Alert Mode”.

## Usage Instructions

1. Power the vehicle-mounted MYOSA board.
2. Power the helmet ESP32 module.
3. Wear the helmet properly.
4. Wait for the “Ready” status on the OLED display.
5. Start the vehicle once the ignition relay is enabled.

## Tech Stack

* ESP32 (MYOSA Board)
* External ESP32 Microcontroller
* APDS-9960 Proximity Sensor
* BMP180 Pressure & Temperature Sensor
* MPU6050 Accelerometer & Gyroscope
* Bluetooth Low Energy (BLE)
* Wi-Fi
* Embedded C / Arduino Framework

## Requirements / Installation

* Arduino IDE
* ESP32 Board Package
* BLE Libraries
* Sensor libraries (APDS9960, BMP180, MPU6050)



