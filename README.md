# Ansible role SSH
Options:
  - Install openssh-server
  - Creat your ssh-keys and add public key to remote host
  - Disable sudo password for ansible_user on remote host

Platforms:
  - Debian, Ubuntu

Ansible dependencies:
  - None

Installation:
1) Install from Github (git installed on your server)
```
ansible-galaxy install git+https://github.com/darexsu/ansible-role-ssh.git --force
```
2) Example playbook
```yaml
---
- hosts: all
  become: yes

  roles:
    - role: ansible-role-ssh
      vars:
        ssh_install: true
        ssh_actions: true
        ssh_actions_add_public_key_to_host: true
        ssh_actions_no_sudo_password_for_ansible_user: true
```
