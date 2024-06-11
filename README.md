# Terraform and Ansible DevOps Project

## Overview
This project demonstrates setting up a simple web application infrastructure on AWS using Terraform and automating server configuration with Ansible.

### Terraform

Terraform is used to provision the following AWS resources:
- VPC
- Subnets (public and private)
- Internet Gateway
- Route Table
- Security Group
- EC2 Instance
- S3 Bucket
- RDS Instance

### Ansible

Ansible is used to automate the configuration of the web server on the EC2 instance:
- Install Apache web server
- Ensure Apache is running
- Deploy a simple HTML file

## Prerequisites

- AWS Account
- Terraform installed on your local machine
- AWS CLI installed and configured
- Ansible installed on your local machine
- SSH Key for accessing EC2 instance

## Terraform Setup

1. Clone the repository:

```sh
git clone https://github.com/yourusername/terraform-aws-project.git
cd terraform-aws-project
```

2. Initialize Terraform:

```sh
terraform init
```

3. Apply Terraform configuration:

```sh
terraform apply
```

4. Review the plan and type yes to proceed.

## Ansible Setup

1. Navigate to the Ansible directory:

```sh
cd ansible-playbook
```
2. Update the hosts file with your EC2 instance's public IP:

```ini
[webservers]
your-ec2-instance-public-ip
```

3. Run the Ansible playbook:

```sh
ansible-playbook -i hosts site.yml --private-key path-to-your-ssh-key.pem
```

### File Structure

```css
terraform-aws-project/
├── ansible-playbook/
│   ├── hosts
│   ├── site.yml
├── main.tf
├── README.md
```
