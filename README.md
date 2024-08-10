# Pulchowk Campus Network Design

This repository contains the comprehensive network design for Pulchowk Campus, including DNS, IP addressing, routing protocols, and essential network services. The design is structured to be scalable, secure, and efficient, meeting the needs of the campus community.

## Table of Contents

1. [Introduction](#introduction)
2. [Network Architecture and Design](#network-architecture-and-design)
3. [DNS and IP Addressing](#dns-and-ip-addressing)
4. [Routing Protocols and Routing Tables](#routing-protocols-and-routing-tables)
5. [Network Services](#network-services)
6. [Web Hosting and Domain Management](#web-hosting-and-domain-management)
7. [Network Components](#network-components)
8. [Conclusion](#conclusion)

## Introduction

### Overview of Computer Networks
Computer networks are the backbone of modern communication systems, enabling the sharing of resources and information across various devices and platforms.

### Objective of the Mini Project
The objective of this project is to design and implement a robust and scalable network for Pulchowk Campus.

## Network Architecture and Design

### Network Topology Overview
The network topology of Pulchowk Campus is structured to provide efficient and reliable connectivity across different departments and buildings.

![Area_Network](https://github.com/user-attachments/assets/6b6339da-09fd-493c-bca4-4efa73b5adbf)

### Hierarchical Network Design
The network is designed hierarchically to optimize routing and improve scalability.

![router-hierarchy](https://github.com/user-attachments/assets/57078014-9cf4-4007-adfb-35e58d671435)

### Network Diagram
Here is the overall network diagram that provides a visual representation of the Pulchowk Campus network design.

![network](https://github.com/user-attachments/assets/ee00441f-6d38-4f39-9aae-775e7881f684)


### Types of Networks
Pulchowk Campus network consists of various types of networks like LAN, WAN, etc., focusing primarily on the LAN.

## Network Components

The Pulchowk Campus Network is composed of the following components:

- **35 Routers**
- **19 DHCP Servers**
- **4 DNS Servers**
- **7 Web Servers**
- **45 Router-to-Router Connections**

## DNS and IP Addressing

### DNS Hierarchy and Servers
The DNS hierarchy within Pulchowk Campus is structured to ensure efficient domain name resolution.

- **NTC**
  - DNS Server: 202.70.64.5
- **Pulchowk Campus**
  - DNS Server: 10.100.1.3 (Area O CIT)
  - ABR 1 DNS Server: 10.100.6.5 (Civil)
  - ABR 2 DNS Server: 10.100.2.5 (DOECE)
  - ABR 3 DNS Server: 10.100.9.4 (White House)

![DNS Hierarchy](https://github.com/user-attachments/assets/81274e0b-fdb4-4d66-ae71-c74ce4c5ddf4)

### DNS Cache and Resolution Process
The DNS cache is crucial for speeding up the domain name resolution process by storing previously resolved queries.

![abr1_dns_cache](https://github.com/user-attachments/assets/4e1b731f-0393-41f9-8897-d37250924773)

### IP Address Allocation and Management
IP addresses are allocated across different areas and servers in the network to ensure organized address management and prevent conflicts.

#### Subnet Allocation Table

| Subnet         | Subnet Mask     | IP Range                    | Broadcast Address  |
|----------------|-----------------|-----------------------------|--------------------|
| **ABR-0: CIT Router** |                 |                             |                    |
| CIT            | 255.255.255.0   | 10.100.1.1 - 10.100.1.254    | 10.100.1.255       |
| **ABR-1: Departments** |                 |                             |                    |
| Civil          | 255.255.254.0   | 10.100.2.1 - 10.100.3.254    | 10.100.3.255       |
| AeroSpace      | 255.255.255.128 | 10.100.4.1 - 10.100.4.126    | 10.100.4.127       |
| Mechanical     | 255.255.255.0   | 10.100.4.129 - 10.100.4.254  | 10.100.4.255       |
| Chemical       | 255.255.255.128 | 10.100.5.1 - 10.100.5.126    | 10.100.5.127       |
| **ABR-2: Departments** |                 |                             |                    |
| DOECE          | 255.255.254.0   | 10.100.6.1 - 10.100.7.254    | 10.100.7.255       |
| Electrical     | 255.255.255.0   | 10.100.8.1 - 10.100.8.254    | 10.100.8.255       |
| **ABR-3: Departments** |                 |                             |                    |
| White House    | 255.255.255.0   | 10.100.9.1 - 10.100.9.254    | 10.100.9.255       |
| Architecture   | 255.255.254.0   | 10.100.10.1 - 10.100.11.254  | 10.100.11.255      |
| MSC Hostel     | 255.255.255.128 | 10.100.12.1 - 10.100.12.126  | 10.100.12.127      |
| Account        | 255.255.255.192 | 10.100.12.129 - 10.100.12.190| 10.100.12.191      |
| Administration | 255.255.255.192 | 10.100.12.193 - 10.100.12.254| 10.100.12.255      |
| **ABR-4: Miscellaneous** |                 |                             |                    |
| Library        | 255.255.255.192 | 10.100.13.1 - 10.100.13.62   | 10.100.13.63       |
| CIT Lab        | 255.255.255.192 | 10.100.13.65 - 10.100.13.126 | 10.100.13.127      |
| Pulchowk Club  | 255.255.255.192 | 10.100.13.129 - 10.100.13.190| 10.100.13.191      |
| Canteen        | 255.255.255.192 | 10.100.13.193 - 10.100.13.254| 10.100.13.255      |
| **ABR-5: Residences** |                 |                             |                    |
| Girls Hostel   | 255.255.255.0   | 10.100.16.1 - 10.100.16.254  | 10.100.16.255      |
| Staff Quarter  | 255.255.254.0   | 10.100.14.1 - 10.100.15.254  | 10.100.15.255      |
| Boys Hostel Block A | 255.255.255.0 | 10.100.17.1 - 10.100.17.254  | 10.100.17.255      |
| Boys Hostel Block B | 255.255.255.0 | 10.100.18.1 - 10.100.18.254  | 10.100.18.255      |
| Boys Hostel Block C | 255.255.255.0 | 10.100.19.1 - 10.100.19.254  | 10.100.19.255      |

#### Router to Router IP Allocation Table

| Connection                           | Subnet Mask     | IP Range                  | Gateway IP        |
|--------------------------------------|-----------------|---------------------------|-------------------|
| CIT Router to ABR 1                  | 255.255.255.252 | 10.100.31.1 - 10.100.31.2  | 10.100.31.3       |
| CIT Router to ABR 2                  | 255.255.255.252 | 10.100.31.5 - 10.100.31.6  | 10.100.31.7       |
| CIT Router to ABR 3                  | 255.255.255.252 | 10.100.31.9 - 10.100.31.10 | 10.100.31.11      |
| CIT Router to ABR 4                  | 255.255.255.252 | 10.100.31.13 - 10.100.31.14| 10.100.31.15      |
| CIT Router to ABR 5                  | 255.255.255.252 | 10.100.31.17 - 10.100.31.18| 10.100.31.19      |
| ABR 1 to ABR 2                       | 255.255.255.252 | 10.100.31.21 - 10.100.31.22| 10.100.31.23      |
| ABR 2 to ABR 3                       | 255.255.255.252 | 10.100.31.25 - 10.100.31.26| 10.100.31.27      |
| ABR 3 to ABR 4                       | 255.255.255.252 | 10.100.31.29 - 10.100.31.30| 10.100.31.31      |
| ABR 4 to ABR 5                       | 255.255.255.252 | 10.100.31.33 - 10.100.31.34| 10.100.31.35      |
| ABR 5 to ABR 1                       | 255.255.255.252 | 10.100.31.37 - 10.100.31.38| 10.100.31.39      |
| ABR 1 to ABR 1.1                     | 255.255.255.252 | 10.100.31.41 - 10.100.31.42| 10.100.31.43      |
| ABR 1.1 to ABR 1.2                   | 255.255.255.252 | 10.100.31.45 - 10.100.31.46| 10.100.31.47      |
| ABR 1 to ABR 1.2                     | 255.255.255.252 | 10.100.31.49 - 10.100.31.50| 10.100.31.51      |
| ABR 1 to Chem                        | 255.255.255.252 | 10.100.31.53 - 10.100.31.54| 10.100.31.55      |
| ABR 1 to Aero                        | 255.255.255.252 | 10.100.31.57 - 10.100.31.58| 10.100.31.59      |
| ABR 1 to Mech                        | 255.255.255.252 | 10.100.31.61 - 10.100.31.62| 10.100.31.63      |
| ABR 1 to Civil                       | 255.255.255.252 | 10.100.31.65 - 10.100.31.66| 10.100.31.67      |
| ABR 2 to ABR 2.1                     | 255.255.255.252 | 10.100.31.69 - 10.100.31.70| 10.100.31.71      |
| ABR 2 to ABR 2.2                     | 255.255.255.252 | 10.100.31.73 - 10.100.31.74| 10.100.31.75      |
| ABR 2.2 to ABR 2.1                   | 255.255.255.252 | 10.100.31.77 - 10.100.31.78| 10.100.31.79      |
| ABR 2 to DOECE                       | 255.255.255.252 | 10.100.31.81 - 10.100.31.82| 10.100.31.83      |
| ABR 2 to Electrical                  | 255.255.255.252 | 10.100.31.85 - 10.100.31.86| 10.100.31.87      |
| ABR 3 to Arch                        | 255.255.255.252 | 10.100.31.89 - 10.100.31.90| 10.100.31.91      |
| ABR 3 to Account                     | 255.255.255.252 | 10.100.31.93 - 10.100.31.94| 10.100.31.95      |
| ABR 3 to Msc Hostel                  | 255.255.255.252 | 10.100.31.97 - 10.100.31.98| 10.100.31.99      |
| ABR 3 to White House                 | 255.255.255.252 | 10.100.31.101 - 10.100.31.102| 10.100.31.103  |
| ABR 3 to Administration              | 255.255.255.252 | 10.100.31.105 - 10.100.31.106| 10.100.31.107  |
| ABR 3 to ABR 3.2                     | 255.255.255.252 | 10.100.31.109 - 10.100.31.110| 10.100.31.111  |
| ABR 3.1 to ABR 3.2                   | 255.255.255.252 | 10.100.31.113 - 10.100.31.114| 10.100.31.115  |
| ABR 3 to ABR 3.1                     | 255.255.255.252 | 10.100.31.117 - 10.100.31.118| 10.100.31.119  |
| ABR 4 to Canteen                     | 255.255.255.252 | 10.100.31.121 - 10.100.31.122| 10.100.31.123  |
| ABR 4 to Pulchowk Club               | 255.255.255.252 | 10.100.31.125 - 10.100.31.126| 10.100.31.127  |
| ABR 4 to Library                     | 255.255.255.252 | 10.100.31.129 - 10.100.31.130| 10.100.31.131  |
| ABR 4 to CIT Lab                     | 255.255.255.252 | 10.100.31.133 - 10.100.31.134| 10.100.31.135  |
| ABR 4 to ABR 4.1                     | 255.255.255.252 | 10.100.31.137 - 10.100.31.138| 10.100.31.139  |
| ABR 4 to ABR 4.2                     | 255.255.255.252 | 10.100.31.141 - 10.100.31.142| 10.100.31.143  |
| ABR 4.2 to ABR 4.1                   | 255.255.255.252 | 10.100.31.145 - 10.100.31.146| 10.100.31.147  |
| ABR 5 to Boys Hostel                 | 255.255.255.252 | 10.100.31.149 - 10.100.31.150| 10.100.31.151  |
| ABR 5 to Girls Hostel                | 255.255.255.252 | 10.100.31.153 - 10.100.31.154| 10.100.31.155  |
| ABR 5 to Staff Quarter               | 255.255.255.252 | 10.100.31.157 - 10.100.31.158| 10.100.31.159  |
| ABR 5 to ABR 5.1                     | 255.255.255.252 | 10.100.31.161 - 10.100.31.162| 10.100.31.163  |
| ABR 5 to ABR 5.2                     | 255.255.255.252 | 10.100.31.165 - 10.100.31.166| 10.100.31.167  |
| ABR 5.1 to ABR 5.2                   | 255.255.255.252 | 10.100.31.169 - 10.100.31.170| 10.100.31.171  |
| CIT Router to CIT Secondary Router   | 255.255.255.252 | 10.100.31.173 - 10.100.31.174| 10.100.31.175  |
| CIT Router to ISP Router             | 255.255.255.252 | 10.100.0.1 - 10.100.0.2    | 10.100.0.3       |


### DHCP Servers
DHCP servers dynamically assign IP addresses to devices within the network.

- **CIT**: 10.100.1.2
- **Chemical**: 10.100.4.132
- **Mechanical**: 10.100.5.2
- **Aerospace**: 10.100.4.2
- **Civil**: 10.100.2.2
- **DOECE**: 10.100.6.2
- **Electrical**: 10.100.8.2
- **Architecture**: 10.100.10.2
- **White House**: 10.100.9.2
- **MSc Hostel**: 10.100.12.2
- **Account**: 10.100.12.130
- **Administration**: 10.100.12.194
- **Canteen**: 10.100.13.194
- **Library**: 10.100.13.2
- **Pulchowk Club**: 10.100.13.130
- **CIT Lab**: 10.100.13.66
- **Girls Hostel**: 10.100.4.132
- **Boys Hostel**: 10.100.19.2 (VLAN 30)
- **Staff Quarter**: 10.100.14.2

## Routing Protocols and Routing Tables

### Router Routing Tables
Router routing tables are crucial for determining the best path for data to travel across the network.

![cit_router_routing_table](https://github.com/user-attachments/assets/4a4c04a6-06e1-4320-b9d7-c831538c97c4)

### BGP Routing Between CIT and ISP Router
BGP is used to manage the exchange of routing information between the Pulchowk Campus (CIT) Router and Nepal Telecom’s ISP infrastructure.

![isp_routing_table](https://github.com/user-attachments/assets/c5f15333-6bd0-4ca6-8c2c-c3a66561aead)

### Multipath Routing Techniques
Multipath routing enhances network resilience by providing multiple paths for data to travel.

![multi_path_routing](https://github.com/user-attachments/assets/767b3da4-1478-483d-846b-7321bf621acf)

### Inter-Area Routing and Testing
Inter-area routing is essential for maintaining connectivity between different areas within the campus network.

![inter_area_ping_test](https://github.com/user-attachments/assets/7f2529f4-37d7-4ad8-836d-1799d9e1e435)

## Network Services

### DHCP Operation and Configuration
The DHCP server dynamically assigns IP addresses to devices within the network.

![dhcp-request](https://github.com/user-attachments/assets/9b218e68-aae9-4931-9953-97b4453eef8a)

### Telnet and Remote Access
Telnet is used for remote management of routers and switches within the campus network.

![telnet](https://github.com/user-attachments/assets/f581c61f-bf07-4299-9879-d151f91f20df)

### Traceroute and Network Diagnostics
Traceroute is a network diagnostic tool used to trace the path that data takes from the source to the destination.

![traceroute_valid](https://github.com/user-attachments/assets/53d82476-a8ac-46c3-a6a4-cc361baea5cd)

## Web Hosting and Domain Management

### Website Hosting Overview
The network includes web hosting services for the campus’s official websites.

- **ISP**
  - www.ntc.net.np: 202.70.64.10
  - www.susheelthapa.com.np: 202.70.64.11
- **Pulchowk Campus**
  - www.civil.pcampus.edu.np: 10.100.2.6
  - www.chemical.pcampus.edu.np: 10.100.4.132
  - www.aero.edu.np: 10.100.4.4
  - www.electrical.pcampus.edu.np: 10.100.1.10
  - www.doece.pcampus.edu.np: 10.100.6.6
  - www.mech.pcampus.edu.np: 10.100.5.4
  - www.arch.pcampus.edu.np: 10.100.10.4

![website_hosting](https://github.com/user-attachments/assets/a65b88fe-565f-4c7d-879a-51f28afa7bb4)
![nepal_telecom_website](https://github.com/user-attachments/assets/e078c98b-6b85-453c-a925-d6ded5abd715)

## Conclusion

This project successfully implemented a comprehensive network design for Pulchowk Campus, including DNS, IP addressing, routing protocols, and essential network services.
