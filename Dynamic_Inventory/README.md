Setting up EC2 External Inventory Script With Ansible
======================================================
Step_01:
--------
Copy the ec2 external inventory script to /etc/Ansible/ec2.py and chmod +x it.
copy the ec2.ini file to /etc/Ansible/ec2.ini as well.

Step_02:
--------
For making a successful API call to AWS, you will need to configure Boto (the Python interface to AWS). There are a variety of methods available, but the simplest is to export the following environment variables:

	export AWS_ACCESS_KEY_ID='ABCD1234'
	export AWS_SECRET_ACCESS_KEY='CDEF5678'

You will also need to set up a few more environment variables to the inventory management script. 

	export ANSIBLE_HOSTS=/etc/ansible/ec2.py 
	export EC2_INI_PATH=/etc/ansible/ec2.ini

Note: "ANSIBLE_HOSTS" variable tells Ansible to use the dynamic EC2 script instead of a static "/etc/ansible/hosts" file.


Step_03:
--------
You can test the script to make sure your config is correct:

	cd /etc/ansible
	./ec2.py –list

As a result, you will be able to see the entire EC2 inventory across all regions in JSON.

Note:
-----
When you execute ec2.py script for the first time, some users facing the problem like:

	ERROR: "Forbidden", while: getting ElastiCache clusters

To get this problem rid off, just uncomment this line inside ec2.ini file.

	elasticache = False
