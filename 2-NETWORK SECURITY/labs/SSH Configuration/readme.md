# SSH Remote Administration Lab

## Author

**Zainab**

---

# Objective

The objective of this lab is to configure Secure Shell (SSH) on a Cisco router and remotely manage it from an engineer's PC. This simulates how network engineers securely access routers in real enterprise environments.

---

# Lab Scenario

A company has a branch office router that needs to be managed remotely.

Instead of travelling to the branch office, the network engineer uses SSH to securely connect to the router from their own PC.

---

# Topology

```
                Home Office

              My-PC
        192.168.1.10
                  |
                  |
           192.168.1.1
             ISP Router
           172.16.1.1/30
                  |
           172.16.1.2/30
           Company Router
           10.10.10.1/24
                  |
                Switch
          ________|________
         |        |        |
       PC1      PC2     Server
```

---

# IP Addressing

| Device | Interface | IP Address | Subnet Mask |
|----------|-----------|------------|--------------|
| My-PC | FastEthernet0 | 192.168.1.10 | 255.255.255.0 |
| ISP Router | G0/0 | 192.168.1.1 | 255.255.255.0 |
| ISP Router | G0/1 | 172.16.1.1 | 255.255.255.252 |
| Company Router | G0/0 | 172.16.1.2 | 255.255.255.252 |
| Company Router | G0/1 | 10.10.10.1 | 255.255.255.0 |
| PC1 | FastEthernet0 | 10.10.10.10 | 255.255.255.0 |
| PC2 | FastEthernet0 | 10.10.10.20 | 255.255.255.0 |
| Server | FastEthernet0 | 10.10.10.100 | 255.255.255.0 |

---

# Configuration Steps

## Step 1

Configured IP addresses on all PCs, routers, and the server.

---

## Step 2

Enabled all router interfaces using the following command:

```
no shutdown
```

---

## Step 3

Configured static routing between the ISP router and the company router.

ISP Router

```
ip route 10.10.10.0 255.255.255.0 172.16.1.2
```

Company Router

```
ip route 192.168.1.0 255.255.255.0 172.16.1.1
```

---

## Step 4

Verified connectivity using ping.

Successful tests:

- My-PC → ISP Router
- My-PC → Company Router
- My-PC → Company PC
- My-PC → Server

---

## Step 5

Configured SSH on the Company Router.

```
hostname Company-R1

ip domain-name company.local

username admin privilege 15 secret Cisco123

crypto key generate rsa

1024

ip ssh version 2

line vty 0 4

login local

transport input ssh
```

---

## Step 6

Saved the configuration.

```
copy running-config startup-config
```

---

# Remote Login

From My-PC

```
ssh -l admin 10.10.10.1
```

Password

```
Cisco123
```

Successful login prompt

```
Company-R1#
```

---

# Verification Commands

```
show ip interface brief

show ip route

show running-config

show ip ssh

show users
```

---

# Skills Learned

- Network Topology Design
- IP Address Planning
- Router Interface Configuration
- Static Routing
- SSH Configuration
- RSA Key Generation
- Secure Remote Administration
- Remote CLI Access
- Configuration Verification
- Saving Cisco Configurations

---

# Real-World Applications

SSH is widely used by network engineers to securely manage routers and switches without being physically present at the remote site.

Common use cases include:

- Remote router configuration
- Network troubleshooting
- Configuration backup
- Interface monitoring
- Secure device management
- Enterprise network administration

---

# Conclusion

This lab demonstrates how to securely configure SSH on a Cisco router and remotely access it from an engineer's PC. It also introduces basic enterprise network design, static routing, and secure remote administration using Cisco Packet Tracer.