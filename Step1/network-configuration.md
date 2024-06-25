### network-configuration.md

# Step 1: Network Configuration

Welcome to the network configuration guide for the Linux System Administration Showcase project. In this document, we will configure the network settings for the Alpine, Ubuntu, and RockyLinux servers. Proper network configuration is crucial for ensuring that the servers can communicate with each other and function correctly within the network topology.

## Network Topology

Here is the network topology for our setup:

![Network Topology](path_to_topology_image.png)

*Replace `path_to_topology_image.png` with the actual path to your network topology image.*

## Network Configuration Details

Each server will be assigned a static IP address within the 192.168.1.0/24 subnet.

### RockyLinux Server

- **Role:** SSH Server, Ansible Control Node
- **Static IP Address:** 192.168.1.10
- **Subnet Mask:** 255.255.255.0
- **Gateway:** 192.168.1.1
- **DNS Server:** 192.168.1.12

#### Configuration Steps

1. **Edit the network configuration file:**
   ```bash
   sudo nano /etc/sysconfig/network-scripts/ifcfg-eth0
   ```

2. **Add the following configuration:**
   ```plaintext
   DEVICE=eth0
   BOOTPROTO=none
   ONBOOT=yes
   IPADDR=192.168.1.10
   NETMASK=255.255.255.0
   GATEWAY=192.168.1.1
   DNS1=192.168.1.12
   ```

3. **Restart the network service:**
   ```bash
   sudo systemctl restart network
   ```

### Ubuntu Server 1

- **Role:** Docker Host, Nginx Web Server
- **Static IP Address:** 192.168.1.11
- **Subnet Mask:** 255.255.255.0
- **Gateway:** 192.168.1.1
- **DNS Server:** 192.168.1.12

#### Configuration Steps

1. **Edit the netplan configuration file:**
   ```bash
   sudo nano /etc/netplan/01-netcfg.yaml
   ```

2. **Add the following configuration:**
   ```yaml
   network:
     version: 2
     renderer: networkd
     ethernets:
       eth0:
         dhcp4: no
         addresses:
           - 192.168.1.11/24
         gateway4: 192.168.1.1
         nameservers:
           addresses:
             - 192.168.1.12
   ```

3. **Apply the netplan configuration:**
   ```bash
   sudo netplan apply
   ```

### Alpine Server

- **Role:** DHCP Server, DNS Server
- **Static IP Address:** 192.168.1.12
- **Subnet Mask:** 255.255.255.0
- **Gateway:** 192.168.1.1

#### Configuration Steps

1. **Edit the network interfaces configuration:**
   ```sh
   sudo nano /etc/network/interfaces
   ```

2. **Add the following configuration:**
   ```plaintext
   auto eth0
   iface eth0 inet static
       address 192.168.1.12
       netmask 255.255.255.0
       gateway 192.168.1.1
   ```

3. **Restart the networking service:**
   ```sh
   sudo /etc/init.d/networking restart
   ```

### Ubuntu Server 2

- **Role:** Database Server
- **Static IP Address:** 192.168.1.13
- **Subnet Mask:** 255.255.255.0
- **Gateway:** 192.168.1.1
- **DNS Server:** 192.168.1.12

#### Configuration Steps

1. **Edit the netplan configuration file:**
   ```bash
   sudo nano /etc/netplan/01-netcfg.yaml
   ```

2. **Add the following configuration:**
   ```yaml
   network:
     version: 2
     renderer: networkd
     ethernets:
       eth0:
         dhcp4: no
         addresses:
           - 192.168.1.13/24
         gateway4: 192.168.1.1
         nameservers:
           addresses:
             - 192.168.1.12
   ```

3. **Apply the netplan configuration:**
   ```bash
   sudo netplan apply
   ```

## Verifying Network Configuration

After configuring the network settings on each server, verify the configurations by performing the following checks:

1. **Ping the Gateway:**
   ```bash
   ping -c 4 192.168.1.1
   ```

2. **Ping the DNS Server:**
   ```bash
   ping -c 4 192.168.1.12
   ```

3. **Ping Other Servers:**
   ```bash
   ping -c 4 192.168.1.10  # Ping RockyLinux from other servers
   ping -c 4 192.168.1.11  # Ping Ubuntu Server 1 from other servers
   ping -c 4 192.168.1.13  # Ping Ubuntu Server 2 from other servers
   ```

If all pings are successful, the network configuration is correct. If you encounter any issues, double-check the network configuration files for typos or incorrect settings.

## Conclusion

You have now successfully configured the network settings for all the servers in the Linux System Administration Showcase project. Proceed to [Step 2: User Management and Security](../Step2/user-management.md) to continue with the project setup.