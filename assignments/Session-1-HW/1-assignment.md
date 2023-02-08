# Assignment #1

## Part 1 - Classwork

1. Build an inventory file with a named group (the name makes no difference):
    add `node1` to the group with an ip address
    set ssh user for this group
    set nother variable with a value that is not an ansible variable: something made up like MYVAR
    set a group variable for the group you have created

2. Run ad hoc commands that will do the following:

    - Using the file module - create the following directories on the web group:
    ~/opsschool
    ~/opsschool/ansible
    /etc/opsschool

    - With the User module create a user:
    name: opsschool
    homedir: /opsschool


3. Create your a playbook that installs docker on the nodes:

    How to install docker - [here](https://docs.docker.com/engine/install/ubuntu/)

    - Install required packages
    - Update the apt package index
    - Add docker’s official GPG key
    - Add docker apt repo
    - Update the apt package index
    - Install docker
    - Restart docker
    - Use handlers to restart service

    it is preferable to run specific modules rather the built in shell/command module per task.


## Part 2

Create a playbook that does the following:

  1. Using the file module, create a file on the nodes with the following content:
  ``` I am a text file I exist on the nodes ```
  2. Add a task to archive the file to a tar.gz archive
  3. Delete the original file
  4. Use wget to download the result of <http://icanhazip.com> on the nodes. Your result should be a local index.html file with your public IP as its content.
  5. convert both ad hoc commands you ran in section 1.2 to playbook tasks and run them as part of the playbook.

## Part 3
  1. Create a dynamic inventory out of your current nodes - no matter what method (preferably [EC2_plugin](https://docs.ansible.com/ansible/latest/collections/amazon/aws/aws_ec2_inventory.html))
  2. Edit your docker install playbook (created in section 1.3), add the following shell command as an extra task: 
  ```sudo docker run -d -p 8080:80 nginx```
  3. Run the playbook on your dynamic inventory - both nodes
  4. To check your success, in your browser navigate to <<node_public_ip>>:8080
  5. Come prepared to talk about why step 2 of this assignment is bad practice

  ** Note: make sure the nodes' security group allows access over port 8080
