# MikroTik Password Change Automation

This project provides an Ansible script for automatically changing user passwords on MikroTik routers. It is useful for managing and updating passwords across a large network of MikroTik devices.

## Features

- Automatically change passwords for MikroTik users.
- Uses Ansible for automating the password change process.
- Supports multiple MikroTik devices simultaneously.
- Allows setting a timeout for operations.

## Prerequisites

To use this project, the following are required:

- [Ansible](https://www.ansible.com/)
- SSH access to MikroTik devices with the `admin` user.
- Ubuntu or a similar operating system (for other systems, adjustments may be required).

## Installation

1. **Install Ansible**:
   ```bash
   sudo apt update
   sudo apt install ansible
   ```

2. **Clone the Project**:
   Clone this repository from GitHub:
   ```bash
   git clone https://github.com/username/mikrotik-password-change-automation.git
   cd mikrotik-password-change-automation
   ```

3. **Configure the `hosts` File**:
   In the `hosts` file, add the IP addresses of your MikroTik devices.

4. **Run the Script**:
   Execute the script using Ansible:
   ```bash
   ansible-playbook -i hosts playbook.yml
   ```

## Usage

To change the password, update the `playbook.yml` file with the new password, and then run the script. The script will automatically connect to MikroTik devices and change the password.

## Project Structure

```
├── hosts                # Ansible configuration file (device IPs)
├── playbook.yml         # Playbook file for changing passwords
├── README.md            # This file
└── .gitignore            # Files to exclude from git
```

## Troubleshooting

- **MikroTik devices are unreachable**: Ensure SSH settings and device access are properly configured.
- **Timeout errors**: If you encounter timeouts, increase the timeout value in the `playbook.yml` file.


---

##ansible-playbook -i hosts playbook.yml
