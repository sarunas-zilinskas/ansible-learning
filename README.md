# Ansible #
### What is this repository for? ###

This template is created so one could clone it and start using it straight away. It includes ansible config, some examples of daily used tasks and all of it in a structured tree.

### Tasks ###
In this repo, you can find folder with task*.md file. My idea, unlike Marius's is that each task should be done in one week. These tasks are not hard enough to struggle for weeks and they do have a structure where difficulty gradually increases so you should be fine with one task per week.

All of the goals defined in tasks should be achieved in sequence, that is, at first write a playbook which achieves goal no. 1, then go on for the 2nd etc. Your playbook should mature during the development of your playbook.
### How do I get set up? ###

* Install ansible locally
* Clone this repository
* Change ansible.cfg or hosts file if needed
* And start using it staright away!

### How do I execute playbooks? ###
* Execute ansible playbooks by simply executing command i.e.:   
`ansible-playbook playbooks/some_playbook.yml -i 192.168.0.1, -k -t tagname -v`

* `ansible-playbook` invokes the ansible executable
* `playbooks/some_playbook.yml` defines the playbook and its path to it
* `-i` parameter defines the machine on which the playbook will be executed for example:    
`-i virtualmachine.somedomain.com` or   
`-i 192.168.0.1,`   
**NOTE: bring attention to the comma if IP address is being used as otherwise ansible will interpret it as inventory name!**

`-k` parameter is used for asking SSH password instead of using ssh key-pair. Keep in mind that you need to install sshpass prior to executing playbook(s).
Install sshpass with: `sudo apt install sshpass`

`-t` parameter defines the tag to use. You don't neccessarily need to run the whole playbook, most of the times you will need to execute only a part of it (ex. check if all cron jobs are in place and not messed with). In order to do that, you should tag steps which are neccessary for particular job and execute playbook with that tag.

`-v` parameter defines the verbosity level. Max level is `-vvvv` which stands for `very very very verbose`. Most of the times you would want `-vv` or in case you are really deep into some crap then use `-vvv`.
### Who do I talk to? ###

* Šarūnas Žilinskas, DevOps engineer: sar.zilinskas@gmail.com