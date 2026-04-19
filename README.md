# Network Packet Sniffer (Python)

## 📌 Overview
This project is a low-level **network packet sniffer** built using Python. It captures and analyzes raw network packets directly from the network interface and breaks them down into different protocol layers such as Ethernet, IPv4, TCP, UDP, and ICMP.

The tool is designed for **educational and learning purposes** to help understand how data travels through a network at the packet level.

---

## ⚙️ Features

- Captures raw network packets in real-time
- Parses Ethernet frames (MAC addresses + protocol type)
- Extracts and analyzes IPv4 packets
- Supports multiple protocols:
  - ICMP (Internet Control Message Protocol)
  - TCP (Transmission Control Protocol)
  - UDP (User Datagram Protocol)
- Displays detailed packet structure in a readable format
- Shows source/destination IPs, ports, flags, and payload data
- Formats raw binary data into human-readable output

---

## 🧰 Technologies Used

- Python 3.x  
- socket library (raw sockets)  
- struct (binary data unpacking)  
- textwrap (formatting output)

---

## 🚀 How to Run

⚠️ This program requires **administrator/root privileges** because it uses raw sockets.

### Linux / WSL only (recommended)

#sudo python3 main.py
#📂 How It Works

Captures raw packets from the network interface using:

socket.socket(socket.AF_PACKET, socket.SOCK_RAW, socket.ntohs(3))
Extracts Ethernet frame information:
Destination MAC
Source MAC
Protocol type
Identifies IP packets and further processes:
IPv4 header
TCP / UDP / ICMP data
Displays structured output in the terminal.
📡 Supported Protocols
Ethernet
IPv4
ICMP
TCP
UDP
⚠️ Disclaimer

This project is created strictly for educational purposes only, to understand how network packets and protocols work.

Do not use this tool on networks or systems without proper authorization. The developer is not responsible for any misuse.

👨‍💻 Author

Muzamil Khan


---

## 👍 Important note (very important)
 code uses:

socket.SOCK_RAW

That means:

❌ Will NOT work on normal Windows CMD
✔ Works on Linux / WSL / Kali Linux
✔ Requires admin/root permissions
