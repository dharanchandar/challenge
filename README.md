# Wirecard Configuration Management Challenge
These playbooks will deploy a very basic implementation of Tomcat Application Server, version 8, and deploy the war file into tomcat.

It has been defined into two roles

1)	install and configure tomcat
2)  deploy

If you want to perform tomcat installation and deployment on the hosts mentioned in hosts file, please execute the following

ansible-playbook -i hosts main.yml 

or if you want only the deployment and restarts , please execute below

ansible-playbook -i hosts main.yml --tags "deploy, restart"

After deployment restarts will be handled using handlers and its tags

We can edit the hosts file as per the target host and the vars has to be changed with 


