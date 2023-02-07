# Assignment #1

## Part 1 - Classwork

1. Build an inventory file with a “web” group:
add `node1` to the group with an ip address
set ssh user for this group

2. Create a playbooks that runs the following tasks on the web group:

- Using the file module - create the following directories on the web group:
~/opsschool
~/opsschool/ansible
/etc/opsschool

- With the User module create a user with a password:
name: opsschool
password: 0p$Sch00l
homedir: /opsschool

3. Create your a playbook to set up docker on the nodes:

How to install docker - [here](https://docs.docker.com/engine/install/ubuntu/)

- Install required packages
- Update the apt package index
- Add docker’s official GPG key
- Add docker apt repo
- Update the apt package index
- Install docker
- Restart docker
- Use handlers to restart service

it is preferable to run specific modules rather the built in shell modules per task.


## Part 2

1. Create a dynamic inventory out of your current nodes - no matter what method (preferably EC2_plugin)
2. Edit your docker setup playbook (created in section 1.3), add the following shell command to it as part of a task ```sudo docker run -d -p 8080:80 nginx```
3. Run the playbook on your dynamic inventory - both nodes
4. To check your success, in your browser navigate to <<node_public_ip>>:8080
5. Come prepared to talk about why step 2 of this assignment is bad practice

** Note: make sure the nodes' security group allows access over port 8080

## Part 3

1. Using the file module, create a file on the nodes with the following content:
``` I am a text file I exist on the nodes ```
2. Add a task to archive the file to a tar.gz archive
3. Delete the original file
4. Use wget to download the result of <http://icanhazip.com> on the nodes. Your result should be a local index.html file with your public IP as its content.
