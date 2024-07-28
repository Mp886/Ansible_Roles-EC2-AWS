Role Name
=========

This Ansible role creates and manages an EC2 instance on AWS.

Requirements
------------

- Ansible 2.9 or higher
- boto3 and botocore libraries for AWS interactions
- Valid AWS credentials

Role Variables
--------------

Default Variables (defaults/main.yml)

- `type`: The instance type to use (default: `t2.micro`)
- `ami`: The Amazon Machine Image (AMI) ID to use (default: `ami-04b70fa74e45c3917`

Other Variables

- `ec2_access_key`: Your AWS access key (should be stored securely, e.g., in Ansible Vault)
- `ec2_secret_key`: Your AWS secret key (should be stored securely, e.g., in Ansible Vault)

Dependencies
------------

This role has no dependencies on other roles.

Example Playbook
----------------k

```yaml
---
- hosts: localhost
  connection: local
  roles:
    - ec2_roles
