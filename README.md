# Linux System Administration 

## Project Overview

This project demonstrates Linux system administration skills through the setup of a complex network infrastructure. The setup includes multiple web servers, database servers, and storage servers, all managed using Ansible for automation. The network is organized using Cisco switches labeled as Top of Rack (TOR).

## Server Roles and IP Addresses

- **Web Servers:**
  - **Web Server 1:** 192.168.1.101
  - **Web Server 2:** 192.168.1.102
  - **Web Server 3:** 192.168.1.103
  - **Web Server 4:** 192.168.1.104

- **Database Servers:**
  - **DB Server 1:** 192.168.1.201
  - **DB Server 2:** 192.168.1.202
  - **DB Server 3:** 192.168.1.203

- **Storage Servers:**
  - **Storage Server 1:** 192.168.1.111
  - **Storage Server 2:** 192.168.1.112

- **Network Devices:**
  - **TOR Switch 1:** 192.168.1.10
  - **TOR Switch 2:** 192.168.1.11
  - **TOR Switch 3:** 192.168.1.12

## Applications and Tools

- **Web Servers:**
  - Nginx

- **Database Servers:**
  - MySQL
  - PostgreSQL

- **Storage Servers:**
  - Ceph
  - GlusterFS

- **Automation and Configuration Management:**
  - Ansible

## Network Topology

![Network Topology](/assets/Network-Overview.png)

## Setup Instructions

Follow the steps in the `system-setup.md` and `network-configuration.md` files to set up and configure the servers and network.

## Demonstrated Skills

- Linux server installation and configuration
- Network setup and configuration using Cisco switches
- Web server setup with Nginx
- Database server setup with MySQL and PostgreSQL
- Storage server setup with Ceph and GlusterFS
- Automation with Ansible

## Repository Structure
```bash
linux-system-administration/
├── README.md
├── Step1/
│   ├── system-setup.md
│   ├── network-configuration.md
├── Step2/
│   ├── user-management.md
│   ├── security-configuration.md
├── Step3/
│   ├── package-management.md
│   ├── web-server-setup.md
├── Step4/
│   ├── file-systems.md
│   ├── backup-strategies.md
├── Step5/
│   ├── network-services.md
│   ├── vpn-setup.md
├── Step6/
│   ├── monitoring.md
│   ├── centralized-logging.md
├── Step7/
│   ├── automation-scripts.md
│   ├── configuration-management.md
├── ansible/
│   ├── inventory
│   ├── playbook.yml
│   └── roles/
├── docker/
│   ├── docker-compose.yml
│   └── application/
├── scripts/
│   ├── backup-script.sh
│   ├── user-management-script.sh
│   └── update-script.sh
└── configurations/
    ├── sshd_config
    ├── ufw-rules
    ├── nginx.conf
    ├── fstab
    └── dhcpd.conf
```