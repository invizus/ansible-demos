# Ansible demo
This is the simplest playbook that demonstrates:
 - inventory (hosts and groups)
 - playbook and tasks

### before running playbook:
 - install ansible (either `sudo pip install ansible` or `sudo apt install ansible`)
 - must have account on target servers (see inventory.ini, you can replace those servers with the ones you have access to)
 - ideally must have sudo rights, or comment out `become: yes` line in playbook.yml if you do not have them.
 - must copy public ssh key to target servers, i.e. `ssh-copy-id 192.168.0.1`

### To run:

`ansible-playbook playbook.yml -i inventory.ini -u anakin --limit server-a --check --ask-become`

Explanation:

`--limit` - will run playbook for only one server

`--check` - will not execute commands remotely, but will check if commands succeed. dry run.

`-u` - specifies which user to login as

`--ask-become` - sudo password

`-i` - specifies which file to use as inventory

Run same without `--check` and `--limit` to make changes on all remote servers:

`ansible-playbook playbook.yml -i inventory.ini -u anakin --ask-become`

## Going further
See what else can you do with ansible https://docs.ansible.com/ansible/latest/collections/index_module.html
