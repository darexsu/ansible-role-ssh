# Ansible role SSH
Ansible dependencies: None

Platforms: Debian, RedHat

Options:
  - Install openssh-server
  - Creat your ssh-keys and add public key to remote host
  - Disable sudo password for ansible_user on remote host

Installation:
1) Install from Github (git installed on your server)
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
        ssh_install: true
        ssh_actions: true
        ssh_actions_add_public_key_to_host: true
        ssh_actions_no_sudo_password_for_ansible_user: true
```
