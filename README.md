# Snort-IDS-Home-Lab
A hands-on Snort 2 IDS home lab using Kali linux, Ubuntu server, and Metasploitable 2.


## Project Overview
This project is a hands-on network intrusion detection lab build using **Snort 2**.

The lab simulates a small network environment where **Kali Linux** is used to generate *test traffic*, **Ubuntu Server** acts as a *router and IDS sensor*, and **Metasploitable 2** serves as a *vulnerable target machine*.

The main objective is to understand how network traffic is monitored, how intrusion detection rules work, and how suspicious network activity can be identified and analyzed using Snort.

## Lab Architecture
The lab consists of three virtual machines running in **VMware Workstation**.
| Virtual Machine | Operating system | Role |
|---|---|---|
| VM 1 | Kali linux | Attacker
| VM 2 | Ubuntu server | Router and IDS 
| VM 3 | Metasploitable 2 | Vulnerable Target

### Network Architecture
The lab uses two virtual networks:
- NAT Network: Connects Kali linux and Ubuntu server.
- Host-only Network: Connects Ubuntu server and Metasploitable 2.

Ubuntu server acts as a router between two networks and monitors traffic through its host-only interface using Snort.

## IP Addressing
| Virtual Machine | Network Interface | IP Address | Network |
|---|---|---|---|
| Kali linux | eth0 | 192.168.243.129 | NAT | 
| Ubuntu Server | ens33 | 192.168.243.135 | NAT | 
| Ubuntu Server | ens37 | 192.168.26.128 | Host-only | 
| Metasploitable 2 | eth1 | 192.168.26.10 | Host-only |

## Network Design 
The lab uses two seperate network segments: 
- **NAT Network (192.168.243.0/24):** Connects Kali linux to Ubuntu server.
- **Host-only Network (192.168.26.0):** Connects Ubuntu server to Metasploitable 2.

Ubuntu server acts as a router between these networks using IPv4 forwarding.

Kali linux communicates with Metaspolitable 2 through Ubuntu server rather than directly.

Snort monitors network traffic on Ubuntu Server's host-only interface (`ens37`).

## Technologies Used

- **VMware Workstation 17 Player** - Virtualization platform
- **Kali linux** - Attacker
- **Ubuntu Server 24.04.5 LTS** - Router and IDS
- **Metasploitable 2** - Vulnerable target machine
- **Snort 2.9.20** - Network intrusion detection system
- **Netplan** - Ubuntu network configuration (Permanent Static IP) 
- **Linux networking tools** - Routing, IP addressing, and connectivity testing

## Learning Objectives

- Understand how network intrusion detection systems work.
- Learn how Snort analyzes network traffic.
- Configure and manage Snort detection rules.
- Monitor network traffic and identify suspcious activity.
- Generate test traffic using Kali linux.
- Analyze Snort alerts and investigate network events.
- Understand network routing and packet forwarding.
- Develop practical blue team and SOC analyst skills.

## Project Roadmap

- [x] Set up three virtual machines.
- [x] Configure NAT and Host-only networks.
- [x] Assign IP addresses.
- [x] Configure Ubuntu server as a router.
- [x] Enable IPv4 forwarding.
- [x] Establish connectivity between Kali and Metasploitable 2.
- [x] Install Snort 2.9.20.
- [x] Configure Snort $HOME_NET.
- [ ] Configure Snort monitoring interface.
- [ ] Configure and understand detection rules.
- [ ] Generate test traffic from Kali linux.
- [ ] Detect suspicious activity using Snort.
- [ ] Analyze and document Snort alerts.
