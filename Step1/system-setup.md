### system-setup.md

# Step 1: System Setup and Initial Configuration

Welcome to Step 1 of the Linux System Administration project! In this step, we will install and configure the Alpine, Ubuntu, and RockyLinux servers. We will also set up the basic network configuration required for our project.

## Topology

Here is the network topology for our setup:

![Network Topology](/assets/network_topology.png)

## Prerequisites

Before you begin, make sure you have the following:

- Access to the installation media for Alpine, Ubuntu, and RockyLinux.
- A virtualization platform or physical machines to host the servers.
- Basic understanding of Linux command-line operations.

## Server Roles and IP Addresses

- **RockyLinux Server:**
  - Role: SSH Server, Ansible Control Node
  - IP Address: `192.168.1.10`

- **Ubuntu Server 1:**
  - Role: Docker Host (running a common enterprise application), Nginx Web Server
  - IP Address: `192.168.1.11`

- **Alpine Server:**
  - Role: DHCP Server, DNS Server
  - IP Address: `192.168.1.12`

- **Ubuntu Server 2:**
  - Role: Database Server for the Dockerized application
  - IP Address: `192.168.1.13`

## Installation Steps

### 1. Installing RockyLinux

1. **Download RockyLinux:**
   - Visit the [RockyLinux download page](https://rockylinux.org/download) and download the latest ISO image.

2. **Create a Bootable USB or Virtual Machine:**
   - Use tools like `Rufus` (for USB) or create a new VM in your virtualization platform.

3. **Boot from the Installation Media:**
   - Insert the USB drive or start the VM and boot from the installation media.

4. **Follow the Installation Wizard:**
   - Choose your language, keyboard layout, and installation destination.
   - Set up your root password and create a user account.

5. **Network Configuration:**
   - During the installation, configure the network settings with the static IP `192.168.1.10`.

### 2. Installing Ubuntu Server 1

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
   - During the installation, configure the network settings with the static IP `192.168.1.11`.

### 3. Installing Alpine Server

1. **Download Alpine Linux:**
   - Visit the [Alpine Linux download page](https://alpinelinux.org/downloads/) and download the latest ISO image.

2. **Create a Bootable USB or Virtual Machine:**
   - Use tools like `Rufus` (for USB) or create a new VM in your virtualization platform.

3. **Boot from the Installation Media:**
   - Insert the USB drive or start the VM and boot from the installation media.

4. **Follow the Installation Steps:**
   - Login as `root` (no password).
   - Run `setup-alpine` and follow the prompts to set up your locale, keyboard layout, hostname, and network settings.
   - Set the static IP to `192.168.1.12`.

### 4. Installing Ubuntu Server 2

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
   - During the installation, configure the network settings with the static IP `192.168.1.13`.

## Initial Configuration

### Updating Packages

After installation, it's essential to update the package lists and upgrade the installed packages to ensure you have the latest updates and security patches.

#### For RockyLinux:
```bash
sudo dnf update -y
sudo dnf upgrade -y
```

#### For Ubuntu:
```bash
sudo apt update
sudo apt upgrade -y
```

#### For Alpine:
```sh
sudo apk update
sudo apk upgrade
```

### Setting Up SSH Access

Ensure SSH is enabled and running on all servers to allow remote access.

#### For RockyLinux:
```bash
sudo systemctl enable sshd
sudo systemctl start sshd
```

#### For Ubuntu:
```bash
sudo systemctl enable ssh
sudo systemctl start ssh
```

#### For Alpine:
```sh
sudo rc-update add sshd
sudo service sshd start
```

### Conclusion

You have now completed the initial setup and configuration of your servers. In the next steps, we will configure user management, security settings, and begin setting up our network services.

Proceed to [Step 2: User Management and Security](../Step2/user-management.md).