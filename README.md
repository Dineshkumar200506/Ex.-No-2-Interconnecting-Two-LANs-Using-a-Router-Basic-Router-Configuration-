# Date :23.07.2026
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
(Insert screenshot of your Packet Tracer setup here)<br>
________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output (Screenshots)
<img width="1917" height="1076" alt="Screenshot 2026-07-23 155702" src="https://github.com/user-attachments/assets/242f1fec-fbcf-40e1-b03d-dcc2698fa752" />
<img width="1917" height="1077" alt="Screenshot 2026-07-23 155713" src="https://github.com/user-attachments/assets/e7f76001-c826-4977-8b89-956ff3e401a1" />
<img width="1915" height="1073" alt="Screenshot 2026-07-23 155720" src="https://github.com/user-attachments/assets/7f368693-6326-4372-af9e-ef1b8040fbf3" />
<img width="1917" height="1078" alt="Screenshot 2026-07-23 155650" src="https://github.com/user-attachments/assets/23dcded4-f025-425a-81e6-a56d68def985" />
<img width="1917" height="1073" alt="Screenshot 2026-07-23 155613" src="https://github.com/user-attachments/assets/c3f6b6f4-e656-4b0c-89c5-2714a18644f6" />

________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

