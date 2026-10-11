# Linux Network Traffic Analysis

## Project Overview
This project investigates network configuration and captures controlled network traffic from an Ubuntu virtual machine using tcpdump.

## Objectives
- Identify the VM's network interface, IP address, and default gateway.
- Inspect active network sockets and listening ports.
- Test connectivity to the default gateway.
- Capture and analyze ICMP packets.

## Tools Used
- Ubuntu Linux
- ip
- ss
- ping
- tcpdump

## Key Findings
- VM IP address: 10.0.2.15
- Default gateway: 10.0.2.2
- Four ICMP echo requests and four replies were captured.
- The controlled ping test showed 0% packet loss.
- The capture contained eight packets and was saved as `captures/gateway-icmp.pcap`.

## Project Files
- `documentation/investigation-notes.md` — Investigation steps, findings, analysis, and conclusion.
- `captures/gateway-icmp.pcap` — Saved packet capture.

## Conclusion
The investigation established a baseline for expected network communication between the Ubuntu VM and its default gateway. It demonstrated how to inspect network configuration, test connectivity, and capture packets using tcpdump.

This test confirms gateway reachability at the time of testing. It does not establish that every network service is accessible or that the network is free from threats.
