## 🧪 Terminal Simulation

```bash
[+] Initializing...
[+] NRF24 ready ✓
[+] BLE Jammer ON!
[+] Target Range Detected: 12m

# 🚨 Cyber Noise Blaster V1 🔊  
_Disrupt. Jam. Control. The 2.4GHz Battlefield._

![PCB Image](./download.png)  
> An advanced signal disruption platform using ESP32 & NRF24L01+ for full-spectrum jamming across 2.4GHz devices.

---

## 🔧 Project Overview

**Cyber Noise Blaster V1** is a next-gen cyber-disruption device built on ESP32 + NRF24L01 modules. It leverages RF noise bursts and smart channel hopping to jam or confuse 2.4GHz-based communication systems, including:

- 📶 **Wi-Fi (1–14 channels)**
- 🎧 **Classic Bluetooth (80 channels)**
- 💙 **BLE (Bluetooth Low Energy - 40 channels)**
- 🚁 **2.4GHz RC drones / IoT gadgets (up to 125 channels)**

📡 **Payload-based signal interference** is created by transmitting noise packets across multiple frequency channels.

---

## ⚙️ Hardware Components

| Component        | Description                          |
|------------------|--------------------------------------|
| 🧠 ESP32 Devkit  | Main controller, supports WiFi + BLE |
| 📡 NRF24L01+     | Noise payload broadcaster            |
| 🔌 3.3V Regulator | Power supply stabilization           |
| 📶 Antenna        | Optional high-gain 2.4GHz antenna    |

✔️ Fully compatible with your **custom PCB V1 design**

---

## 💣 Key Features

- ✅ BLE Jammer (Default in V1)
- 🚧 Wi-Fi & Classic Bluetooth Jamming *(future firmware update)*
- 🧠 Smart channel hopping across 2.4GHz
- 📈 Extended range: 30+ meters (can be boosted)
- 🛠 Payload size customizable in `RF24.cpp` @ Line 1972
- 🔍 Real-time debugging over serial monitor

---

## 📁 File Structure


---

## 📡 Supported Jamming Spectrum

| Device Type        | Frequency Band       | Channels Used   |
|--------------------|----------------------|------------------|
| Bluetooth Classic  | 2.402–2.480 GHz       | 80               |
| BLE (Low Energy)   | 2.402–2.480 GHz       | 40               |
| WiFi (2.4 GHz)     | 2.412–2.484 GHz       | 14               |
| NRF/Drone          | 2.400–2.525 GHz       | Up to 125        |

> 🔧 Code can be modified to support full 125-channel hopping (see `RF24_setChannel()` in `main.ino`)

---

## 🚀 Setup Instructions

1. Flash the `main_ble_jammer.ino` code to ESP32 using Arduino IDE
2. Ensure NRF24L01 is connected to ESP32 as per `/hardware` schematic
3. Open serial monitor – if noise transmission starts, device is working
4. For BLE jamming, make sure device is within 10–20m range of targets

---

## 🧠 Future Upgrades (V2 Roadmap)

- [ ] OLED Screen for real-time status
- [ ] Web-based GUI for payload/channel control
- [ ] WiFi jammer payloads (Beacon Floods, Deauth)
- [ ] Drone auto-detection & kill-switch
- [ ] ESP32-CAM based visualization (attack feedback)

---

## 📢 Antenna Tips

- Use standard 2.4GHz WiFi antennas for better range
- Add external amplifier module (PA+LNA) for increased disruption power
- Use shielded wiring for NRF24L01 for stable signal

---

## ⚠️ Legal Notice

> 🛑 This tool is for **educational & controlled testing** only.  
> 📵 **Jamming is illegal in many countries** without government permission.  
> 📜 Use responsibly. We are not responsible for any misuse.

---

## 📜 License

MIT License – Use, modify, distribute with freedom.

---

### Made with 🔥 by a passionate cyber engineer.