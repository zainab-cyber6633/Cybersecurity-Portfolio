# OSI Model

## Overview

The Open Systems Interconnection (OSI) Model is a conceptual framework developed by the International Organization for Standardization (ISO). It describes how data travels from one device to another through seven different layers.

The OSI Model helps network engineers and cybersecurity professionals understand how communication works and where network problems occur.

---

# Learning Objectives

After completing this topic, you will be able to:

* Define the OSI Model.
* Explain the purpose of each OSI layer.
* Identify protocols and devices used at each layer.
* Understand the data flow through the OSI Model.
* Troubleshoot network issues using the OSI Model.

---

# What is the OSI Model?

The OSI Model divides network communication into seven layers. Each layer performs a specific function and communicates with the layer directly above and below it.

This layered approach makes networking easier to understand, troubleshoot, and develop.

---

# The Seven Layers of the OSI Model

| Layer Number | Layer Name   | Main Function                                   |
| ------------ | ------------ | ----------------------------------------------- |
| 7            | Application  | Provides network services to users              |
| 6            | Presentation | Data formatting and encryption                  |
| 5            | Session      | Establishes and manages communication sessions  |
| 4            | Transport    | Reliable data delivery                          |
| 3            | Network      | Logical addressing and routing                  |
| 2            | Data Link    | Physical addressing and error detection         |
| 1            | Physical     | Transmits data through cables or wireless media |

---

# Layer 7 – Application Layer

## Purpose

The Application Layer provides network services directly to end users and applications.

It is the layer where users interact with the network.

## Common Protocols

* HTTP
* HTTPS
* FTP
* SMTP
* POP3
* IMAP
* DNS

## Examples

* Opening a website
* Sending an email
* Downloading a file

---

# Layer 6 – Presentation Layer

## Purpose

The Presentation Layer prepares data before it is sent to the Application Layer.

It is responsible for:

* Data Translation
* Data Encryption
* Data Decryption
* Data Compression

## Examples

* SSL/TLS Encryption
* JPEG Images
* PNG Images
* MP4 Videos

---

# Layer 5 – Session Layer

## Purpose

The Session Layer establishes, manages, and terminates communication sessions between devices.

Functions include:

* Session Establishment
* Session Maintenance
* Session Termination

Example:

A video meeting remains connected until one participant ends the session.

---

# Layer 4 – Transport Layer

## Purpose

The Transport Layer ensures reliable communication between sender and receiver.

Functions include:

* Segmentation
* Flow Control
* Error Recovery
* Reliable Delivery

## Protocols

* TCP
* UDP

TCP provides reliable communication.

UDP provides faster communication with less overhead.

---

# Layer 3 – Network Layer

## Purpose

The Network Layer determines the best path for data to travel between networks.

Functions include:

* Logical Addressing
* Routing
* Path Selection

## Protocols

* IP
* ICMP
* OSPF
* RIP

## Device

Router

---

# Layer 2 – Data Link Layer

## Purpose

The Data Link Layer transfers data between devices on the same network.

Functions include:

* Physical Addressing
* Error Detection
* Frame Delivery

## Protocols

* Ethernet
* PPP

## Device

Switch

---

# Layer 1 – Physical Layer

## Purpose

The Physical Layer transmits binary data through physical media.

Functions include:

* Electrical Signals
* Optical Signals
* Radio Signals
* Cabling

## Devices

* Hub
* Repeater
* Cable
* Connector

---

# Data Encapsulation

When data is transmitted, each OSI layer adds its own header.

The process is called Encapsulation.

When the receiver receives the data, each layer removes its corresponding header.

This process is called De-encapsulation.

---

# PDU (Protocol Data Unit)

| Layer        | PDU     |
| ------------ | ------- |
| Application  | Data    |
| Presentation | Data    |
| Session      | Data    |
| Transport    | Segment |
| Network      | Packet  |
| Data Link    | Frame   |
| Physical     | Bits    |

---

# Memory Trick

To remember the layers from top to bottom:

**All People Seem To Need Data Processing**

* Application
* Presentation
* Session
* Transport
* Network
* Data Link
* Physical

---

# Real-World Example

When you open a website:

1. Application Layer creates the HTTP request.
2. Presentation Layer encrypts the data using HTTPS.
3. Session Layer manages the communication session.
4. Transport Layer adds TCP information.
5. Network Layer adds the IP address.
6. Data Link Layer adds the MAC address.
7. Physical Layer sends the bits through the network cable or Wi-Fi.

The receiving device performs the reverse process.

---

# Advantages of the OSI Model

* Simplifies networking concepts.
* Makes troubleshooting easier.
* Standardizes communication.
* Supports interoperability between different vendors.
* Helps network design and implementation.

---

# Interview Questions

### What is the OSI Model?

The OSI Model is a seven-layer conceptual framework used to explain how network communication occurs between devices.

### Which layer is responsible for routing?

The Network Layer (Layer 3).

### Which device works at Layer 2?

A Switch.

### Which device works at Layer 3?

A Router.

### Which protocol is used for reliable communication?

TCP.

### Which layer is responsible for encryption?

Presentation Layer.

---

# Summary

* The OSI Model has seven layers.
* Each layer performs a specific networking function.
* Layer 3 is responsible for routing.
* Layer 2 handles MAC addresses and switching.
* Layer 4 provides reliable communication using TCP.
* Understanding the OSI Model is essential for networking and cybersecurity professionals.

---

# References

* Cisco Networking Academy
* CompTIA Network+
* Microsoft Learn
* RFC Documentation

---

## Author: Zainab Ijaz
