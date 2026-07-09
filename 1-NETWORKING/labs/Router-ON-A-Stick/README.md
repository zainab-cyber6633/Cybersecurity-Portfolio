# Lab  - Router-on-a-Stick (Inter-VLAN Routing)

## Objective

The objective of this lab is to configure VLANs, enable trunking between a Layer 2 switch and a router, and implement Inter-VLAN Routing using the Router-on-a-Stick (ROAS) method.

---

# Topology

```text
                Router
              Gig0/0
                 |
          Trunk Link (802.1Q)
                 |
              Fa0/24
             +---------+
             | Switch  |
             +---------+
      Fa0/1  Fa0/2  Fa0/3  Fa0/4
        |       |       |       |
      PC1     PC2     PC3     PC4
```

---

# Devices Used

- 1 Cisco 2960 Switch
- 1 Cisco Router (1941/2911)
- 4 PCs
- Copper Straight-Through Cables

---

# IP Addressing

| Device | VLAN | IP Address | Subnet Mask | Default Gateway |
|----------|------|----------------|----------------|----------------|
| PC1 | VLAN 10 | 192.168.10.10 | 255.255.255.0 | 192.168.10.1 |
| PC2 | VLAN 10 | 192.168.10.20 | 255.255.255.0 | 192.168.10.1 |
| PC3 | VLAN 20 | 192.168.20.10 | 255.255.255.0 | 192.168.20.1 |
| PC4 | VLAN 20 | 192.168.20.20 | 255.255.255.0 | 192.168.20.1 |

---

# VLAN Configuration

| VLAN ID | Name | Assigned Ports |
|----------|------|----------------|
| 10 | HR | Fa0/1, Fa0/2 |
| 20 | Finance | Fa0/3, Fa0/4 |

---

# Trunk Configuration

| Interface | Mode |
|------------|------|
| Fa0/24 | Trunk |

The trunk link carries traffic for multiple VLANs between the switch and the router using IEEE 802.1Q encapsulation.

---

# Router Configuration

| Subinterface | VLAN | IP Address |
|---------------|------|------------|
| Gig0/0.10 | VLAN 10 | 192.168.10.1/24 |
| Gig0/0.20 | VLAN 20 | 192.168.20.1/24 |

---

# Testing

## Successful Tests

- PC1 → PC2
- PC3 → PC4
- PC1 → PC3
- PC2 → PC4

All devices successfully communicated after configuring Inter-VLAN Routing.

---

# Verification Commands

## Switch

```bash
show vlan brief

show interfaces trunk
```

## Router

```bash
show ip interface brief

show running-config
```

---

# Concepts Learned

- VLAN Creation
- VLAN Assignment
- Access Ports
- Trunk Ports
- IEEE 802.1Q
- Router-on-a-Stick (ROAS)
- Inter-VLAN Routing
- Default Gateway Configuration
- IP Addressing
- Network Segmentation

---

# Key Learning

- VLANs separate broadcast domains.
- Devices in different VLANs cannot communicate without Layer 3 routing.
- Trunk ports allow multiple VLANs to travel over a single physical link.
- Router-on-a-Stick enables communication between VLANs using router subinterfaces.

---

# Conclusion

This lab demonstrates how to configure multiple VLANs on a Layer 2 switch and enable communication between them using Router-on-a-Stick. It also provides practical experience with trunking, VLAN segmentation, and Inter-VLAN Routing, which are fundamental concepts in enterprise networking.
