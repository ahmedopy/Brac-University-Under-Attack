# 🛡️ BRAC University Under Attack

> A multi-area network design & security simulation project for a university campus under cyber attack.

## 📌 Overview

This project simulates the **BRAC University network** under a coordinated cyber attack scenario.  
We designed and configured a hierarchical routed network with redundancy, DHCP relay, RIP v2 and failover routes to maintain service availability.

**Topic:** Topic 1 – BRAC University Under Attack  
**Tools:** Cisco Packet Tracer, Cisco 2901 Routers, 2960-24TT Switches

---

## 🧠 Key Features

- ✅ **Four campus subnets:** CSE, EEE, MNS, ADMIN  
- ✅ **Centralized server block:** Web, DNS, Email, DHCP  
- ✅ **RIPv2** with passive interfaces  
- ✅ **DHCP relay** across subnets  
- ✅ **Static failover routes** (primary/backup)  
- ✅ **Super PCs** per department  
- ✅ **WAN links** between routers (serial connections)
- ✅ **Recursive static routing**

## ⚙️ How to Run

1. Install **Cisco Packet Tracer** (v8+ recommended)
2. Open `simulations/bracu_under_attack.pkt`
3. Verify:
   - DHCP leases on CSE/EEE/MNS PCs
   - Ping from any PC to `10.0.15.1` (server gateway)
   - Failover: shut down primary link, traffic reroutes via backup
  

