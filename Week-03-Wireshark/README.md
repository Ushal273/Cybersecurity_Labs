# Week 3 – Wireshark: The Basics

## Objective
Learn how to analyse network traffic using Wireshark.

---

## What is Wireshark?
Wireshark is a free, open-source network protocol analyser used to capture and inspect packets of data travelling across a network. It is widely used by cybersecurity professionals for network troubleshooting and threat detection.

---

## Key Concepts

### Packets
Every internet communication is broken into packets.
Example flow: Open Google → DNS → TCP → HTTPS → Webpage

### Important Packet Fields
- Source IP – where the packet came from
- Destination IP – where it is going
- Protocol – HTTP, DNS, TCP, UDP
- Packet Length – size of the packet
- Timestamp – when it was captured

---

## HTTP vs HTTPS
- HTTP – Unencrypted. Content can be read in Wireshark.
- HTTPS – Encrypted. Content cannot be read.

---

## Useful Wireshark Filters
- http
- tcp
- udp
- dns
- ip.addr==192.168.1.5

---

## Key Takeaways
Wireshark allows analysts to inspect network traffic in real time. Understanding packet structure and filters is a fundamental skill for SOC analysts when investigating suspicious network activity.


---

## Screenshots

