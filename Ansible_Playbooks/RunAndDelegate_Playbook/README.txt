RunAndDelegate_Playbook
=======================
A playbook for the implementation of run_once in Ansible-Playbook.

HOW TO RUN PLAYBOOK:
====================
>>> To DRY Run the playbook (Means, To make sure everything will 
execute as expected), Use the following command:

    ansible-playbook runonce.yml --check

>>> To actually run the playbook, use the following command:

    ansible-playbook runonce.yml

NOTE: In this playbook, Task01(Creation of file01.txt) will be 
executed only on first host of group PROD whereas Task02(Creation
of file02.txt) will be executed on both the hosts mentioned in 
host group PROD.

>>> To change the default property of "run_once", use the 
"delegate_to".

    ansible-playbook delegateto.yml
