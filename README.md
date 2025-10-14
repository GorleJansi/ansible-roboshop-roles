# GorleJansi DevOps Practice Repository

This repository contains Ansible playbooks, roles, and supporting files for deploying and configuring various microservices and applications. It includes infrastructure setup using EC2, Route53 DNS records, application setup, and database initialization.

## Repository Structure
```bash
.
├── group_vars/             # Variables for Ansible playbooks
├── roles/                  # Reusable Ansible roles for each component
├── 01-ec2-r53.yaml         # Playbook to create EC2 instances and Route53 records
├── ansible.cfg             # Ansible configuration file
├── inventory.ini           # Inventory of hosts and groups
├── main.yaml               # Main playbook to run all tasks
└── README.md               # Project documentation
```
## Features

- Provision EC2 instances dynamically using Ansible.
- Configure Route53 DNS records automatically.
- Setup applications and dependencies (Node.js, Java, Python, MongoDB, MySQL).
- Use reusable roles for clean, modular, and maintainable playbooks.
- Load initial data into databases (MongoDB and MySQL).

## How to Use

1. Clone the repository:

```bash
git clone https://github.com/GorleJansi/<repository-name>.git
cd <repository-name>
```

2. Run the main playbook:

```bash
ansible-playbook -i inventory.ini main.yaml
```

3. Pass dynamic variables if needed:

```bash
ansible-playbook -i inventory.ini main.yaml -e "instances=mongodb,redis"
```

## Prerequisites

- Ansible >= 2.10
- Python 3.x
- AWS credentials configured for provisioning EC2 and Route53
- Required IAM permissions for EC2 and Route53 operations

## Authors

- Piyush Kumar Gorle

## License

This project is licensed under the MIT License.
