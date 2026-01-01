# Intro to LAN

**Path:** Pre-Security (TryHackMe)  
**Difficulty:** Easy  
**Status:** Completed ✅  
**Date:** 01 Jan 2026  
**Time spent:** 30 minutes  

---

## 🎯 Objective
Learn the technologies and designs that power private networks, including LAN topologies, subnetting basics, ARP, and DHCP. 

---

## 1) LAN Topologies
A network **topology** describes how devices are arranged/connected in a LAN. 

### Common topologies
- **Star topology:** Devices connect to a central switch/hub; common and easy to manage but the central device is a single point of failure. 
- **Bus topology:** Devices share one main backbone cable; cheaper but can become slow and harder to troubleshoot. 
- **Ring topology:** Devices form a loop; one break can affect the whole network (depends on implementation). 

---

## 2) Subnetting (Primer)
Subnetting is the process of splitting a larger network into smaller networks (subnets) so IP addressing and network management becomes easier and more organize.

**Why subnetting matters:**
- Better organization of devices
- Reduces broadcast traffic
- Helps apply security and access control by network segments 
---

## 3) ARP (Address Resolution Protocol)
ARP resolves an **IP address** (logical identifier) to a **MAC address** (physical identifier) inside a local network.

### ARP message types
- **ARP Request:** Broadcast “Who has this IP?” 
- **ARP Reply:** The owner replies with its MAC address. 

---

## 4) DHCP (Dynamic Host Configuration Protocol)
DHCP automatically assigns IP configuration to new devices joining a network (IP address, gateway, DNS, etc.). 

### DHCP flow (high level)
- Discover → Offer → Request → ACK (device asks, server offers, device accepts, server confirms). 

---

## 💡 Key Takeaways
- Topologies affect reliability and troubleshooting. 
- Subnetting helps manage and segment networks. 
- ARP maps IP ↔ MAC on LAN. 
- DHCP makes IP assignment automatic. 

---

## Why this matters for pentesting
Most real environments are segmented networks, and understanding LAN behavior (ARP, DHCP, topology) helps later with enumeration, traffic analysis, and attacks like spoofing in advanced rooms. 

---

## Next room
OSI Model
