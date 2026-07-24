# Date :23/07/2026
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
<img width="1917" height="1018" alt="Screenshot 2026-07-23 155058" src="https://github.com/user-attachments/assets/50ea9039-ec07-42ee-ab62-bfae0f0a6e7b" />
<img width="1916" height="1007" alt="Screenshot 2026-07-23 155119" src="https://github.com/user-attachments/assets/5888a1e3-4844-41f7-9963-22eaaa2a5b6d" />
<img width="1915" height="1012" alt="Screenshot 2026-07-23 155131" src="https://github.com/user-attachments/assets/793f7b90-f6b2-4864-9b86-8d822b09e5b2" />
<img width="1910" height="1020" alt="Screenshot 2026-07-23 155749" src="https://github.com/user-attachments/assets/934f6268-28d4-42ad-adc2-3b5c581981a1" />
<img width="1917" height="1015" alt="Screenshot 2026-07-23 154959" src="https://github.com/user-attachments/assets/b242dda0-ee00-4e15-a670-1541db8cb4b6" />
<img width="1917" height="1011" alt="Screenshot 2026-07-23 155029" src="https://github.com/user-attachments/assets/db1dbdbc-b506-4314-91b7-f023d43b824e" />


________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

