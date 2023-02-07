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

ansible webservers -i hosts -m shell -a "whoami" 

ansible webservers -i hosts -m shell -a "cat /proc/meminfo|head -2" 

ansible nodes -m group -a "name=somegroup state=present" 

ansible nodes -m group -a "name=somegroup state=present" -b

ansible nodes -m group -a "name=somegroup state=absent" -b


ansible webservers -m shell -a "cat /etc/passwd|grep -i ubuntu" -b -K

ansible nodes -i hosts -m user -a "name=opsschool group=opsschool shell=bin/bash createhome=yes" -b

ansible appserver -m user “name=opsschool group=admins append=yes shell=bin/bash”

ansible localhost -m setup

ansible-inventory -i inventory --list

ansible -i inventory  web -m file -a "dest=~/opsschool mode=755 state=directory" 

ansible -i inventory  web -m file -a "dest=~/opsschool/ansible mode=755 state=directory" 

ansible localhost -m user -a "name=opsschool password=0p$Sch00l home=/opsschool" -b  

ansible localhost -m file -a  "path=~/.test  mode=755 owner=ubuntu state=touch" 

```
