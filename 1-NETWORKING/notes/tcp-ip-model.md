# TCP/IP Model

**Author:** Zainab  
**Category:** Networking Notes  
**Level:** Beginner  
**Purpose:** Understanding how devices communicate over networks.

---

# Introduction

TCP/IP (Transmission Control Protocol/Internet Protocol) Model is a networking framework used for communication over the Internet and modern computer networks.

It defines how data is transferred between devices using different protocols.

TCP/IP model consists of **4 layers**:

1. Application Layer
2. Transport Layer
3. Internet Layer
4. Network Access Layer


---

# 1. Application Layer

## Function

The Application Layer provides network services directly to user applications.

It combines the functions of OSI:

- Application Layer
- Presentation Layer
- Session Layer


## Common Protocols

### HTTP / HTTPS

Used for accessing websites and secure web communication.

### DNS

Converts domain names into IP addresses.

Example: google.com → IP Address

### FTP

Used for transferring files between systems.

### SMTP

Used for sending emails.

### SSH

Used for secure remote access to devices.


---

# 2. Transport Layer

## Function

The Transport Layer provides communication between applications and ensures data delivery.

Main responsibilities:

- Data segmentation
- Error checking
- Flow control
- Reliable communication


## TCP (Transmission Control Protocol)

TCP is a connection-oriented protocol.

Features:

- Reliable data delivery
- Error checking
- Data retransmission
- Ordered communication


Examples:

- Web browsing
- Email
- File transfer


## UDP (User Datagram Protocol)

UDP is a connectionless protocol.

Features:

- Faster communication
- Low latency
- No retransmission


Examples:

- Online gaming
- Video streaming
- Voice calls


---

# 3. Internet Layer

## Function

The Internet Layer is responsible for logical addressing and routing.

Responsibilities:

- IP addressing
- Packet forwarding
- Route selection


## Protocols

### IP (Internet Protocol)

Provides logical addresses to devices.

Types:

- IPv4
- IPv6


### ICMP

Used for network testing and error reporting.

Example:ping 8.8.8.8



### ARP

Used to find MAC addresses from IP addresses inside a local network.


## Devices

- Router
- Layer 3 Switch


---

# 4. Network Access Layer

## Function

The Network Access Layer handles communication between devices on the same network.

It manages:

- MAC addressing
- Frame transmission
- Physical data transfer


## Technologies

- Ethernet
- Wi-Fi
- Fiber Optic


## Devices

- Switch
- Hub
- Network Interface Card (NIC)


---

# TCP/IP Data Encapsulation

When data moves through TCP/IP layers, information is added at each layer.


Application Data

↓

Segment
(Transport Layer)

↓

Packet
(Internet Layer)

↓

Frame
(Network Access Layer)

↓

Bits


---

# TCP/IP Addressing

## MAC Address

Physical address of a network device.

Example:00:1A:2B:3C:4D:5E



## IP Address

Logical address assigned to a device.

Example:192.168.1.10



## Port Number

Identifies network services and applications.

Examples:
HTTP - 80
HTTPS - 443
SSH - 22
DNS - 53
FTP - 21


---

# TCP/IP Security Importance

TCP/IP knowledge helps cybersecurity professionals in:

- Network traffic analysis
- Packet analysis
- Firewall configuration
- Intrusion detection
- Troubleshooting


---

# OSI vs TCP/IP

| OSI Model | TCP/IP Model |
|---|---|
| 7 Layers | 4 Layers |
| Reference model | Practical model |
| Developed by ISO | Developed by DoD |
| Used for learning | Used in real networks |


---

# Conclusion

TCP/IP Model is the foundation of Internet communication.

Understanding TCP/IP helps in network administration, troubleshooting, and cybersecurity.
