# CodeAlpha Network Sniffer

## 1. Introduction
In modern computer networking and cybersecurity, understanding how data travels across a medium is fundamental to both maintaining network health and detecting malicious activity.A **Network Sniffer** (also known as a packet analyzer) is a tool designed to intercept, capture, and log data packets as they stream across a network interface. 

By capturing raw network traffic, this project delves beneath high-level user interfaces to analyze data at the protocol level. Developing a custom network sniffer provides a practical baseline for understanding how data encapsulation works, how network protocols interact, and how security analysts expose vulnerabilities, clear bottlenecks, or identify unauthorized data transmissions within a network infrastructure.

---

## 2. Project Objectives
The primary goals of developing this network sniffing application include:

* **Real-Time Packet Interception:** Build a functional Python script utilizing low-level libraries (`socket` or `scapy`) capable of binding to a network interface card (NIC) and capturing live, incoming and outgoing IP packets.
***Protocol Analysis & Decoding:** Implement parsing logic to systematically strip down network headers, allowing the application to identify and distinguish between different network and transport layer protocols such as TCP, UDP, and ICMP
* **Metadata Extraction:** Successfully extract and display crucial network metrics from each packet payload, specifically tracking the **Source IP address**, **Destination IP address**, and **Port numbers** to chart the flow of communication.
* **Security & Inspection Awareness:** Evaluate the structural contents of unencrypted payloads to demonstrate the inherent security risks of cleartext protocols (like HTTP, FTP, or DNS), highlighting the critical industry need for robust encryption methods (like HTTPS or TLS).

---

## 3. Environment Setup & Dependencies

### Prerequisites
* **Python:** Version `3.14.5` was utilized for this environment.
* **Scapy Library:** A powerful Python library used for packet capturing and network analysis in cybersecurity projects.

### Installation
The environment was prepared by verifying the Python installation status and installing the `scapy` core module via the command line terminal:


4. Development & Code Structure
Inside Visual Studio Code, a dedicated project workspace was established containing the primary script named sniffer.py.
Implementation Logic (sniffer.py)
The sniff function is imported directly from the scapy.all module space.
A target callback function named packet_callback handles processing for incoming packets, routing their default operational summaries directly to the output console.
The processing packet loop is initialized using the sniff() parameters, configured to automatically stop execution after intercepting a fixed ceiling of 20 consecutive packets.
from scapy.all import sniff

5. Execution & Live Traffic Capture
To deploy the tool and begin logging network data, execute the file directly through your integrated terminal environment:
python sniffer.py
Telemetry Analysis
Upon deployment, the custom script binds successfully to the machine's active network interfaces, intercepting live runtime traffic streams and parsing them dynamically:
Captured Protocol Varieties: The terminal monitor successfully reads encrypted HTTPS handshakes and fundamental transport-layer TCP transactions.
Metric Extraction: The application actively registers the internal addressing framework, mapping out Source IP addresses, Destination IP addresses, and relative host connection ports.
Live Infrastructure Insights: The ongoing logs reflect real-world, background communication strings processing across the adapter simultaneously while web browsing or running active network applications
