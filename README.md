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

firewall-cmd --list-all
```

## Useful Modules
```
Schema: https://github.com/ansible/ansible-lint/tree/main/src/ansiblelint/schemas
ansible.builtin.user
ansible.builtin.group
ansible.builtin.known_hosts
ansible.builtin.slurp
ansible.posix.authorized_key
ansible.builtin.service
ansible.builtin.dnf
ansible.builtin.yum
ansible.builtin.copy
ansible.builtin.lineinfile
ansible.builtin.command
ansible.builtin.shell
ansible.posix.firewalld
ansible.builtin.uri
ansible.builtin.set_fact
ansible.builtin.debug
ansible.builtin.file
ansible.builtin.fail
ansible.builtin.fetch
ansible.builtin.blockinfile
ansible.builtin.stat
ansible.posix.synchronize
ansible.builtin.template
ansible.builtin.import_playbook
ansible.builtin.import_tasks
ansible.builtin.include_tasks
ansible.builtin.import_role
ansible.builtin.reboot
ansible.builtin.package_facts
ansible.builtin.yum_repository
ansible.builtin.rpm_key
ansible.posix.at
ansible.builtin.cron
ansible.builtin.systemd
ansible.posix.mount
ansible.builtin.hostname
```

## Concepts
```
variables: https://rol.redhat.com/rol/app/courses/rh294-9.0/pages/ch03
secrets: https://rol.redhat.com/rol/app/courses/rh294-9.0/pages/ch03s03
loops: https://rol.redhat.com/rol/app/courses/rh294-9.0/pages/ch04
handlers: https://rol.redhat.com/rol/app/courses/rh294-9.0/pages/ch04s03
when: https://rol.redhat.com/rol/app/courses/rh294-9.0/pages/ch04s07
jinja: https://rol.redhat.com/rol/app/courses/rh294-9.0/pages/ch05s03
host_vars: https://rol.redhat.com/rol/app/courses/rh294-9.0/pages/ch06
ansible-galaxy: https://rol.redhat.com/rol/app/courses/rh294-9.0/pages/ch07s05
collections: https://rol.redhat.com/rol/app/courses/rh294-9.0/pages/ch07s07
system-roles: https://rol.redhat.com/rol/app/courses/rh294-9.0/pages/ch07s09
pre-tasks: https://rol.redhat.com/rol/app/courses/rh294-9.0/pages/ch07s11
troubleshooting: https://rol.redhat.com/rol/app/courses/rh294-9.0/pages/ch08s02
redhat.rhel_system_roles.storage: https://rol.redhat.com/rol/app/courses/rh294-9.0/pages/ch09s07
edhat.rhel_system_roles.network: https://rol.redhat.com/rol/app/courses/rh294-9.0/pages/ch09s09
```
