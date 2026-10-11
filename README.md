Linux Network Traffic Analysis

Objective

Investigate Ubuntu network configuration, test gateway connectivity, and capture ICMP traffic using tcpdump

Tools
- Ubuntu Linux
- ip, ss, ping, tcpdump

Findings
- VM IP: 10.0.2.15
- Default gateway: 10.0.2.2
- Captured 8 ICMP packets: 4 request and 4 replies.
- Ping test completed with 0% packet loss.
- Saved capture: captures/gateway-icmp.pcap

Conclusion

The investigation established a baseline for expected network communication and demonstrated basic packet capture and analysis.
Gateway reachability does not guarantee that every network service is accessible or that the network is threat-free

Evidence
- documentation/investigation-notes.md
- captures/gateway-icmp.pcap

