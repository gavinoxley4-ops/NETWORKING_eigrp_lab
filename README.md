# Project: Distance Vector Routing & Layer 3 Redundancy  
Gavin Oxley

This repository documents my implementation of Lab 3 from my Network Engineering course.  
The goal of the lab was to deploy a multi-router, multi-switch enterprise network using:

- EIGRP (with 2 AS)
- HSRP for default gateway redundancy
- IPv4 VLAN segmentation
- LACP Link Aggregation between Cisco and Juniper
- DHCP for all VLANs
- NAT on the edge router
- NTP synchronization
- Wireshark captures of HSRP & EIGRP

All documentation in this repository was written by me in my own words.  

The official lab manual from the class wasn't included to avoid any copyright issues or academic integrity violations, but an abridged version was created in the Overview doc to explain the purpose of the lab.

---

Repository Contents

### /configs/
A semi-sanitized export of the configurations for every device in the topology:
- Cisco 2911 (EIGRP AS 110)
- Cisco 4331 (EIGRP AS 111)
- Cisco 3750 switches  
- HPE 2530 switch  
- Juniper SRX345  
- Edge Router with NAT  


## Summary of the Network 

### VLANs
- VLAN 1101  
- VLAN 1102  
- VLAN 1103  
- VLAN 1104  
- Native VLAN

### EIGRP
- **AS 110** – Left LAN  
- **AS 111** – Right LAN  

### **HSRP**
Each VLAN uses:
- Active gateway on one router  
- Standby gateway on the other  
- Virtual default gateway ending in .254

### **DHCP**
One router serves every VLAN, including a reserved IP for PC3 based on MAC.

### **NAT**
Performed on the edge router; all private networks overload to the public/WAN interface.

---

## Verification
- Devices can reach each other across AS110/111  
- HSRP failover tested successfully  
- Each VLAN receives DHCP  
- Internet outbound works through NAT  
- EIGRP adjacencies form correctly  
- Wireshark captures verify HSRP and EIGRP operations  

---

## Purpose?
This repo serves as a public record of our network engineering lab work and demonstrates skills in:
- Routing protocols  
- Layer 3 redundancy  
- Multi-vendor configuration  
- Enterprise network design  
- Troubleshooting & documentation  
- Wireshark analysis  
