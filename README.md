# Packet Sniffer in Python (Windows)

## 📌 Objective
Create a basic **packet sniffer** using Python that captures and displays raw network packets on a Windows system. This tool is useful for learning how packet capturing works at a low level.

---

## ⚙️ Requirements

- **Python 3.6+**
- **Windows OS**
- **Administrator Privileges** (required for raw socket access)
---

### 📦 Python Dependencies


`pip install colorama`

`colorama` is optional — used for colored terminal output. You can remove it if you prefer plain text.

---

### 🧰 Features

- Captures raw packets on a selected network interface

- Displays protocol-level information (IP, TCP, UDP, ICMP)

- Lightweight and easy to extend
---

### 📄 How It Works

- Uses raw sockets to intercept traffic.

- Parses Ethernet and IP headers manually.

- Displays source, destination IPs, and protocol type.

---

### 🚀 Getting Started

1. Install Npcap (if not already installed)

- Download and install it from: (https://nmap.org/npcap/)

- Ensure that "Install Npcap in WinPcap API-compatible Mode" is checked during installation.

2. Clone the Repository

```python
git clone https://github.com/your-username/packet-sniffer-python.git
cd packet-sniffer-python
```

3. Run the Sniffer as Administrator
   
   `python sniffer.py`
---

### 🔍 Sample Output

```python
Available Interfaces:
0: \Device\NPF_{D84265DB-3CCE-465E-8373-428E4F363E0B}
1: \Device\NPF_{825ABF3A-551D-4F47-B75E-DE94716AC41A}
2: \Device\NPF_{1D7BC99C-08B0-4B7D-B50E-F34B7A4B3793}
3: \Device\NPF_{680CA062-7EFF-4FA6-B1A2-BA445E868D1D}
4: \Device\NPF_{3BE6988A-A4A2-427A-B1D6-25CFB67CEBC9}
5: \Device\NPF_{3E532C12-D71A-43E7-AA23-70A892912E38}
6: \Device\NPF_{F5D1CED8-1458-4D5D-B82E-6B32B39EDDB6}
7: \Device\NPF_Loopback
8: \Device\NPF_{20FC7FC1-1B93-4115-9AE5-F48E08F63AFC}

Select interface number to sniff on: 0

[*] Starting packet sniffing on: \Device\NPF_{D84265DB-3CCE-465E-8373-428E4F363E0B}
[*] Packet captured: Src=192.168.1.10 Dst=142.250.190.14 Protocol=TCP
[*] Packet captured: Src=192.168.1.10 Dst=142.250.190.14 Protocol=UDP
[*] Packet captured: Src=192.168.1.10 Dst=142.250.190.14 Protocol=ICMP
...
```
---
### 🔐 Disclaimer

This tool is intended for educational and authorized testing only. Unauthorized use on networks you don’t own or have permission to monitor may violate laws or terms of service.


