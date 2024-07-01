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
  - **Storage Server 1:** 192.168.1.91
  - **Storage Server 2:** 192.168.1.92

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
  - GlusterFS

- **Automation and Configuration Management:**
  - Ansible

## Network Topology

![Network Topology](path_to_topology_image.png)

## Setup Instructions

Follow the steps in the `system-setup.md` and `network-configuration.md` files to set up and configure the servers and network.

## Demonstrated Skills

- Linux server installation and configuration
- Network setup and configuration using Cisco switches
- Web server setup with Nginx
- Database server setup with MySQL and PostgreSQL
- Storage server setup with Ceph and GlusterFS
- Automation with Ansible
