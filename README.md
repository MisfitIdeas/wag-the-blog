# WAG-the-Blog

WAG is an Ansible playbook for setting up a LEMP stack for WordPress. It is heavily influenced by the wonderful [Trellis](https://github.com/roots/trellis) by [Roots](https://roots.io), but is intentionally incomplete in some respects and tries to paint enough of the canvas that WordPress developers who are new to Ansible can see where it is going, while also leaving enough of the details missing that users will have to get their hands dirty with Ansible. 

Out of the box for production purposes, Trellis is certainly a better bet. WAG is not intended to be used for anything production out of the box.  The goal of WAG is to showcase enough of Ansible that WordPress developers can get an idea of what they can do with it...without actually doing all of it. We all learn by doing and WAG wants users to fork it and play with it and make it work for them

Unlike Trellis, WAG uses [Percona MySQL](https://www.percona.com) instead of MariaDB. WAG also adds the [Percona Toolkit](https://www.percona.com/software/mysql-tools/percona-toolkit) for MySQL. WAG uses UFW instead of ferm. And WAG places a bit more emphasis on monitoring tools like dstat and htop. As a WordPress developer, you might stumple into an Ansible framework like Trellis that makes a lot of really good decisions. You might not agree with all of them, though, or maybe your needs are just a little bit different. If you haven't used Ansible before, modfiying something like Trellis for your needs might be a bit daunting. Hopefully, WAG will be easy for new Ansible users to start working with and gain exposure. But if it isn't, or if you see any way that it could be made better, please feel free to submit a PR or open an issue. 

## What's included in WAG

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

Before using WAG, you will need to make sure that you have Ansible installed on your computer. You will also need to modify `inventory/host_vars/wag-the-blog` with the SSH info of your host. You should also modify the MySQL password in `inventory/host_vars/wag-the-blog` and make sure you change the root user password for MySQL. 

To run this playbook, you will run `ansible-playbook -i inventory/hosts wordpress.yaml` from your command line. 
