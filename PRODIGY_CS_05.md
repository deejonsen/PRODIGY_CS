---

# 🌐 Network Packet Sniffer

## 📖 Overview

The **Network Packet Sniffer** is a Python-based tool that captures live network traffic for analysis. Using Scapy’s powerful packet inspection capabilities, it displays source and destination IPs, protocols, and basic payload information in real time. It is designed specifically for educational and ethical use as it helps users understand how data travels across networks.

## ⚠️ **Important**: This tool should be used only in environments where you have explicit permission. Never deploy packet sniffers to monitor traffic on public networks or devices you do not own.

---

## ✨ Features

- 📡 Real-time packet capture
- 🌍 Display of source and destination IP addresses
- ⚙️ Filter traffic by protocol (e.g., TCP, UDP)
- 🔍 Analyze packet metadata and payload summary
- 🗂️ Lightweight, terminal-based monitoring
- 📦 No permanent storage (keeps RAM free by default)

---

## 🛠️ Tech Stack

| Component        | Details                                  |
|------------------|------------------------------------------|
| **Language**     | Python 3.13.5                            |
| **Library**      | `scapy`                                  |
| **Platform**     | Windows OS (requires Npcap)              |
| **Interface**    | Console-based command line               |
| **Privileges**   | Admin (to access low-level packet data)  |

---

## 🚀 Installation

### 1️⃣ Install Python

Download Python from [python.org](https://www.python.org/downloads)

### 2️⃣ Install Scapy

```bash
pip install scapy
```

### 3️⃣ Install Npcap

- Visit: [https://npcap.com](https://npcap.com)
- ✅ During setup, enable:
  - "WinPcap-compatible mode"
  - "Support loopback traffic"
  - "Install for all users"

---

## 📄 Code Sample

```python
from scapy.all import sniff, IP

def packet_callback(packet):
    if IP in packet:
        print(f"\n🔍 Packet Captured:")
        print(f"Source IP: {packet[IP].src}")
        print(f"Destination IP: {packet[IP].dst}")
        print(f"Protocol: {packet[IP].proto}")
        print(f"Summary: {packet.summary()}")

# Capture only TCP traffic (filter is optional)
sniff(filter="tcp", prn=packet_callback, store=False)
```

---

## 📈 Sample Output

```text
🔍 Packet Captured:
Source IP: 192.168.0.5
Destination IP: 172.217.22.174
Protocol: 6
Summary: Ether / IP / TCP 192.168.0.5:54321 > 172.217.22.174:443 S
```

---

## 🧪 Usage Instructions

1. Open Command Prompt **as Administrator**
2. Navigate to project folder:
   ```bash
   cd C:\Path\To\NetworkPacketSniffer
   ```
3. Run the script:
   ```bash
   python sniffer.py
   ```
4. Browse the internet or open apps to generate traffic
5. View packet info in real time

---

## 🔐 Ethical Guidelines

- 📜 Use only on networks you control or have permission to inspect.
- 🚫 Never sniff personal or private traffic on public networks.
- 👨‍🎓 Educational use only; respect digital privacy.

---

<img width="1119" height="492" alt="Screenshot 2025-07-10 190041" src="https://github.com/user-attachments/assets/a72661ae-34c6-45b1-9eec-8be98cd05667" />
<img width="985" height="517" alt="Screenshot 2025-07-14 133446" src="https://github.com/user-attachments/assets/63a0dc04-e88f-41ee-b37f-d07fb083f00a" />
<img width="1366" height="725" alt="Screenshot 2025-07-14 133410" src="https://github.com/user-attachments/assets/a3b2cd63-04fd-4f82-bfa4-46fef3ccb5b0" />
<img width="1366" height="720" alt="Screenshot 2025-07-14 132643" src="https://github.com/user-attachments/assets/98381ca1-3f34-4e74-a768-b81f19fc90d9" />
<img width="979" height="521" alt="Screenshot 2025-07-14 132531" src="https://github.com/user-attachments/assets/b925cd8c-8bbe-4fdc-90e7-59fccc9b56b7" />
<img width="976" height="515" alt="Screenshot 2025-07-14 132451" src="https://github.com/user-attachments/assets/349cb411-49ba-41b2-9f5a-7875ba207bfe" />
