# ezplatform-vagrant

This repository will let you to install eZ Platform with Vagrant and Ansible. The full stack contains:

- Varnish 6.x
- Nginx 1.10.x
- MariaDB 10.1.x
- PHP 7.2.x
- Redis  3.2.x

# Requirements

First you need to install [Vagrant](https://www.vagrantup.com/docs/installation/)  and [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) 

<u>Tips</u>: If you're running on Windows, it's recommended to install Virtual Box on windows Host and Vagrant + Ansible on WSL (windows subsystem for Linux)

# Installation

Before building the VM, you need to install extra ansible roles. Those roles will help download, install and configure all different layers. So the first command to run is: 

```bash
$ ansible-galaxy install -r provisioning/requirements.yml
```

Now you could use vagrant to build the stack via

```bash
$ vagrant up
```

It will take some minutes to download a minimal Debian image (version 9.x) and software packages.