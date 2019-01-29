
### The Role/Playbook is provisioning resources on AWS.

#####Needs to install https://galaxy.ansible.com/geerlingguy/repo-epel

$ansible-galaxy install geerlingguy.repo-epel

### ec2.py Dynamic Inventory for EC2
https://www.devon.nl/en/ansible-dynamic-inventory-for-ec2/

group_vars/tag_ansible_group_webservers is responsible for the repository.
---
# Variables for the web server configuration

# Ethernet interface on which the web server should listen.
# Defaults to the first interface. Change this to:
#
#  iface: eth1
#
# ...to override.
#
iface: '{{ ansible_default_ipv4.interface }}'

# this is the repository that holds our sample webapp
repository: https://github.com/davidfirmino/site.git

# this is the appversion (git commit)
webapp_version: bcca0fa48ceb61a11c6ccba5b85830dc00f2fef7


### HOW TO USE


