# XL Network Solutions - Multi-Floor Network Design

## 📄 Project Overview

This project demonstrates the design and configuration of a multi-floor enterprise network for XL Network Solutions, a mid-sized company operating across seven floors. Each floor is equipped with its own set of devices, switches, and routers, forming a segmented yet interconnected network.

---

## 🏢 Physical Scenario Creation

This network represents a seven-floor building of XL Network Solutions, where each floor accommodates 8 PCs. Floor-wise topologies are distributed as follows:

| Floor No. | Topology |
|---|---|
| Floor 1 | Star |
| Floor 2 | Star |
| Floor 3 | Mesh |
| Floor 4 | Mesh |
| Floor 5 | Ring |
| Floor 6 | Ring |
| Floor 7 | Ring |

### Network Hardware

- **Switch Used:** Cisco 2960
- **Router Used:** Cisco 2911

### Physical Layout

- Each floor has a dedicated 2960 switch connecting all devices using Fast Ethernet ports.
- Each floor has a dedicated 2911 router.
- Routers across floors are connected in a **bus topology** for seamless inter-floor communication.
- Switch-to-Router connections use **Gigabit Ethernet** to ensure high-speed transfer.
- Inter-floor router connections also use **Gigabit Ethernet** for improved bandwidth.

---

## 🌐 IP Addressing Scheme

To ensure clear segmentation and efficient IP management, floor-wise addressing was implemented. The first three floors use **Private Class B IPs**, while the top four floors use **Public Class C IPs**.

| Floor No. | Gateway | IP Range (PCs) |
|---|---|---|
| Floor 1 | 172.16.1.1 | 172.16.1.2 - 172.16.1.9 |
| Floor 2 | 172.17.1.1 | 172.17.1.2 - 172.17.1.9 |
| Floor 3 | 172.18.1.1 | 172.18.1.2 - 172.18.1.9 |
| Floor 4 | 200.200.1.1 | 200.200.1.2 - 200.200.1.9 |
| Floor 5 | 200.201.1.1 | 200.201.1.2 - 200.201.1.9 |
| Floor 6 | 200.202.1.1 | 200.202.1.2 - 200.202.1.9 |
| Floor 7 | 200.203.1.1 | 200.203.1.2 - 200.203.1.9 |

---

## 📡 Routing Protocol

- **Protocol Used:** RIP (Routing Information Protocol)
- Each floor’s router exchanges routing information dynamically using RIP.
- This ensures all floors learn about each other’s networks automatically.

---

## 🔗 Inter-PC Communication Testing

- **Ping Command:** Used to verify connectivity between devices on different floors.
- **Tracert Command:** Used to trace packet flow and understand the routing path between floors.

---

## 📷 Snapshots

Physical network design and device configurations were documented through snapshots:

| Figure No. | Description |
|---|---|
| Fig 1 | Floors 1-3 Layout |
| Fig 2 | Floors 4-7 Layout |
| Fig 3 | Full Network View (Floors 1-7) |
| Fig 4 | Example Router Configuration (Floor 2) |
| Fig 5 | Example Traceroute Command Output |

---

## 📬 About Me

- **Project By:** Aryan
- **Contact:** aryandangi362006@gmail.com


---

## 📑 Purpose of the Project

- To demonstrate practical understanding of IP addressing, subnetting, and topology design.
- To practice configuration of Cisco Routers and Switches.
- To simulate and troubleshoot real-world enterprise networking scenarios.
