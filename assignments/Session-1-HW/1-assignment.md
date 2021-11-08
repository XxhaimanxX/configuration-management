# Assignment #1

## Part 1

1. Create a dynamic inventory out of your current nodes - no matter what method
2. Edit the docker_setup.yml playbook, add the following shell command to it as part of a task ```sudo docker run -d -p 8080:80 nginx```
3. Run the playbook on your dynamic inventory - both nodes
4. To check your success, in your browser navigate to <<node_public_ip>>:8080

** Note: make sure the nodes' security group allows access over port 8080

## Part 2

1. Using the file module, create a file on the nodes with the following content:
``` I am a text file I exist on the nodes ```
2. Add a task to archive the file to a tar.gz archive
3. Delete the original file
4. Use wget to download the result of http://icanhazip.com on the nodes. Your result should be a local index.html file with your public IP as its content.