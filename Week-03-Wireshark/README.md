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

<img width="959" height="422" alt="image" src="https://github.com/user-attachments/assets/106ce2a8-8870-48d5-9e27-bcca5351df44" />

<img width="959" height="248" alt="image" src="https://github.com/user-attachments/assets/e44ef2ef-001c-43a2-b873-ec2383d3c9c4" />

<img width="952" height="240" alt="image" src="https://github.com/user-attachments/assets/a06ad852-00f9-45e8-bb08-cfe0d491fa12" />


<img width="959" height="277" alt="image" src="https://github.com/user-attachments/assets/9089db0f-3d28-49ef-ab10-edbb2b35ff75" />




