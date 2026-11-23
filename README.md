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
