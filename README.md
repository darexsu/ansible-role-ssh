# Ansible role SSH
[![CI Molecule](https://github.com/darexsu/ansible-role-ssh/actions/workflows/ci.yml/badge.svg)](https://github.com/darexsu/ansible-role-ssh/actions/workflows/ci.yml)

Ansible dependencies: None

Platforms: Debian, Ubuntu, RHEL, CentOS, Rocky, Oracle

Options:  
  - Create ssh-keys and add public key to remote host
  - Disable sudo password for ansible_user on remote host

Installation:
1) Install from Galaxy
```
ansible-galaxy install darexsu.ssh --force
```
2) Example playbook
```yaml
---
- hosts: all
  become: yes

  roles:
    - role: darexsu.ssh
      vars:        
        ssh_actions: true
        ssh_actions_add_public_key_to_host: true
        ssh_actions_no_sudo_password_for_ansible_user: true
```
