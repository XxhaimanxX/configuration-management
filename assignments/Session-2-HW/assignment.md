# Assignment

1. Convert the docker playbook you created in the previous assignment to a role that will install docker, and run nginx.
2. Convert all shell/command tasks to use the modules (for instance docker module).
3. Use conditionals to make the role generic – the role should be able to install docker on ubuntu/redhat distributions
4. Use a variable list to pass the list of users that should be added to docker group as part of the install process. The default users should be ubuntu/ec2-user depending on the distribution type. The role should allow one user or more on each run.
5. Add a redhat server to the ubuntu servers you already have from session 1, and test your role on both ubuntu and redhat with different docker versions.
6. Make sure your new node is also a part of your dynamic inventory.
7. Bonus Round: Modify the role to install a specific version on docker (not only the latest), the user will be able to pick a version to install, and the role will have a specific version as the default.

# 🏁 That it your'e done!🏁 

![Done!](https://media.giphy.com/media/3o7qDEq2bMbcbPRQ2c/giphy.gif?cid=ecf05e47ehhssxpgmqeeqhoqj9xsmnx8gh7vnjlfgnejjsxy&rid=giphy.gif&ct=g)