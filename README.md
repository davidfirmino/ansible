- Install https://galaxy.ansible.com/geerlingguy/repo-epel
$ ansible-galaxy install geerlingguy.repo-epel

- ec2.py Dynamic Inventory for EC2
https://www.devon.nl/en/ansible-dynamic-inventory-for-ec2/

- group_vars/tag_ansible_group_webservers is responsible for the repository.

This is the repository that holds our sample webapp
repository: https://github.com/davidfirmino/site.git

This is the appversion (git commit)
webapp_version: bcca0fa48ceb61a11c6ccba5b85830dc00f2fef7

- HOW TO USE

1 - Deploy the infrastructure (AWS) 
- Configure ec2.ini (AWS Credentials)
- Configure group_var/all (AWS Credentials)

2 - Install the application

ansible-playbook -i ec2.py install-application.yml -b --key-file "instance-keypair-name"

3 - To update the application use

ansible-playbook -i ec2.py application-update.yml -b --key-file "instance-keypair-name"
