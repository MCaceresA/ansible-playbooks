# Ansible Playbooks for Server Automation

![Ansible Logo](https://upload.wikimedia.org/wikipedia/commons/2/24/Ansible_logo.svg)

This repository contains a collection of Ansible playbooks designed to automate the configuration and management of Debian-based servers. Tasks include package installation, service configuration, and security hardening.

## Included Playbooks

The repository includes several playbooks for different purposes, ensuring quick and consistent configuration across Debian servers.

### 1. **ActiveMQ Installation**  
Playbook: `install_activeMQ.yml`  
- Installs and configures **ActiveMQ**, a popular messaging system.  
- Sets up services to start automatically on boot.  

### 2. **CrowdStrike Falcon Sensor Installation**  
Playbook: `install_crowdstrike.yml`  
- Installs **CrowdStrike Falcon Sensor** for advanced server protection.  
- Configures the agent with CID and provisioning token.  
- Enables the service to start automatically.  

### 3. **Java Zulu 17 Installation**  
Playbook: `install_java_zulu17.yml`  
- Downloads and installs **Zulu JDK 17** from Azul Systems.  
- Configures appropriate environment variables.  

### 4. **Nginx Installation**  
Playbook: `install_nginx.yml`  
- Installs and configures **Nginx**, a web server and reverse proxy.  
- Enables the service for automatic startup.  

### 5. **Sudo Installation and Configuration**  
Playbook: `install_sudo.yml`  
- Ensures the `sudo` package is installed.  
- Configures basic access rules for users.  

### 6. **Zabbix Agent 2 Installation**  
Playbook: `install_zabbix_agent2.yml`  
- Installs and configures **Zabbix Agent 2** for monitoring.  
- Configures parameters such as `Server`, `ServerActive`, and `Hostname`.  
- Starts and enables the service for automatic startup.  

## How to Use These Playbooks  

1. Install Ansible on the control machine:  
   ```bash
   sudo apt update && sudo apt install ansible -y
   ```  
2. Clone the repository:  
   ```bash
   git clone https://github.com/your-repo/ansible-playbooks.git
   cd ansible-playbooks
   ```  
3. Run a playbook:  
   ```bash
   ansible-playbook -i inventory install_nginx.yml
   ```  
