# 🏢 Office Network Simulation using Cisco Packet Tracer

This project is a simulation of a complete office network using **Cisco Packet Tracer**, designed for learning and demonstration purposes. It includes 4 interconnected routers in a **ring topology**, with each router connecting to its own LAN segment consisting of switches and PCs. A central server is also configured to provide services to the entire network.

---

## 📁 Project Structure


---

## 🌐 Network Design Overview

- 🔁 **4 Cisco 2811 Routers** connected in a ring topology
- 🖧 **4 Cisco 2960 Switches** (1 per router)
- 🖥️ **8 PCs** (2 per switch)
- 🗄️ **1 Server** (providing services to the entire network)
- 📡 **Routing Protocol**: RIP v2
- 🌍 **All devices can communicate** across the entire network

---

## 🧩 IP Addressing Scheme

| Segment         | Subnet            | Devices                             |
|-----------------|-------------------|-------------------------------------|
| R0 LAN          | 192.168.10.0/24   | PC0, PC1, Server                    |
| R1 LAN          | 192.168.20.0/24   | PC2, PC3                            |
| R2 LAN          | 192.168.30.0/24   | PC4, PC5                            |
| R3 LAN          | 192.168.40.0/24   | PC6, PC7                            |
| Router Links    | 192.168.0.0/30 → 192.168.3.0/30 | Inter-router communication  |

---

## ⚙️ Routing Configuration (RIP)

All routers use RIP v2 for dynamic routing:
```bash
router rip
 version 2
 no auto-summary
 network 192.168.0.0
 network 192.168.1.0
 network 192.168.2.0
 network 192.168.3.0
 network 192.168.10.0
 network 192.168.20.0
 network 192.168.30.0
 network 192.168.40.0

🖥️ Server Configuration
IP Address: 192.168.10.100

Default Gateway: 192.168.10.1

Services: HTTP, DNS (optional)

🚀 How to Use
Open the .pkt file in Cisco Packet Tracer.

Explore the topology and configuration.

Use the Command Prompt in any PC to ping other PCs or the Server.

Open a web browser in a PC and access http://192.168.10.100 if HTTP service is enabled.

🎯 Learning Objectives
Understand LAN and WAN configurations

Configure and test dynamic routing (RIP)

Use Cisco devices (2811 Routers, 2960 Switches)

Simulate real-world office network setups

📸 Preview
Coming soon: Screenshot of the topology.

📃 License
This project is open-source and intended for educational use. Feel free to use or modify it for your own labs or assignments.

🙌 Credits
Created by [Your Name]
Project for network simulation using Cisco Packet Tracer.



---

Let me know if you'd like to customize the author name, add diagrams/screenshots, or include multiple services like DHCP or DNS in the README!
