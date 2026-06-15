# Computer Networks Assignment - Router Configuration and Routing Protocols

## Project Overview
[cite_start]This repository contains the practical implementation for the **Computer Networks** module assignment at **NSBM Green University Town**[cite: 5, 6]. [cite_start]The core objective of this project is to design, configure, and evaluate different routing paradigms—including **Static Routing**, **RIPv2**, and **EIGRP**—using **Cisco Packet Tracer**[cite: 3, 4, 121].

**Student Details:**
* [cite_start]**Name:** T.G.U.Sasanka [cite: 9]
* [cite_start]**Student ID:** 39301 [cite: 10]
* [cite_start]**Lecturer:** Mr. Krishantha Ranaweera [cite: 7]
* [cite_start]**Submission Date:** 14 June 2026 [cite: 8]

---

## 🛠️ Repository Contents
This repository includes the following essential deliverables required for submission:
* 📁 **Cisco Packet Tracer Workspace Files (.pkt):**
    1.  [cite_start]`Task2_StaticRouting.pkt` - Triangular topology connecting the remote subnets via static mapping.
    2.  [cite_start]`Task3_PartA_RIP.pkt` - Linear topology deployed with RIPv2 dynamic routing protocol.
    3.  [cite_start]`Task3_PartB_EIGRP.pkt` - Linear topology deployed with EIGRP Autonomous System 10 framework[cite: 182, 240].
* 📄 **Documentation:**
    * `README.md` - Technical setup guidelines and structural repository overview.

---

## 📐 Network Topologies & Addressing Layouts

### 1. Triangular Topology (Task 2 - Static Routing)
[cite_start]Used to demonstrate manual explicit path configuration across isolated networks using next-hop routing:
* [cite_start]**Router 1 LAN Subnet:** `192.168.1.0/24` [cite: 106, 107]
* [cite_start]**Router 2 LAN Subnet:** `192.168.2.0/24` [cite: 111, 112]
* [cite_start]**Router 3 LAN Subnet:** `192.168.3.0/24` [cite: 116, 117]
* **Inter-Router Transit WAN Links:** `12.0.0.0/30` | `11.0.0.0/30` | [cite_start]`10.0.0.0/30` [cite: 106, 107, 112]

### 2. Linear Topology (Task 3 - Dynamic Routing)
[cite_start]Used to contrast auto-discovery and path convergence across regional university networks using RIP and EIGRP[cite: 121, 241]:
* [cite_start]**KandyNSBM LAN Subnet:** `172.16.0.0/16` [cite: 124, 129]
* [cite_start]**Kandy to Colombo Inter-WAN Link:** `14.0.0.0/30` [cite: 130, 136]
* [cite_start]**Colombo to Galle Inter-WAN Link:** `15.0.0.0/30` [cite: 137, 143]
* [cite_start]**GalleNSBM LAN Subnet:** `173.16.0.0/16` [cite: 138, 144]

---

## 🚀 Configuration & Execution Blocks

### 1. Basic Device Hardening (Task 1)
[cite_start]Baseline terminal identification provisioning and securing management lines with local passwords[cite: 12, 22]:

```text
Router> enable
Router# configure terminal
Router(config)# hostname kandyNSBM_39301
kandyNSBM_39301(config)# line console 0
kandyNSBM_39301(config-line)# password NSBM
kandyNSBM_39301(config-line)# login
kandyNSBM_39301(config-line)# end
kandyNSBM_39301# write memory
