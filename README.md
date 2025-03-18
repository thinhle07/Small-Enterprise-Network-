# Small-Enterprise-Network-
This Cisco Packet Tracer project simulates a secure small business network for 25 employees, featuring VLAN segmentation (Sales and IT), wireless access, NAT for internet connectivity, and STP redundancy. It includes ACL-enforced security and supports wired and wireless segments with reliable external access.

## Scenario
This project simulates a small business network in Cisco Packet Tracer, supporting 25 employees across Sales and IT departments. It uses VLANs, wireless access, NAT, and STP for a secure, redundant design with ACLs and external connectivity.

## Network Diagram
![Network_Diagram](https://github.com/user-attachments/assets/2ed8b183-bda3-4067-a18b-e723ffb8755e)

## Key Features
- VLAN Segmentation: Three VLANs (Sales-Wired: 192.168.10.0/24, Sales-Wireless: 192.168.15.0/24, IT: 192.168.20.0/24) for department isolation and traffic management.
- Inter-VLAN Routing: Configured on a Cisco 2911 router using subinterfaces for seamless communication.
- Wireless Access: WPA2-PSK secured wireless network (SSID: "Sales-Mobile") for Sales department mobility.
- DHCP: Centralized IP assignment on the router for all VLANs, simplifying device management.
- NAT: Translates internal private IPs to a public IP (203.0.113.1) for internet connectivity, tested with an external PC simulating the internet.
- Security: Standard ACL blocks IT-to-Sales traffic while permitting other flows, enhancing network control.
- Redundancy: Spanning Tree Protocol (STP) between two Cisco 2960 switches ensures fault tolerance with a backup link.

## Topology
- Devices: 1 Router (Cisco 2911), 2 Switches (Cisco 2960), 1 Wireless Access Point, 5 PCs (end devices), 1 PC (simulating internet).
- Connections: Trunks for VLAN traffic, access ports for endpoints, and a redundant switch link.

## Usage
- Open the .pkt file in Cisco Packet Tracer (version 8.0 or later recommended).
- Test connectivity:
    - Intra-VLAN pings (e.g., Sales-Wired PC1 to PC2).
    - Inter-VLAN pings (e.g., Sales to IT, blocked in reverse by ACL).
    - NAT to internet (ping 203.0.113.2 from any internal PC).
- Verify configurations with show commands (e.g., show ip nat translations, show vlan brief, show spanning-tree) or check the running_config folder.
