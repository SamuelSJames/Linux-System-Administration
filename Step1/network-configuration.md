# Network Configuration

## Network Topology

![Network Topology](/assets/network_topology.png)

## Network Configuration Details

### Web Servers

- **Static IP Addresses:**
  - Web Server 1: 192.168.1.101
  - Web Server 2: 192.168.1.102
  - Web Server 3: 192.168.1.103
  - Web Server 4: 192.168.1.104

### Database Servers

- **Static IP Addresses:**
  - DB Server 1: 192.168.1.201
  - DB Server 2: 192.168.1.202
  - DB Server 3: 192.168.1.203

### Storage Servers

- **Static IP Addresses:**
  - Storage Server 1: 192.168.1.111
  - Storage Server 2: 192.168.1.112

### Network Devices

- **TOR Switches:**
  - TOR Switch 1: 192.168.1.10
  - TOR Switch 2: 192.168.1.11
  - TOR Switch 3: 192.168.1.12

## Configuration Steps

### Configuring Network Interfaces

#### For Ubuntu Servers:

1. **Edit the netplan configuration file:**
   ```bash
   sudo nano /etc/netplan/01-netcfg.yaml
   ```
