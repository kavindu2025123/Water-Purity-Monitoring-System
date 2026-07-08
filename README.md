# 💧 Automated Water Purity Monitoring System

An embedded data acquisition and signal processing system for continuous water quality monitoring using a Raspberry Pi Pico and turbidity sensor.

This project was developed as part of the Data Acquisition & Signal Processing course and demonstrates real-time sensor interfacing, calibration, digital signal filtering, timestamped data logging, and water turbidity trend analysis.

---

## 📌 Project Overview

The system continuously measures water turbidity (NTU), processes noisy sensor readings using digital filtering techniques, and stores timestamped measurements for later analysis.

Unlike simple sensor projects, this system focuses on improving measurement accuracy through sensor calibration and advanced signal processing.

---

## ✨ Features

- Real-time turbidity measurement
- Analog data acquisition using Raspberry Pi Pico
- Sensor calibration using a professional turbidity meter
- Conversion of voltage to NTU using a quadratic calibration model
- RTC-based timestamping
- EEPROM data logging
- Digital signal filtering
- Noise reduction and outlier removal
- Trend analysis of water quality
- Low-cost embedded monitoring solution

---

## 🛠 Hardware

- Raspberry Pi Pico
- Turbidity Sensor Module
- DS3231 RTC Module
- 24C08 EEPROM
- Breadboard & Supporting Components

---

## ⚙ Software & Tools

- C Programming
- Raspberry Pi Pico SDK
- Python
- NumPy
- Matplotlib
- Signal Processing Algorithms

---

## 📈 System Workflow

Sensor
↓

Analog Voltage

↓

Raspberry Pi Pico ADC

↓

Calibration Equation

↓

Digital Signal Filtering

↓

Timestamp (RTC)

↓

EEPROM Data Logging

↓

Data Analysis & Visualization

---

## 📊 Signal Processing

Several filtering techniques were evaluated:

- Moving Average
- Exponential Moving Average (EMA)
- Median Filter
- Hampel Filter

After sensitivity analysis, the **Median Filter (Window = 9)** provided the best balance between:

- Noise reduction
- Signal preservation
- Stable measurements

---

## 📐 Sensor Calibration

The turbidity sensor was calibrated against a professional turbidity meter.

Quadratic calibration model:

T = 496.8V² − 3804.8V + 7154.5

Where:

- **T** = Turbidity (NTU)
- **V** = Sensor Voltage

This significantly improved measurement accuracy compared to raw sensor readings.

---

## 📁 Data Logging

Every measurement includes:

- Timestamp
- Sensor Voltage
- Calculated NTU

Measurements are automatically stored in EEPROM every 20 minutes.

---

## 📊 Results

- Successfully collected 100 continuous measurements
- Reduced sensor noise using digital filtering
- Improved accuracy through calibration
- Enabled trend analysis of water turbidity over time

---

## 🚀 Future Improvements

- Wi-Fi / MQTT connectivity
- Cloud dashboard
- Mobile application
- pH sensor integration
- TDS sensor integration
- Automatic contamination alerts
- SD card storage
- Battery-powered deployment

---

## 🎯 Applications

- Smart Aquariums
- Drinking Water Monitoring
- Environmental Monitoring
- Water Treatment Plants
- Research Laboratories
- IoT Water Quality Systems

---

## 👨‍💻 Team

- Kavindu Gamhatha
- Shyaman Jeewannath
- Sathsara Achintha
- Vishwa Anjana

---

## 📄 License

MIT License
