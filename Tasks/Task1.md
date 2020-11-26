# Ansible - task 1
This task goal is to get familiar with ansible.    
With this task you will get familiar with playbook(s), how to write them and their execution.

In order to start working with ansible, I strongly advise to create some VM's in order to not execute playbooks in your own machine and also keep in mind that one of ansible's main feature is managing multiple machines with one playbook at once.

## Goals: ##
1. Create some VM's. 2 or 3 is enough (pro tip: create VM, install some linux distro (ex. debian) and clone them to have several machines).
2. Populate hosts file with your VM's.
3. Create a custom directory in user's home directory
Write a playbook which: 
4. Copies 1 file to the custom directory on one machine
5. Copies 1 file to the custom directory on all machines
6. Copies 3 files to the custom directory on all machines using **with_items** block
7. Add step which overwrites a file only if in machine A (one of whichever) file does not exist yet. Basically - don't overwrite

## Material to read ##
1. https://docs.ansible.com/ansible/latest/collections/ansible/builtin/copy_module.html
2. https://docs.ansible.com/ansible/latest/collections/ansible/builtin/items_lookup.html