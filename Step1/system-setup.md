# System Setup and Initial Configuration

## Topology

![Network Topology](path_to_topology_image.png)

## Prerequisites

- Installation media for Ubuntu
- Virtualization platform or physical machines
- Basic Linux command-line knowledge

## Server Roles and IP Addresses

- **Web Servers:**
  - Web Server 1: 192.168.1.101
  - Web Server 2: 192.168.1.102
  - Web Server 3: 192.168.1.103
  - Web Server 4: 192.168.1.104

- **Database Servers:**
  - DB Server 1: 192.168.1.201
  - DB Server 2: 192.168.1.202
  - DB Server 3: 192.168.1.203

- **Storage Servers:**
  - Storage Server 1: 192.168.1.111
  - Storage Server 2: 192.168.1.112

## Installation Steps

### Installing Ubuntu Server

1. **Download Ubuntu Server:**
   - Visit the [Ubuntu download page](https://ubuntu.com/download/server) and download the latest LTS ISO image.

2. **Create a Bootable USB or Virtual Machine:**
   - Use tools like `Rufus` (for USB) or create a new VM in your virtualization platform.

3. **Boot from the Installation Media:**
   - Insert the USB drive or start the VM and boot from the installation media.

4. **Follow the Installation Wizard:**
   - Choose your language, keyboard layout, and installation destination.
   - Set up your root password and create a user account.

5. **Network Configuration:**
   - During the installation, configure the network settings with the static IP addresses mentioned above.

6. **Update Packages:**
   ```bash
   sudo apt update
   sudo apt upgrade -y
   ```
