# Laconia Cybersecurity Lab

## Project Overview

Laconia is a virtual enterprise cybersecurity lab I designed and built to develop practical skills in system administration, networking, cybersecurity, and security monitoring.

The environment simulates a small corporate network using Windows Server, Windows 10, and multiple Linux systems connected through VMware Workstation.

The lab provides hands-on experience with Active Directory, DNS, Group Policy, network configuration, identity and access management, and Splunk SIEM.

## Technologies Used

- **Virtualization:** VMware Workstation
- **Operating Systems:** Windows Server 2019, Windows 10, Debian Linux, Kali Linux, Parrot Security OS
- **Identity Management:** Active Directory Domain Services (AD DS), LDAP, Group Policy
- **Networking:** TCP/IP, DNS, NAT, host-only networking
- **Security Monitoring:** Splunk Enterprise
- **Security Tools:** Linux command-line utilities and network troubleshooting tools

## Project Objectives

- Build and administer a realistic Windows domain environment.
- Configure and troubleshoot communication between Windows and Linux systems.
- Implement centralized identity and access management.
- Develop practical experience with security monitoring and log analysis.
- Use the environment for cybersecurity exercises and incident investigation.


## Network Architecture

The Laconia lab uses VMware Workstation with two virtual networks:

- **VMnet1 (Host-only / RingGate):** 192.168.10.0/24 — Internal communication between lab machines.
- **VMnet8 (NAT):** 192.168.88.0/24 — Provides external network connectivity through the host.

### Virtual Machines

| Machine | Operating System | Internal IP | Role |
|---|---|---|---|
| Laconia Domain Controller | Windows Server 2019 | 192.168.10.10 | Active Directory, DNS, Group Policy |
| Rocinante | Windows 10 | 192.168.10.20 | Domain-joined workstation |
| Medina | Kali Linux | 192.168.10.30 | Security testing |
| MCRN Security | Parrot Security OS | 192.168.10.40 | Security testing |
| Splunk Server | Debian Linux | 192.168.10.50 | Centralized log collection and analysis |

### Active Directory Configuration

- **Domain:** `laconia.local`
- **Domain Controller:** Windows Server 2019
- **Services:** Active Directory Domain Services, DNS, Group Policy
- **Configuration:** Organizational Units (OUs), user accounts, security groups, and domain-joined Windows workstation

## Security Monitoring — Splunk SIEM

I installed Splunk Enterprise on a dedicated Debian Linux virtual machine to develop practical skills in centralized log management, security monitoring, and incident investigation.

### Configuration

- **SIEM Platform:** Splunk Enterprise 10.4.3
- **Operating System:** Debian Linux
- **Internal IP Address:** `192.168.10.50`
- **Receiving Port:** TCP 9997

### Implementation

- Installed and configured Splunk Enterprise on Debian.
- Configured Splunk to receive forwarded data.
- Verified connectivity and data forwarding to the Splunk server.
- Established a foundation for collecting and analyzing security events from the lab environment.

### Next Steps

- Install Splunk Universal Forwarder on the Windows 10 workstation.
- Collect Windows Security Event Logs.
- Practice searching and investigating authentication events.
- Develop basic security monitoring dashboards and alerts.

This environment allows me to practice Windows domain administration, network troubleshooting, access management, and security monitoring in an isolated virtual lab.


