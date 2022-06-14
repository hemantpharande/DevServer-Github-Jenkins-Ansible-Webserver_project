# DevServer-Github-Jenkins-Ansible-Webserver_project

In this project developer develope code in developer server and push it in to github repository. Jenkins automatically detect this commit and build job and this build job file automatically send in to ansible server. Ansible server copy this file and send it in to webserver by triggering ansible playbook. Ansible playbook copy this file and send it in to web server.

1. First Start 4 server for this project. 1-> DevServer 2-> Jenkins-server 3-> Ansible-Server 4-> Web-Server 
2. SSH to Jenkins Server and install java, git and jenkins s/w on it. Start Jenkins Server.
3. SSH Ansible server and install python, ansible software on it.
4. On Ansible server add private ip address of web server to  etc/ansible/hosts this file location.
5. Also ssh-keygen command create ssh authentication and send .pub file to host using ssh-copy-id command.
6. Start pasword authentication using etc/ssh/sshd-config file updation. "systemctl restrt sshd" Use this command for restarting sshd daemon.
7. on web server instance install httpd server. and start it.
8. On jenkins server install pluggins "publish to ssh". and add jenkins server and ansible server password authentication on it.
9. Create jenkins job with freestyle type.
  Add git hub repo url.
  
