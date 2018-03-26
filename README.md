ANSIBLE
-----------
# Running a playbook
## Playbook
`cat site.yml`
`ansible-playbook -i myhosts site.yml`

##Playbook breakdown
What happened here?
*	`--- denotes the beginning of a YAML file`
*	`hosts: host tells Ansible to run the tasks on the host host`
*	`become: true makes all your tasks run as sudo`
*	- name: is basically a comment, describing what the task does`
*	`apt: specifies the module we want to use`
*	`name: is an argument to the apt module, that specifies the name of the package to install.`
`To see all arguments for a specific module, allowed values, and other details, you can use the CLI documentation that is included with Ansible:`
`ansible-doc apt`
 
`To close the documentation, enter q in the terminal.`
---
`NOTE: This tutorial is using Ubuntu. If your own hosts are RHEL/CentOS, you should use the yum module instead.`
`Ansible ensures`
`If you run the playbook again, Ansible does the former, and instead of "Changed: 1", you will get "OK: 2, Changed 0". Try it out:`

`ansible-playbook -i myhosts site.yml`
 

Ensure a package is removed
Update the playbook to remove sysstat.

`sed -i -e 's/state: latest/state: absent/' -e 's/ensure.*/ensure sysstat is removed/' site.yml`

 

Then re-run the playbook:

`ansible-playbook -i myhosts site.yml`
