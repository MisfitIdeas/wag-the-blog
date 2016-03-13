# WAG-the-Blog

Ansible playbooks for setting up a LEMP stack for WordPress. This is heavily influenced by the wonderful [Trellis](https://github.com/roots/trellis) by [Roots](https://roots.io/)

## What's included

WAG-the-Blog will configure any Ubuntu 14.04 server with the following:

* Nginx (with FastCGI)
* PHP 7.0
* Percona MySQL (a drop-in MySQL replacement)
* Composer
* WP-CLI
* Memcached
* ufw
* dstat 
* [glances](https://github.com/nicolargo/glances) installed via PIP
* htop
* sysstat

## Requirements

Make sure all dependencies have been installed before moving on:

* [Ansible](http://docs.ansible.com/ansible/intro_installation.html#latest-releases-via-pip) >= 2.0.0.2

