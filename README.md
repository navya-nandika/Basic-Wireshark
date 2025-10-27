**Capture and Analyze Network Traffic Using Wireshark**

*Objective:*

To capture live network packets using Wireshark, analyze them, and identify basic network protocols such as HTTP, DNS, TCP.

*Tools Used:*

Wireshark (installed inside Kali Linux running on VMware Workstation)

Operating System: Kali Linux (Guest VM)

Virtualization Software: VMware Workstation / VMware Player

*Setup Steps:*

1.Installed Wireshark in Kali Linux using:

sudo apt update
sudo apt install wireshark -y


2.Allowed non-root users to capture packets:

sudo dpkg-reconfigure wireshark-common
sudo usermod -aG wireshark $USER (user - navya here)


3.(Then logged out and back in.)

4.Started Wireshark and selected the active interface eth0.

Generated traffic by:

# Visiting websites (e.g.,  google.com) -> from firefox

# Running websites from google terminal

# Stopped the capture after about 1 minute.

Applied filters to analyze traffic by protocol:

http → View HTTP packets -> Web communication

dns → View DNS queries -> domain name resolution

tcp / udp → View transport layer traffic -> web communication

Exported capture as TASK5.pcap.

*HTTP:*

<img width="1280" height="537" alt="image" src="https://github.com/user-attachments/assets/d41fd594-d1e0-4b25-9dfa-b391d370da93" />

*DNS:*

<img width="1681" height="625" alt="image" src="https://github.com/user-attachments/assets/08490619-832a-4147-8323-d59629f8aa7f" />

*TCP:*

<img width="1689" height="555" alt="image" src="https://github.com/user-attachments/assets/49fe5a2e-3f36-4a25-9514-76821c0a5dcd" />

QUesttions: 


1.What is Wireshark used for? 

Wireshark is a network protocol analyzer used to capture, inspect, and analyze network traffic in real time. It helps identify what data is flowing through the network, which protocols are being used, and can diagnose network issues or detect suspicious activity.


2.What is a packet? 

A packet is a small unit of data transmitted over a network. It contains a header (with routing and protocol information) and a payload (the actual data being sent). Networks transfer data in packets so it can be efficiently sent and reassembled at the destination.


3.How to filter packets in Wireshark? 

Wireshark provides a display filter bar at the top. You can filter packets by typing protocol names or expressions such as http, dns, tcp, or icmp.


4.What is the difference between TCP and UDP? 

TCP (Transmission Control Protocol) is connection-oriented, ensures reliable delivery, and uses acknowledgments and retransmissions. UDP (User Datagram Protocol) is connectionless, faster, but does not guarantee delivery or order.


5.What is a DNS query packet? 

A DNS query packet is sent from a client to a DNS server to resolve a domain name (like google.com) into its corresponding IP address.


6.How can packet capture help in troubleshooting? 

Packet capture helps identify where communication is failing, detect latency, dropped packets, misconfigurations, or malicious traffic by showing what is actually being transmitted across the network.


7.What is a protocol? 

A protocol is a set of rules that define how data is transmitted and received over a network, ensuring devices communicate correctly (e.g., TCP, HTTP, DNS).


8.Can Wireshark decrypt encrypted traffic? 

Wireshark cannot normally decrypt encrypted traffic like HTTPS or SSH unless you have the appropriate decryption keys or use specific debugging setups that provide session keys.


*Author : Navya Nandika*

*Date: October 27, 2025*
