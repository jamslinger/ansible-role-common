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

Update `/etc/hosts` file:
```
common_update_hosts_file: true
```
**Important:** This will replace the entire hosts file. You can add 
additional entries via `common_host_entries`:
```
common_host_entries:
  - ip: 10.0.0.1
    host: my-host
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
