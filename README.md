Ansible Role: Common
=========
This ansible role contains common tasks like changing the hostname
and disabling swap.

Requirements
------------
None

Variables
------------
New Hostname:
```
common_hostname: ""
```

Disable swap:
```
common_disable_swap: true
```

Example Playbook
------------
```
- hosts: all
  vars:
    - common_hostname: myhost
  roles:
    - jamslinger.common
```

License
------------
MIT
