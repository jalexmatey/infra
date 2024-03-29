# Infrastructure

> How all my services are configured.  

This repository contains the configurations for most of my devices/services:
- [Plex](https://www.plex.tv/) for video streaming.
- A MacOS theme for deb and rpm based distros.

## Requirements
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

## Install
```bash
# clone the repo to your local machine
git clone https://github.com/jalexm8/home-tech.git
```

## Update
```bash
git checkout main
git pull
```

## To run
```bash
# Fedora workstation
ansible-playbook fedora-workstation.yml --ask-become-pass --ask-vault-pass

# Ubuntu server, pre init
ansible-playbook ubuntu-server.yml --ask-become-pass --ask-vault-pass -e 'custom_ssh_port=22'

# Ubuntu server, post init
ansible-playbook ubuntu-server.yml --ask-become-pass --ask-vault-pass
```
