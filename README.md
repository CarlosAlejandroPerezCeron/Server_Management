# Server_Management
Ansible playbooks and Terraform scripts to configure and maintain servers.


# Server Management

This repository contains Ansible playbooks and Terraform scripts to efficiently manage servers.

## Structure
- `ansible/`: Contains the playbooks and configuration files for Ansible.
- `terraform/`: Terraform scripts to provision and configure servers.
- `docs/`: Additional documentation.

## Requirements
- Ansible installed (`pip install ansible`)
- Terraform installed ([Official Guide](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli))
- SSH access to the servers for Ansible.
- Credentials configured for AWS or Azure for Terraform.

## Usage
### Ansible
1. Define your servers in `ansible/hosts`.
2. Run the playbook:
 ```bash
 ansible-playbook -i ansible/hosts ansible/main.yml

## Roles

### nginx
Configures the NGINX web server. Includes installation, custom configuration, and restart.

### users
Creates users with default password, groups, and shell settings.

### firewall
Manages firewall rules using UFW. Allows HTTP and SSH traffic by default.

### Validation
Each role includes validation tasks to ensure changes were applied correctly.
