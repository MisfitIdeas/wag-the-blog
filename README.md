# WAG-the-Blog

Ansible playbooks for setting up a LEMP stack for WordPress. This is heavily influenced by the wonderful Trellis by Roots. The main differences are WAG will use Percona instead of MariaDB; WAG adds the [Percona Toolkit](https://www.percona.com/software/mysql-tools/percona-toolkit) for MySQL; WAG uses UFW instead of ferm; and WAG emphasizes monitoring tools like dstat and htop a bit more than Trellis does. Trellis is much more fully featured than WAG at the moment. WAG is intentionally sparse in several places so that users who are new to managing their Website with Ansible can jump in and start adding to the project started. For the most part, WAG tries to be simple and avoid lower-level configuration. One exception to this is the use of tersmitten's [Ansible Percona Server](https://github.com/Oefenweb/ansible-percona-server) and [Ansible Percona Toolkit](https://github.com/Oefenweb/ansible-percona-toolkit). Termitten extended prior works on deploying Percona MySQL via Ansible in a very comprehensive and usable way and there is simply no reason to avoid reinventing that wheel when their work can be incorporated with a simple install from Ansible Galaxy. 

## What's included

WAG-the-Blog will configure any Ubuntu 14.04 server with the following:

* Nginx (with FastCGI)
* PHP FPM
* Percona MySQL (a drop-in MySQL replacement)
* Perconal Toolkit
* UFW
* dstat 
* [glances](https://github.com/nicolargo/glances) installed via PIP
* htop
* sysstat

## Requirements

Make sure all dependencies have been installed before moving on:

* [Ansible](http://docs.ansible.com/ansible/intro_installation.html#latest-releases-via-pip) >= 2.0.0.2

