VLANs 

Here’s the basic VLAN layout that was used:

| VLAN | Subnet | Purpose | HSRP VIP |
|------|--------|---------|----------|
| 1101 | 10.1.1.0/24 | Clients | 10.11.1.254 |
| 1102 | 10.1.2.0/24 | Clients | 10.11.2.254 |
| 1103 | 10.1.3.0/24 | Clients | 10.11.3.254 |
| 1104 | 10.1.4.0/24 | Clients | 10.11.4.254 |
| Native | 10.1.7.0/24 | Trunk native VLAN | 10.0.5.254|

Every VLAN SVI on the routers participates in HSRP.

The internal network runs on 10.1.0.0/24 (IPs assigned to invidual interfaces to ping throughout the internal network).
