Linux Network Traffic Analysis
1. Objective
Investigate basic network configuration and capture controlled network traffic from an Ubuntu virtual machine 

2. Lab Enviroment
- OS: Ubuntu 26.04.1 LTS
- Hostname: soc-lab
- Interface: enp0s8
- VM IP: 10.0.2.15
- Gateway: 10.0.2.2
- Tool: tcpdump

3. Investigation Steps
- Inspected network interfaces using ip -r addr.
- Reviewed routing information using ip route
- Inspected network socket using ss -tunap.
- Tested gateway connectivity using ping -c 4 10.0.2.2.
- Captured ICMP packets using tcpdump
- Saved the capture as captures/gateway-icmp.pcap.
- Read the saved packets using tcpdump.

4. Findings
- VM address: 10.0.2.15.
- Default gatewway: 10.0.2.2
- Ping received 4 replies with 0% packet loss.
- Captured 8 packets: 4 ICMP echo requests and 4 echo replies.
- Requests travelled from the VM to the gateway.
- Replies travelled from the gateway back to the VM.
- Each displayed ICMP message had a reported length of 64 bytes.
- The saved capture file was approximately 936 bytes.

5. Analysis
- The VM successfully communicated with its default gateway.
- The four ICMP echo requests received four corresponding replies.
- No packet loss was observed during the controlled ping test.
- The capture showed expected request-and-reply traffic.
- This test confirms gateway reachablitity at the time of testing; it does not prove that every network service is accessible or that the network is free from threats.

6. Conclusion
The Investigation successfully documented the Ubuntu VM network configuration and captured controlled ICMP traffic between the VM and its default gateway.
The packet capture contained four echo requests and four corresponding replies, with no packet loss observed in the ping test. This exercise established a 
baseline for recognizing expected network communication and demostrated how tcpdump can capture and inspect packets for futher investigation.

7. Project Files
- README.md: Project overview, objectives, and key findings.
- documentation/investigation-notes.md: Detailed investigation notes.
- captures/gateway-icmp.pcap: Saved ICMP packet capture.

