
### The Role/Playbook is provisioning resources on AWS.

#####Needs to install https://galaxy.ansible.com/geerlingguy/repo-epel

$ansible-galaxy install geerlingguy.repo-epel

### ec2.py Dynamic Inventory for EC2
https://www.devon.nl/en/ansible-dynamic-inventory-for-ec2/

##group_vars/tag_ansible_group_webservers is responsible for the repository.

# this is the repository that holds our sample webapp
repository: https://github.com/davidfirmino/site.git

# this is the appversion (git commit)
webapp_version: bcca0fa48ceb61a11c6ccba5b85830dc00f2fef7

### HOW TO USE


