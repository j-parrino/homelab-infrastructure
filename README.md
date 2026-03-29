# Homelab Infrastructure Build

## Overview

This project documents the design and deployment of a personal homelab environment built using VMware Workstation to simulate real-world IT infrastructure. The lab is used to develop hands-on skills in system administration, networking, and cybersecurity.

The environment mirrors enterprise-style systems including Active Directory, internal networking, and multi-VM deployments.

---

## Objectives

* Build a stable virtualized lab environment using VMware Workstation
* Deploy and manage Windows and Linux systems
* Configure Active Directory domain services
* Practice network configuration and segmentation concepts
* Strengthen system administration and troubleshooting skills
* Simulate security-focused environments

---

## Technologies Used

* VMware Workstation (Virtualization)
* Windows Server 2019
* Windows 10/11
* Linux (Ubuntu)
* Active Directory
* TCP/IP Networking
* NAT / Host-Only Networking
* Remote Desktop / SSH

---

## Lab Environment

### Host System

* Hypervisor: VMware Workstation
* Hardware: AMD Ryzen 3 5425U (2.70 GHz), 32GB, 2 TB

### Virtual Machines

| VM Name  | OS             | Role                      |
| -------- | -------------- | ------------------------- |
| DC01     | Windows Server | Domain Controller         |
| Client01 | Windows 10     | Domain-joined workstation |
| LINUX01  | Ubuntu         | Linux server              |
| Kali     | Kali           | Attack machine            |
| SecOnion | CentOS         | Intrusion Detection       |
| pfsense  | FreeBSD        | Firewall                  |
| Splunk   | Ubuntu         | SIEM                      |

---

## Network Design

* Configured **host-only network** for internal lab communication
* Used **NAT networking** for internet access when needed
* Static IP addressing for domain environment
* Isolated lab network from host system

---

## Architecture Diagram

![Lab Diagram](./diagrams/homelab-diagram.png)

---

## Implementation

### 1. VMware Workstation Setup

* Installed VMware Workstation on host system
* Created virtual network adapters (NAT and Host-Only)
* Configured VM networking for internal communication

### 2. Domain Controller Setup

* Installed Windows Server
* Promoted to Domain Controller
* Configured Active Directory Domain Services
* Created users, groups, and organizational units

### 3. Client Machine Setup

* Installed Windows 10
* Joined system to domain
* Verified authentication and domain connectivity

### 4. Linux System Setup

* Installed Ubuntu
* Configured networking and SSH access
* Practiced basic Linux system administration

---

## Screenshots

### VMware Workstation Interface

![VMware](./screenshots/vmware-dashboard.png)

### Active Directory Users & Computers

### Active Directory Management
![Active Directory](./screenshots/ad-users.png)
Displays organizational units and user account management within the Active Directory domain, demonstrating identity and access control configuration.

### Domain Join Verification
![Domain Join](./screenshots/domain-join.png)
Displays a client system successfully joined to the Active Directory domain, confirming proper DNS configuration, domain integration, and centralized authentication.

### Security Onion System Access (Linux)
![Security Onion](./screenshots/linux-access.png)
Demonstrates command-line access to the Security Onion management system, including hostname identification, user context, and network configuration within the lab environment. This system is used for security monitoring, intrusion detection, and log analysis.

### Linux System Monitoring (Kali)
![Linux Monitoring](./screenshots/linux-monitoring.png)
Real-time system monitoring using htop, displaying CPU utilization, memory usage, and active processes within the Kali Linux environment.

---

## Key Takeaways

* Built and managed a multi-VM lab using VMware Workstation
* Gained hands-on experience with Active Directory
* Practiced network configuration using NAT and host-only networks
* Strengthened troubleshooting and system administration skills

---

## Future Improvements

* Implement network segmentation (advanced virtual networking)
* Add firewall rules and access control policies
* Integrate logging and monitoring tools
* Expand lab with additional servers and services
* Simulate security incidents and response workflows

---
