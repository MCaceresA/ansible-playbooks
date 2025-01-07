# ![Ansible Logo](https://upload.wikimedia.org/wikipedia/commons/2/24/Ansible_logo.svg)

# Ansible Playbooks for Server Automation

This repository contains a collection of Ansible playbooks designed to automate the configuration and management of Debian-based servers. The playbooks cover a variety of tasks ranging from installing software packages to configuring system services, all aimed at improving efficiency and consistency in server management.

## Included Playbooks

The repository includes multiple playbooks for various server setup and maintenance tasks. Each playbook is intended to be reusable and customizable based on the specific needs of your environment. Key tasks automated by these playbooks include package installations, service configurations, and security hardening.

## Zabbix Agent 2 Installation Playbook

One of the key playbooks in this repository is designed to automate the installation and configuration of **Zabbix Agent 2** on Debian-based servers. Zabbix is an enterprise-level monitoring solution, and this playbook ensures that the agent is installed correctly, configured with your server’s details, and the service is properly started and enabled for automatic startup.

The playbook includes the following steps:
- Installation of required tools like `wget`.
- Download and installation of the Zabbix release package.
- Installation of Zabbix Agent 2 and any necessary plugins.
- Configuration of critical settings such as the `Server`, `ServerActive`, and `Hostname` parameters.
- Enabling and starting the Zabbix Agent 2 service to ensure it runs automatically on boot.

The Zabbix Agent 2 configuration file is customized with the correct server address, ensuring the agent communicates with the Zabbix server effectively.

This playbook helps simplify the process of setting up Zabbix Agent 2 on multiple Debian-based servers, ensuring consistency across your environment.

## Other Playbooks

In addition to the Zabbix Agent 2 installation, the repository includes several other playbooks designed to automate various server configuration tasks. These playbooks aim to streamline the setup and management of servers in a consistent and repeatable manner.
