update-all-servers
=========

Ansible playbook to update any packages for all servers managed by Ansible that use apt and/or yum package managers.


How to Use
------------

To use this playbook just run this command.

	1. ansible-galaxy install -r requirements.yml -p roles/  
	2. ansible-playbook master.yml -e @vars/all_vars.yml -i /Users/Brad/.ansible/hosts


Requirements
------------

None

Variables
------------

Should the servers be rebooted if needed. The default is "no"
```
	reboot: "yes"
```

Roles
------------

	stancel.update-servers


Additional Info
------------

I have setup a bash profile alias to allow calling the playbook and choosing whether to reboot (yes/no as the first parameter argument)

```
alias update-all='function _update-all() { cd /Users/Brad/DevOps/Ansible_Playbooks/playbooks/update-all-servers; ansible-playbook master.yml -i /Users/Brad/.ansible/hosts --extra-vars "reboot=$1"; };_update-all'
```




