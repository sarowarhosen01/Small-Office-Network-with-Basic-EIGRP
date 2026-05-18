# Small Office Network with Basic EIGRP

![Cisco](https://img.shields.io/badge/Cisco-Network%20Engineer-blue?style=for-the-badge&logo=cisco)
![Packet Tracer](https://img.shields.io/badge/Packet%20Tracer-8.2.2-orange?style=for-the-badge)
![EIGRP](https://img.shields.io/badge/Routing-EIGRP-green?style=for-the-badge)
![CCNA](https://img.shields.io/badge/CCNA-Certified-1E90FF?style=for-the-badge)

**A production-like small office network design featuring dynamic EIGRP routing, VLAN segmentation, and enterprise services.**

![Network Topology](https://via.placeholder.com/800x400/0A2540/FFFFFF?text=Small+Office+EIGRP+Topology) <!-- Replace with actual screenshot -->

## Project Overview

Designed and implemented a scalable small office network for a fictional company ("TechFlow Solutions") supporting ~100 users across multiple departments. The network uses Cisco devices in Packet Tracer and incorporates **EIGRP** as the primary dynamic routing protocol for efficient route propagation and rapid convergence.

This project emphasizes **security-first design**, redundancy, and modern network automation practices.

**Live Demo:** Open the `.pkt` file in Cisco Packet Tracer 8.2+

## Project Goals

- Implement a hierarchical, segmented network using best practices
- Deploy EIGRP for dynamic routing with optimal metrics and summarization
- Ensure secure inter-VLAN communication and remote access
- Configure essential services (DHCP, DNS, NTP, SSH)
- Document configurations, verification steps, and troubleshooting
- Demonstrate automation readiness with Ansible/Python

## Features

- Multi-router EIGRP AS 100 with neighbor authentication
- VLAN segmentation (Admin, Sales, Guest, Server)
- Inter-VLAN routing via Layer 3 device
- DHCP server with reservations
- NAT/PAT for internet access
- Basic firewall policies (ACLs)
- SSH and secure management
- Monitoring & logging foundations

## Technologies Used

- **Routing:** EIGRP (IPv4)
- **Switching:** VLANs, Trunking (802.1Q), VTP
- **Security:** ACLs, SSH, Password Encryption, EIGRP Authentication
- **Services:** DHCP, DNS, NTP, NAT
- **Tools:** Cisco Packet Tracer, Ansible (examples), Python (Netmiko/Paramiko)
- **Monitoring:** Zabbix/Grafana (conceptual integration)
- **OS/Platforms:** Cisco IOS, Linux (for automation)

## Network Architecture Overview

The network follows a **three-tier hierarchical design** (simplified for small office):

- **Core/Distribution:** Router R1 (acts as core with EIGRP and inter-VLAN routing)
- **Access:** Layer 2 switches with VLANs
- **Edge:** WAN simulation and NAT

**Key Design Principles:** Redundancy in routing, traffic segmentation, least-privilege access, and scalability.

## Network Topology Diagram (ASCII)

```ascii
                  Internet (Simulated)
                        |
                     [R1 - Core Router]
                       /     \
                      /       \
                [SW1]         [R2 - Branch Router]
                 |               |
            [VLANs 10/20/30]   [VLAN 40 - Remote]
                 |
            End Devices (PCs, Printers, Servers)
