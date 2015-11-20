# ansible-itop

Ansbile playbook to setup an iTOP environment with Apache and MariaDB.

### Operational System

This module was tested on Ubuntu 14.04.

### General Configuration

This module was created with multiple virtualhosts in mind, to easily create fresh install for development (customization) of iTop.
The virtualhost name it's gonna be the concatenation of the below variables: itop_instance+domain.

  * Edit the hosts file to your host.
  * Change the variables in group_vars/all.
  * Run the ansible-playbook. Ex: ansible-playbook -b --ask-become-pass -k -i hosts site.yml (for running in localhost, with commom user over SSH).
  * After the installation, runs http://yoursite.example.com/web and configure iTOP.

### Variables
  * itop_instance: name of the instance. 
  * domain: domain name.
  * dbname: MariaDB database for iTOP (do not use '-').
  * dbuser: MariaDB user for accessing the database.
  * dbpassword: MariaDB users's password.
  * mariadb_rootpass: MariaDB root's password.
  * install_teemip: Install or not TeemIP module.
  * install_module: Add write permissions to itop-config.php for installing modules
