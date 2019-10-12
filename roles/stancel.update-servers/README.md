update-servers
=========

Basic Ansible role to update any packages for servers that use apt and/or yum package managers

Requirements
------------

None

Role Variables
--------------

Should the servers be rebooted if needed. The default is no.
```
	update_servers_reboot: "no"
```
Dependencies
------------

None

Example Playbook
----------------

	- hosts: all
	  vars_files:
	    - vars/main.yml
	  roles:
	    - stancel.update-servers


or 


	- hosts: all
	  vars:
		update_servers_reboot: "yes"
	  roles:
	    - stancel.update-servers

License
-------

BSD

Author Information
------------------

[Brad Stancel](https://github.com/stancel)
