# radware_alteon_modules

## Description
The alteon_modules project provides an Ansible collection for managing and automating your Radware Alteon devices. It consists of a set of modules and roles for performing tasks related to Radware devices configuration. This collection is for customers who wish to create Ansible playbooks in a very simple and intuitive way.
These modules make use of the REST API support implemented on Alteon hardware and virtual platforms.
With Radware Ansible modules, you can simplify frequent tasks such as:
- Alteon device setup - basic settings like DNS, NTP etc.
- Alteon network setup (VLANs, IP Interfaces, Routing)
- Application delivery


<img src="https://www.radware.com/RadwareSite/MediaLibraries/Images/logo.svg" width="300px">

[![CI sanity tests & deploy to galaxy](https://github.com/Radware/radware_alteon_modules/actions/workflows/ansible-sanity-and-deployment.yml/badge.svg)](https://github.com/Radware/radware_alteon_modules/actions/workflows/ansible-sanity-and-deployment.yml)


## Requirements
- Ansible >= 2.15.0
- Python >= 3.9
- alteon-sdk python package

## Installation
Before using this collection, you need to install it with the Ansible Galaxy command-line tool:
```
# ansible-galaxy collection install radware.radware_alteon
# pip install alteon-sdk
```
Please not that it will not be upgraded automatically when you upgrade the Ansible package.
To upgrade the collection to the latest available version, run the following command:
```
# ansible-galaxy collection install radware.radware_alteon --upgrade
```
You can also install a specific version of the collection, for example:
```
# ansible-galaxy collection install radware.radware_alteon:==1.1.2
```

## Use Cases
Once the collection is installed, you can use it in a playbook by specifying the full namespace path to the module, plugin and/or role.

```
- hosts: localhost

  tasks:
  - name: alteon configuration command
    radware.radware_alteon.alteon_config_l7_content_class:
      provider: 
        server: 192.168.1.1
        user: admin
        password: admin
        validate_certs: no
        https_port: 443
        ssh_port: 22
        timeout: 5
      state: present
      parameters:
        content_class_id: 3
        name: content_class3
        content_class_type: http2
```

## Support
This collection supports versions 1.x and higher of the radware.radware_alteon Ansible collection. Ensure you are using a compatible version by checking the version number.
If you have any questions about the radware_alteon_modules collection, please refer to the official Radware Alteon Documentation for detailed guides and troubleshooting steps.

## Testing
The collection was tested against the following environments:

Ansible Versions: 2.14.0, 2.15.0, 2.16.0
Python Versions: 3.9 , 3.10, 3.11
Radware Alteon Devices:
- Alteon SA/VX
- Alteon VA virtual appliances

Automation tests were done to verify all modules functionality.
The tests covered various scenarios, including typical use cases and edge cases.
The tests included setup and configuration of network elements such as VLANs, IP interfaces, and routing.
These tests included applying configurations and verifying the outcomes directly on Radware Alteon devices.
Various scenarios such as device setup, network configuration, and application delivery were tested.

#### Test Results:

Functionality: All modules performed as expected, accurately configuring the Radware Alteon devices according to the provided playbook instructions.
Reliability: The modules were consistent in their performance across different Ansible and Python versions.
Compatibility: No significant compatibility issues were observed with supported Radware Alteon hardware and virtual platforms.

## License Information
GNU General Public License v3.0
Copyright 2024 Radware LTD

