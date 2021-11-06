# Welcome to Your First Configuration Management Session!

I hope you have set up your development environment. [Next: **Prerequisites** ➡️](prerequisites.md)

## List of Ad-Hoc Commands that we used in the sessions

General Structure:

```bash
ansible <host-pattern> [options]

ansible <inventory> -m <modulename> -a <arguments to the module>
```

```bash
ansible localhost -m command -a uptime  

ansible webservers -m yum -a “name=httpd state=latest”

ansible appserver -m user “name=opsschool group=admins append=yes shell=bin/bash”

ansible localhost -m setup

ansible-inventory -i inventory --list

ansible -i inventory  web -m file -a "dest=~/opsschool mode=755 state=directory" 

ansible -i inventory  web -m file -a "dest=~/opsschool/ansible mode=755 state=directory" 

ansible localhost -m user -a "name=opsschool password=0p$Sch00l home=/opsschool" -b  

ansible localhost -m file -a  "path=~/.test  mode=755 owner=ubuntu state=touch" 
```
