# Ansible - task 2
This tasks goal is to deepen knowledge of ansible and start working with text files i.e. config files.    
With this task you will get familiar with **line**, **blockinfile** **insertafter** and some regex.


## Goals: ##
Write a playbook which: 
1. Installs apache2
2. Installs/updates to the newest version of apache2 Just like running `apt update && apt install` [See Material to read #1]
3. Copies an HTML static file which outputs "Hello world!" to the apache's dir **only if** apache is installed [See Material to read #3]
4. Modifies apache's config file by changing virtualhost port to 81 (Default is 80) [See Material to read #4]
5. Using **blockinfile** and **insertafter** do some changes to apache's config - change DocumentRoot, Alias etc. For example:

        DocumentRoot /var/www/

        Alias /html /var/www/html
        <Directory /var/www/html>
        AllowOverride All
        </Directory>

        Alias /html2 /var/www/html2
        <Directory /var/www/html2>
        AllowOverride All
        </Directory>

6. When the config is changed, make sure apache service is restarted in order to take changes into affect [See Material to read #5]
7. This time instead of using systemd, make the playbook a bit more tidy by implementing **notify** to restart service after changing config [See Material to read #2]

## Material to read ##
1. https://docs.ansible.com/ansible/latest/collections/ansible/builtin/apt_module.html
2. https://docs.ansible.com/ansible/latest/user_guide/playbooks_handlers.html
3. https://dev.to/setevoy/ansible-check-if-a-package-installed-on-a-remote-system-4402
4. https://docs.ansible.com/ansible/latest/collections/ansible/builtin/lineinfile_module.html
5. https://docs.ansible.com/ansible/latest/collections/ansible/builtin/systemd_module.html
