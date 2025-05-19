

<h1 align="center">💥Cyber Noise Blaster V1 — BLE/WiFi Jamming Suite 💥</h1>

<p align="center">
  <a href="#"><img src="https://img.shields.io/badge/Jammer-BLE%2FWiFi-red?style=for-the-badge&logo=bluetooth"></a>
  <a href="#"><img src="https://img.shields.io/badge/Version-1.0-blue?style=for-the-badge"></a>
  <a href="#"><img src="https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge"></a>
  <a href="#"><img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge"></a>
  <a href="#"><img src="https://img.shields.io/badge/⚠️_Educational_Use_Only-red?style=for-the-badge"></a>
</p>

---


https://<your-username>.github.io/<repository-name>/

---

## 🧠 Project Overview

The **Cyber Noise Blaster V1** is an open-source, hardware-based pentesting tool designed to **jam BLE & Wi-Fi** signals using **ESP32** and one or two **NRF24L01+ PA/LNA** modules. Perfect for red teaming, security demonstrations, and educational purposes.

With flexible SPI support, you can run either a **single** or **dual** jamming setup by simply adjusting the wiring and modifying the code.

---

**Cyber Noise Blaster V1** is a next-gen cyber-disruption device built on ESP32 + NRF24L01 modules. It leverages RF noise bursts and smart channel hopping to jam or confuse 2.4GHz-based communication systems, including:

- 📶 **Wi-Fi (1–14 channels)**
- 🎧 **Classic Bluetooth (80 channels)**
- 💙 **BLE (Bluetooth Low Energy - 40 channels)**
- 🚁 **2.4GHz RC drones / IoT gadgets (up to 125 channels)**

📡 **Payload-based signal interference** is created by transmitting noise packets across multiple frequency channels.

---

- ✅ BLE Jamming – Disrupts BLE 4.0 / 5.0 signals.
- ✅ Noise Signal Generator – Generates interference with random payload.
- ✅ NRF24 Channel Hopping – Can hop across up to 125 channels.
- ✅ Extendable to WiFi Jamming – Transition from BLE to WiFi jamming is possible.
- ✅ **30+ Meter Range** – With simple 2.4GHz antennas.
- ✅ **Compact PCB Design** – Ready for portable deployment.
- ✅ **Ideal for Security Research & Pentesting.**

---

## ⚙️ Hardware Required

| Component       | Description                         |
|----------------|-------------------------------------|
| ESP32           | Main microcontroller                |
| NRF24L01+       | 2.4GHz signal transceiver           |
| PCB             | Custom PCB designed by you          |
| Antenna         | Basic 2.4GHz or Router Antenna      |
| Power Supply    | 5V via USB or LiPo Battery          |

✔️ Fully compatible with your **custom PCB V1 design**

---

## 💣 Key Features

- ✅ BLE Jammer (Default in V1)
- 🚧 Wi-Fi & Classic Bluetooth Jamming *(future firmware update)*
- 🧠 Smart channel hopping across 2.4GHz
- 📈 Extended range: 30+ meters (can be boosted)
- 🛠 Payload size customizable in `RF24.cpp` @ Line 1972
- 🔍 Real-time debugging over serial monitor


## 📡 Wiring Diagram & Pin Configuration

Below is the pinout for connecting **NRF24L01+** modules to the **ESP32**:

### 🔁 Dual NRF24L01+ (Advanced Mode)

| NRF Module | SPI Bus | ESP32 Pins           |
|------------|---------|----------------------|
| Module 1   | HSPI    | 🧠 SCK = 14, MISO = 12, MOSI = 13, CS = 15, CE = 16 |
| Module 2   | VSPI    | ⚙️ SCK = 18, MISO = 19, MOSI = 23, CS = 21, CE = 22 |

---

### 🧩 Single NRF24L01+ (Basic Mode)

You can choose **either** HSPI **or** VSPI:

| SPI Bus | ESP32 Pins                          |
|---------|-------------------------------------|
| VSPI    | 📦 SCK = 18, MISO = 19, MOSI = 23, CS = 21, CE = 22 |
| HSPI    | 📦 SCK = 14, MISO = 12, MOSI = 13, CS = 15, CE = 16 |

---

### 🔘 Optional: Switch Button Pin

You can attach a button/switch to:

- 🟢 `GPIO 33` → Use it to **manually trigger jamming** or mode switching!

---

💡 Make sure to use **capacitors** (10uF–100uF) close to the NRF24 module if you face power instability issues!

---

> ✨ This modular wiring design makes it super easy to scale the project in **future versions**, including OLED displays and more!


## 🤝 Contributing
Pull requests are welcome. For major changes, please open an issue first.

## ⚠️ Disclaimer
This project is for **educational and ethical security research only**. Misuse may be illegal. Use responsibly.

## 📜 License
[MIT License](LICENSE) – feel free to use and modify with credit.

