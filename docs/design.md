# Network Design

The topology is split into three main sections:


## Left LAN (EIGRP AS 110)
- Cisco 2911 router  
- Cisco 3750 switch  
- HPE 2530 switch  
- PCs 1 and 2  
- VLANs 1101–1104

This side acts as one half of each HSRP gateway pair.

## Right LAN (EIGRP AS 111)
- Cisco 4331 router  
- Cisco 3750 switch  
- One or two lab PCs  
- Same VLANs (1101–1104)

This side provides the other half of the HSRP gateway pairs.


## Core / Edge
- Juniper SRX345 with LACP connections to both routers  
- Edge router performing NAT  
- Windows VM + TFTP server at the bottom of the topology  

The SRX sits between both routing domains, and redistribution happens on the routers that connect to it.
