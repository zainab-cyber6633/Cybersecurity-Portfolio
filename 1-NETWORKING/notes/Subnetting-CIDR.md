# Subnetting & CIDR 
**Author:** Zainab Ijaz 
**Category:** Networking Notes 
**Level:** Begginer to Intermediate 
**Purpose:** Understanding subnetting , subnet mask , and CIDR notation for efficient ip address management .

______
# Introduction 
Subnetting is the process of dividing a large network into smaller , manageable networks  called **subnets**

it improves network performance , enhance security and makes efficient use of ip addresses.

__________

# Why subnetting is important 
Subnetting helps to :

- Reduce network congestion
- Improve network performance
- Increase security
- Organize networks efficiently
- Optimize IP address usage

___________
# what is a subnet ?

A subnet (subnetwork) is a smaller section of a lare IP network .

Example :
________
Original Network :
192.168.1.0/24

Subnets:
192.168.1.0/26
192.168.1.64/26
192.168.1.128/26
192.168.1.192/26
______
 # network ID 
A network ID identifies the network .
Example :
```
 IP Address :
192.168.1.25

subnet mask :
255.255.255.0
Network ID :
192.168.1.0
____________

# host ID 
the host ID identifies a specific device within the network .
Example :
``` 
Network ID :
192.168.1.0

Host:
192.168.1.25
```
________

# Subnet MASK 
a subnet mask separates the ** network ID** from the **host ID**.
common sunet masks:

|CIDR | Subnet mask|
|-----|------------|
| /8 | 255.0.0.0|
|/16 | 255.255.0.0 |
|/24 |255.255.255.0|
|/25 |--------etc |

_______

 # CIDR (classless inter-domain routing )
CIDR is a method of representing subnet mask using a prefix length .
Example :
```
192.168.1.0/24
```
here :
- 24 bits represent the netowrk id 
- 8 bits represent the host id 
__
 # binary basics 
IPv4 addresses are 32 bits long
Example :
``` 
192.168.1.10
Binary:

11000000.10101000.00000001.00001010
```
Subnetting uses binary calculations to divide networks.

________
# Real-World Uses

Subnetting is used in:

- Enterprise networks
- Universities
- Data centers
- Cloud environments
- Internet Service Providers (ISPs)
_________

# Security Importance

Subnetting improves security by:

- Isolating departments
- Reducing broadcast traffic
- Limiting unauthorized access
- Supporting network segmentation

---
# Key Terms

- Network ID
- Host ID
- Subnet
- Subnet Mask
- CIDR
- FLSM
- VLSM
- Broadcast Address
- Default Gateway

---

# Conclusion

Subnetting is an essential networking concept that divides large networks into smaller, more efficient subnets. A strong understanding of subnetting is important for routing, VLANs, network design, troubleshooting, and cybersecurity.

