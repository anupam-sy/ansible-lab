VarImplementation_Playbook
==========================
A playbook for variable implementation in Ansible-Playbook.

HOW TO RUN PLAYBOOK:
====================
>>> To DRY Run the playbook (Means, To make sure everything will 
execute as expected), Use the following command:

    ansible-playbook vartest.yml --check

>>> To actually run the playbook, use the following command:

    ansible-playbook vartest.yml

NOTE: Use "vars" for inbuilt variable in playbook and to pass
a variable file, use "vars_files".
