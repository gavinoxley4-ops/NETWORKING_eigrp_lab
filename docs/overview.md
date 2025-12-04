# Overview

This lab focused on building a routed IPv4 network with backup gateways and two separate EIGRP domains.  
We had two main parts of the network (left and right), each running its own EIGRP ASN, and a Juniper SRX345 in the middle acting as the edge router.

Lab objectives:
- Set up multiple VLANs  
- Configure redundant gateways with HSRP  
- Run EIGRP AS 110 and AS 111  
- Redistribute routes between them  
- Serve DHCP for all VLANs  
- Set up NAT on the edge router  
- Configure NTP  
- Capture HSRP + EIGRP traffic in Wireshark  

All documentation here is my own explanation of how the lab worked.
