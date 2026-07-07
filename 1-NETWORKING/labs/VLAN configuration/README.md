# Lab 03 - VLAN Configuration 

## Objective
Configure multiple VLANs on a Cisco switch and enable communication between VLANs using Router-on-a-Stick.

## Topology
- 1 Cisco 2911 Router
- 1 Cisco 2960 Switch
- 3 PCs

## VLAN Configuration
- VLAN 10
- VLAN 20
- VLAN 30

## IP Addressing
| Device | VLAN | IP Address | Default Gateway |
|--------|------|------------|-----------------|
| PC1 | VLAN 10 | 192.168.10.10 | 192.168.10.1 |
| PC2 | VLAN 20 | 192.168.20.10 | 192.168.20.1 |
| PC3 | VLAN 30 | 192.168.30.10 | 192.168.30.1 |

## Tasks Performed
- Created VLAN 10, VLAN 20, and VLAN 30.
- Assigned switch ports to the appropriate VLANs.
- Configured the trunk port between the switch and the router.
- Configured Router-on-a-Stick using subinterfaces.
- Assigned IP addresses to router subinterfaces.
- Configured default gateways on all PCs.
- Verified connectivity using ping.

## Skills Practiced
- VLAN Creation
- Port Assignment
- Trunk Configuration
- Router-on-a-Stick
- Inter-VLAN Routing
- IP Addressing
- Network Troubleshooting

## Verification Commands
show vlan brief
show interfaces trunk
show ip interface brief
show running-config
show ip route

## Result
Successfully configured three VLANs and enabled communication between them using Router-on-a-Stick.

## Author
Zainab Ijaz