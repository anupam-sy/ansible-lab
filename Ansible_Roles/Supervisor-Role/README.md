supervisor-role
===============

An ansible role for the installation of Supervisor on Ubuntu(14,16) and CentOS(6,7).

Requirements
------------

None

Role Variables
--------------

```
ConfigVars:
  - conf_filename: "service01"
    command: "/usr/local/bin/long01.sh"
    stderr_logfile: "/var/log/long.err01.log"
    stdout_logfile: "/var/log/long.out01.log"

  - conf_filename: "service02"
    command: "/usr/local/bin/long02.sh"
    stderr_logfile: "/var/log/long.err02.log"
    stdout_logfile: "/var/log/long.out02.log"

```

Dependencies
------------

None

Example Playbook
----------------

A playbook to use the role.

```
---
  - hosts: hostgroup/host
    become: true
    roles: 
      - supervisor-role
```

License
-------

BSD

Author Information
------------------

```
Name: Anupam Yaadav
Email: anupam.yaadav@gmail.com
```
