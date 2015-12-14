# ansible-itop

Ansbile playbook to setup an iTOP environment with Apache and MariaDB.

### Operational System

This module was tested on Ubuntu 14.04.

### General Configuration

  This module was refactore from the previous version, which accepted just virtualhosts. Now it can also be used with single web server purpose.

  * Edit the hosts file to your host.
  * Change the variables in group_vars/all.
  * Run the ansible-playbook. Ex: ansible-playbook -b --ask-become-pass -k -i hosts site.yml (for running in localhost, with commom user over SSH).
  * Or run with the existing Vagrant file, just make a 'vagrant up' in the directory.
  * After the installation, runs http://yoursite.example.com/web and configure iTOP.

### Variables
  * vhost: True to use vhost, False to not.
  * fqdn: If using vhost, specifies the FQDN (itop.example.com).
  * dbname: MariaDB database for iTOP (do not use '-').
  * dbuser: MariaDB user for accessing the database.
  * dbpassword: MariaDB users's password.
  * mariadb_rootpass: MariaDB root's password.
  * install_teemip: Install or not TeemIP module.
  * install_module: Add write permissions to itop-config.php for installing modules
