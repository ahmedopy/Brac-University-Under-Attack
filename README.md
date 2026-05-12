# 🛡️ BRAC University Under Attack

A multi-area network design & security simulation project for a university campus under cyber attack.

## 📌 Overview

This project simulates the **BRAC University network** under a coordinated cyber attack scenario.  
We designed and configured a hierarchical routed network with redundancy, DHCP relay, RIP v2 and failover routes to maintain service availability.

**Tools:** Cisco Packet Tracer, Cisco 2901 Routers, 2960-24TT Switches

---

## 🏛️ Network Architecture
- ✅ **Four campus subnets:** CSE (`10.0.0.0/22`), EEE (`10.0.8.0/22`), MNS (`10.0.12.0/23`), ADMIN (`10.0.14.0/24`)
- ✅ **Centralized server block:** Web Server, DNS Server, Email Server, DHCP Server (`10.0.15.0/29`)
- ✅ **Super PCs per department:** CSE, EEE, MNS, ADMIN, SERVER
- ✅ **WAN links between routers:** Serial connections with `/30` subnetting

## 🚦 Routing Protocols & Techniques
- ✅ **Dynamic Routing (RIPv2):** Version 2 with no auto-summary
- ✅ **Passive interfaces:** On GigabitEthernet ports to prevent unnecessary updates
- ✅ **Recursive static routing:** Next-hop resolution via routing table
- ✅ **Floating static routes:** Backup routes with Administrative Distance 200
- ✅ **Default gateway configuration:** For all end devices and servers

## 🔁 Failover & Redundancy
- ✅ **Primary/Backup WAN links:** Automatic failover when primary link fails
- ✅ **ADMIN to CSE link:** Primary `10.0.15.18` | Backup `10.0.15.29`
- ✅ **ADMIN to EEE link:** `10.0.15.22`
- ✅ **ADMIN to MNS link:** `10.0.15.26`
- ✅ **Server to Backup link:** `10.0.15.14` (Server) & `10.0.15.13` (Backup)

## 📡 DHCP & Address Management
- ✅ **DHCP Relay (IP Helper-Address):** CSE and MNS routers relay DHCP requests to `10.0.15.5`
- ✅ **DHCP Server:** Centralized at `10.0.15.5` (Server Block)
- ✅ **Dynamic IP assignment:** For CSE, EEE, and MNS department PCs
- ✅ **Static IP assignment:** For servers, routers, and Super PCs

## ⚙️ How to Run

1. Install **Cisco Packet Tracer** (v8+ recommended)
2. Open `simulations/bracu_under_attack.pkt`
3. Verify:
   - DHCP leases on CSE/EEE/MNS PCs
   - Ping from any PC to `10.0.15.1` (server gateway)
   - Failover: shut down primary link, traffic reroutes via backup
  

