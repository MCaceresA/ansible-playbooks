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

## Falcon Sensor Installation Playbook

One of the key playbooks in this repository is designed to automate the installation and configuration of the **CrowdStrike Falcon Sensor** on Debian-based servers. CrowdStrike Falcon is a leading endpoint protection platform, and this playbook ensures that the Falcon Sensor is installed correctly, configured with your server’s unique CID and provisioning token, and the service is properly started and enabled for automatic startup.

The playbook includes the following steps:

- **Installation of required tools like `wget`**: Ensures that `wget` is installed on the server for downloading files from the internet.
- **Installation of necessary libraries**: Installs the required library (`libnl-genl-3-200`) to support certain Falcon Sensor functionalities.
- **Copying the Falcon Sensor package to the server**: Transfers the `.deb` package for Falcon Sensor from the local machine to the server.
- **Installation of the Falcon Sensor package**: Installs the Falcon Sensor using the `.deb` package.
- **Configuration of the Falcon Sensor**: Uses the `falconctl` command to configure the sensor with the correct CID and provisioning token.
- **Starting the Falcon Sensor service**: Ensures that the Falcon Sensor service is started and running.
- **Enabling the Falcon Sensor service on boot**: Configures the service to start automatically upon server restart.

The Falcon Sensor is configured with the necessary credentials (CID and token) to connect to your CrowdStrike environment, ensuring that the server is protected by the CrowdStrike platform.

This playbook simplifies the process of setting up the Falcon Sensor on multiple Debian-based servers, ensuring consistent and automated protection across your environment.


## Other Playbooks

In addition to the Zabbix Agent 2 installation, the repository includes anothers other playbooks designed to automate various server configuration tasks. These playbooks aim to streamline the setup and management of servers in a consistent and repeatable manner.
