VaultImpl_Playbook
==================
A playbook for implementation of Ansible-Vault.

TO ENCRYPT A FILE:
==================
>>> To encrypt a file, use the following command:

    ansible-vault encrypt <filename.yml>    

HOW TO RUN PLAYBOOK:
====================
>>> To actually run the playbook, use the following command:

    ansible-playbook --ask-vault-pass vartest.yml

NOTE: The above statement will ask for the ansible-vault
password. After entering the correct password, playbook
will be executed. Otherwise you will get the following 
error:
    
    ERROR! Attempting to decrypt but no vault secrets found 
