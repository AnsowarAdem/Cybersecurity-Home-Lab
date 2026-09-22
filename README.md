# Cybersecurity & Infrastructure Home Lab

**Proxmox • Windows • Linux • Synology • Raspberry Pi • Networking • Pi-hole • Nginx • Uptime Kuma • T-Pot • Wazuh**

---

## Overview

This project documents the cybersecurity and infrastructure lab I built and maintain at home.

What started as a few computers and Raspberry Pis gradually grew into a dedicated home lab with its own physical rack, networking equipment, storage, virtualization servers, monitoring tools, and security platforms.

The goal was to build something closer to a small real-world IT environment instead of simply running isolated virtual machines on my computer. I wanted a place where I could break things, rebuild them, troubleshoot problems, deploy services, experiment with security tools, and gain hands-on experience managing infrastructure from the ground up.

My rack now includes physical networking equipment, a Proxmox virtualization host, Synology NAS, Raspberry Pi systems, routers, a network switch, and UPS battery backup. On top of that hardware, I run Windows and Linux virtual machines along with services for DNS filtering, reverse proxying, uptime monitoring, SIEM monitoring, vulnerability testing, and honeypot telemetry.

This lab is constantly evolving as I learn new technologies and add new projects.

---

## 🖥️ What I Built

The lab combines both **physical hardware and virtual infrastructure**.

Instead of treating each cybersecurity project as a separate environment, I designed the home lab so many of my projects can operate together as part of the same network.

For example:

* Proxmox provides virtualization for Windows, Linux, and cybersecurity systems
* Synology provides centralized network storage
* Raspberry Pis host lightweight infrastructure services
* Pi-hole provides network-wide DNS filtering
* Nginx provides reverse proxy functionality for internal services
* Uptime Kuma monitors whether services and systems are available
* Wazuh provides centralized security monitoring and endpoint visibility
* T-Pot provides honeypot telemetry and malicious traffic visibility
* My routers and Ethernet switch connect the physical lab infrastructure
* A UPS helps keep critical networking and infrastructure equipment online during brief power interruptions

Building everything myself has given me experience not only deploying services, but also understanding how the different pieces of an IT environment depend on one another.

---

## 🧰 Lab Components

| Component           | Platform         | Purpose                                                                   |
| ------------------- | ---------------- | ------------------------------------------------------------------------- |
| Hypervisor          | Proxmox VE       | Hosts Windows, Linux, and cybersecurity virtual machines                  |
| Windows VM          | Windows 11       | Endpoint testing, administration, and security monitoring                 |
| Linux VM            | Ubuntu           | Linux administration and infrastructure services                          |
| Honeypot            | T-Pot            | Captures and analyzes malicious activity                                  |
| Storage             | Synology NAS     | Centralized storage, backups, and NFS                                     |
| DNS Filtering       | Pi-hole          | Network-wide DNS filtering and visibility                                 |
| Reverse Proxy       | Nginx            | Routes traffic to internal web services                                   |
| Monitoring          | Uptime Kuma      | Monitors service availability and response times                          |
| Security Monitoring | Wazuh            | SIEM, endpoint monitoring, threat detection, and vulnerability visibility |
| Compute             | Raspberry Pi     | Hosts lightweight infrastructure services                                 |
| Network             | Routers + Switch | Connects physical and virtual lab systems                                 |
| Power               | UPS              | Provides battery backup for critical lab infrastructure                   |

---

## 🎯 Lab Objectives

I built this lab to develop practical experience beyond classroom assignments and certification material.

The main objectives are to:

* Build and administer a virtualized environment using Proxmox
* Manage Windows and Linux systems
* Configure and troubleshoot local network infrastructure
* Operate network-attached storage
* Deploy self-hosted services
* Manage Raspberry Pi infrastructure
* Monitor service health and availability
* Implement network-level DNS filtering
* Configure reverse proxy services
* Deploy SIEM and endpoint monitoring
* Generate and analyze security telemetry
* Practice vulnerability management and threat detection
* Troubleshoot networking, storage, virtualization, and operating-system issues
* Improve infrastructure reliability and redundancy
* Document technical projects in a way that reflects real IT operations

---

## 🧪 Technologies Used

### Virtualization

* Proxmox VE
* Windows 11
* Ubuntu Linux
* Virtual networking
* Virtual storage
* Linux bridges

### Networking

* Primary router
* Secondary lab router
* Managed/wired Ethernet infrastructure
* Ethernet switch
* TCP/IP
* DNS
* DHCP
* Internal network segmentation

### Storage

* Synology NAS
* NFS
* Local storage
* Network-attached storage
* Backup storage

### Raspberry Pi Infrastructure

* Raspberry Pi
* Pi-hole
* Nginx reverse proxy
* Uptime Kuma
* Docker containers

### Cybersecurity

* Wazuh SIEM
* T-Pot Honeypot
* Endpoint monitoring
* Security event collection
* Threat hunting
* Vulnerability detection
* CVE analysis
* MITRE ATT&CK mapping

### Infrastructure

* UPS battery backup
* Windows endpoints
* Linux systems
* Self-hosted services
* Physical home lab rack

---

## 🏗️ Lab Architecture

The environment is built around a dedicated physical home lab rack containing the networking, compute, storage, and power infrastructure.

A simplified view of the environment is shown below:

```text
                             Internet
                                |
                           Main Router
                                |
                         Secondary Router
                                |
                             Switch
              ┌─────────────────┼──────────────────┐
              │                 │                  │
         Proxmox Host      Synology NAS      Raspberry Pi
              │                 │                  │
       ┌──────┼──────┐          │          ┌───────┼────────┐
       │      │      │          │          │       │        │
   Windows  Ubuntu  T-Pot      NFS      Pi-hole  Nginx   Uptime
     VM       VM   Honeypot                     Proxy     Kuma
       │
       └─────────────── Wazuh Monitoring ───────────────┐
                                                        │
                                          Windows / Linux Endpoints
```

---

## 🔧 Why I Built It

One of the main reasons I built this environment was to move beyond simply reading about cybersecurity and IT infrastructure.

Working with a physical rack and real hardware introduces problems that do not always appear in guided labs: networking mistakes, storage issues, resource limitations, failed services, DNS problems, VM configuration errors, remote-access issues, and hardware constraints.

Those problems are part of what makes the lab valuable.

Instead of following a perfectly controlled tutorial environment, I have to troubleshoot systems that I actually depend on and understand how changes to one part of the network can affect everything else.

The lab has become my personal environment for experimenting with infrastructure, cybersecurity, networking, virtualization, and system administration.

---

## 🚀 Current Projects

The home lab also serves as the foundation for several cybersecurity projects, including:

* **Wazuh SIEM Home Lab** – Centralized endpoint monitoring, security event analysis, vulnerability detection, and MITRE ATT&CK mapping
* **Vulnerability Management Lab** – Vulnerability scanning, remediation, rescanning, and validation using Nessus
* **Active Directory Security Lab** – Windows Server, Active Directory, DHCP, administrative accounts, Group Policy, and PowerShell automation
* **T-Pot Honeypot** – Collection and analysis of malicious traffic and attack telemetry

Additional infrastructure and security projects will continue to be added as the lab grows.

---

## 📈 Ongoing Development

This is not a finished lab.

I continue to expand the environment by adding new systems, improving network architecture, deploying security tools, strengthening monitoring, and documenting what I learn along the way.

The goal is for this repository to show both the infrastructure itself and my progression in designing, administering, securing, and troubleshooting a real home lab environment.
