# WAG-the-Blog

Ansible playbooks for setting up a LEMP stack for WordPress. This is heavily influenced by the wonderful Trellis by Roots. The main differences are WAG will use Percona instead of MariaDB; WAG adds the [Percona Toolkit](https://www.percona.com/software/mysql-tools/percona-toolkit) for MySQL; WAG uses UFW instead of ferm; and WAG emphasizes monitoring tools like dstat and htop a bit more than Trellis does.

## What's included

WAG-the-Blog will configure any Ubuntu 14.04 server with the following:

* Nginx (with FastCGI)
* PHP FPM
* Percona MySQL (a drop-in MySQL replacement)
* Composer
* WP-CLI
* Memcached
* UFW
* dstat 
* [glances](https://github.com/nicolargo/glances) installed via PIP
* htop
* sysstat

## Requirements

Make sure all dependencies have been installed before moving on:

* [Ansible](http://docs.ansible.com/ansible/intro_installation.html#latest-releases-via-pip) >= 2.0.0.2

