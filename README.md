# server-playground

## Installation
```
pip3 install ansible
```

## Useful Ad-Hoc Commands
```
# docs
ansible-config list
ansible-doc -l 

# get host configs
export ANSIBLE_INVENTORY=inventory/local
export SERVER_GROUP=cloud
ansible $SERVER_GROUP -m ansible.builtin.ping
ansible $SERVER_GROUP -m ansible.builtin.setup -a "filter=ansible_env,ansible_architecture"
ansible $SERVER_GROUP -m ansible.builtin.include_role -a "name=base_server"
```
