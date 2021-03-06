PostgreSQL for Development
==========================

[![GitHub](https://img.shields.io/github/license/honatas/ansible-role-postgresql-dev?style=plastic)](https://github.com/Honatas/ansible-role-postgresql-dev/blob/master/LICENSE)
[![Travis](https://img.shields.io/travis/honatas/ansible-role-postgresql-dev?style=plastic)](https://travis-ci.org/Honatas/ansible-role-postgresql-dev "View the build status on Travis")
[![Ansible Quality Score](https://img.shields.io/ansible/quality/48294?style=plastic)](https://galaxy.ansible.com/honatas/postgresql_dev)
[![coffee](https://img.shields.io/badge/buy%20me%20a-coffee-brown?style=plastic)](https://ko-fi.com/honatas "Buy me a coffee")  

Ansible role for a very basic installation of [PostgreSQL](https://www.postgresql.org) better suited for development environments, especially [Vagrant](https://www.vagrantup.com) boxes. It installs the database and the command-line client, and enables remote access so you can also connect a client from outside the Vagrant virtual machine (such as [DBeaver](https://dbeaver.io/) from your host machine - just remember to configure port forwarding on your vagrantfile).  

The software is installed from PostgreSQL's PPA, documented [here](https://www.postgresql.org/download/linux/ubuntu/).  

PostgreSQL is installed as a systemd service named **postgres**.


Role Variables
--------------

**postgres_version**: Version of PostgreSQL to be installed.  
Default: 12  

**postgres_ubuntu_version**: Version name of the Ubuntu where PostgreSQL is going to be installed.  
Default: focal


Example Playbook
----------------

Default installation
```yaml
roles:
  - honatas.postgresql_dev
```

Installs PostgreSQL 11 on Ubuntu 18.04
```yaml
roles:
  - { role: honatas.postgresql_dev, postgresql_version: 11, postgresql_ubuntu_version: bionic }
```


Dependencies
------------

None

Requirements
------------

None

License
-------

MIT


Contributions
-------------

Feel free to open an issue or add a pull request. Anytime. Really, I mean it.  

Also, if you like my work, I'll let you know that I love [coffee](https://ko-fi.com/honatas).  
