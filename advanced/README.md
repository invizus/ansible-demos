# Ansible demo
This playbook demonstrates use of variables in host_vars. The idea is:
 - inventory keeps the list of hosts or environments
 - host_vars and group_vars hold configuration
 - roles automate stuff

### before running playbook:
 - install ansible (either `sudo pip install ansible` or 
   `sudo apt install ansible`)

 - must have account on target servers (see inventory.ini, you can replace
   those servers with the ones you have access to)

 - must have sudo rights
 - must copy public ssh key to target servers, i.e.
   `ssh-copy-id hostname.example.com`

### To run:

`ansible-playbook playbook-nginx.yml -u username`

or `ansible-playbook playbook-nginx.yml -u username --ask-become` if you need
to provide sudo password.

