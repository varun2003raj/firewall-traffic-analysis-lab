# Firewall Traffic Analysis Lab

This lab demonstrates how network traffic can be generated, captured, and analyzed to observe scanning behavior and investigate network communication.

## 1. Network Device Discovery
![Network Discovery](01_network_device_discovery_glasswire.png)

GlassWire was used to identify active devices on the network.

## 2. Target System Identification
![Windows IP](02_windows_ipconfig_target.png)

The target system IP address was identified using Windows `ipconfig`.

## 3. Attacker Machine Identification
![Kali IP](03_kali_ifconfig_attacker.png)

The attacker machine IP address was confirmed using Kali `ifconfig`.

## 4. Connectivity Test
![Ping Test](04_ping_connectivity_test.png)

Connectivity to the target host was verified using:
ping 192.168.29.172


## 5. Port Scanning
![Nmap Scan](05_nmap_port_scan.png)

A SYN scan was performed to identify open ports.


sudo nmap -sS 192.168.29.172


## 6. Packet Capture
![tcpdump Capture](06_tcpdump_packet_capture.png)

Network traffic was captured using tcpdump.


sudo tcpdump -i any host 192.168.29.172


## 7. Traffic Analysis
![Traffic Analysis](07_tcpdump_traffic_analysis_grep.png)

Captured packets were filtered to analyze communication patterns.


grep "192.168.29.172" traffic.txt


## Result

The analysis revealed SYN packets generated during the Nmap scan and ARP
