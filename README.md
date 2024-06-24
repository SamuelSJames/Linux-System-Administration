# Linux System Administration Showcase

Welcome to the Linux System Administration Showcase project! This repository demonstrates essential Linux system administration tasks using four different servers: two Ubuntu servers, one Alpine server, and one RockyLinux server. The project highlights the configuration and management of DHCP, DNS, and Nginx servers, along with the use of Docker and Ansible for automation.

## Project Overview

This project aims to showcase various Linux system administration skills by setting up and configuring key network services, managing a Dockerized application, and automating repetitive tasks using Ansible. By completing this project, you'll gain hands-on experience with server configuration, service management, and automation.

## Project Structure

The project is organized into daily tasks, with each day focusing on specific aspects of system administration. Here’s a quick overview of what you will find in this repository:

- **Day 1: System Setup and Initial Configuration**
  - Install and configure Alpine, Ubuntu, and RockyLinux servers.
  - Configure basic network settings.

- **Day 2: User Management and Security**
  - Create and manage user accounts and groups.
  - Implement basic security measures.

- **Day 3: Package Management and Software Installation**
  - Install and configure essential software packages.
  - Setup and configure Nginx on RockyLinux.

- **Day 4: File Systems and Storage Management**
  - Configure and manage file systems and storage.
  - Implement backup strategies.

- **Day 5: Networking and Remote Access**
  - Configure DHCP and DNS on Alpine.
  - Setup and configure SSH on Ubuntu Server 2.

- **Day 6: Monitoring and Logging**
  - Implement system monitoring and logging.
  - Setup a centralized logging server.

- **Day 7: Automation and Scripting**
  - Create automation scripts for routine tasks.
  - Configure and use Ansible for automation.

## Server Roles

- **Ubuntu Server 1:**
  - Docker Host (running a common enterprise application)

- **Ubuntu Server 2:**
  - SSH Server
  - Ansible Control Node

- **Alpine Server:**
  - DHCP Server
  - DNS Server

- **RockyLinux Server:**
  - Nginx Web Server
  - Database Server for the Dockerized application

## Getting Started

To get started with this project, follow the steps below:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/linux-system-administration-showcase.git
   cd linux-system-administration-showcase
   ```

2. **Setup the Servers:**
   - Follow the documentation in the `Day1/system-setup.md` file to install and configure Alpine, Ubuntu, and RockyLinux servers.
   - Configure network settings as described in the `Day1/network-configuration.md` file.

3. **Install Ansible on Ubuntu Server 2:**
   ```bash
   sudo apt update
   sudo apt install ansible -y
   ```

4. **Run Ansible Playbooks:**
   - Navigate to the `ansible/` directory.
   - Run the provided playbooks to automate repetitive tasks.
   ```bash
   ansible-playbook -i inventory playbook.yml
   ```

## Repository Structure

```plaintext
linux-system-administration-showcase/
├── README.md
├── Day1/
│   ├── system-setup.md
│   ├── network-configuration.md
├── Day2/
│   ├── user-management.md
│   ├── security-configuration.md
├── Day3/
│   ├── package-management.md
│   ├── web-server-setup.md
├── Day4/
│   ├── file-systems.md
│   ├── backup-strategies.md
├── Day5/
│   ├── network-services.md
│   ├── vpn-setup.md
├── Day6/
│   ├── monitoring.md
│   ├── centralized-logging.md
├── Day7/
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

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or create a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Thank you for exploring this project! Feel free to reach out if you have any questions or need further assistance. Happy learning!
