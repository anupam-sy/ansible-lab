TagIMPL_Playbook
================
A playbook to implement tagging in ansible-playbooks.

HOW TO RUN PLAYBOOK:
====================
>>> To DRY Run the playbook (Means, To make sure everything will 
execute as expected), Use the following command:

    ansible-playbook tag.yml --check

>>> To actually run the playbook with a prticulat task, use the 
following command:

    ansible-playbook tag.yml -tags treepackage 

>>> To skip some tags, use the "--skip-tags" run the playbook
like this:

    ansible-playbook tag.yml --skip-tags treepackage
