CLI_Playbook
=============
A playbook for variable implementation using "vars", "vars_files"
and "--extra-vars" in Ansible-Playbook.

HOW TO RUN PLAYBOOK:
====================
>>> To actually run the playbook, use the following command:

    ansible-playbook cli.yml --extra-vars="hostgroup=PROD"

NOTE: In this playbook, we are using variables using three different 
types:
  1. Using "vars"
  2. Using "vars_files"
  3. Passing a variable using command line.
