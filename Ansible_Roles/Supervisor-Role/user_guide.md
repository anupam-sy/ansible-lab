User Guide:
===========
We are assuming the below mentioned directory structure for this role:

```
AnsibleRoles /
	- ansible.cfg
	- inventory / hosts
	- roles / supervisor-role / role-dirs (Like defaults, tasks, handlers etc.)
	- runner.yml
```

Execution:
----------
To execute this ansible role, we need three files:

1) ansible.cfg:
---------------
This is the configuration file for ansible to work with.

Example:

```
[defaults]

# Path of inventory file
inventory = /home/vagrant/SupervisorRole/inventory/hosts
# The forks parameter controls how many hosts are configured by Ansible in parallel.
forks     = 5
```

2) inventory:
-------------
This is the hosts file inside which we define all the hosts on which our role/playbook
will execute.

Example:
```
[Ubuntu14]
192.168.33.36 ansible_user=vagrant

[Ubuntu16]
192.168.33.60 ansible_user=vagrant

[CentOS6]
192.168.33.51 ansible_user=vagrant

[CentOS7]
192.168.33.52 ansible_user=vagrant
```

3) runner-playbook
------------------
This is playbook to run our ansible-role.

Example:
```
---
  - hosts: Ubuntu16
    become: true
    roles:
      - supervisor-role
```