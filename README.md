#   Ansible Apache Deployment

##  Overview
This project demonstrates automated deployment of an Apache web server on AWS EC2 using Ansible.

##  Architecture
Ansible Control Node → SSH → Target EC2 → Apache Deployment

##  Technologies Used
- AWS EC2
- Ansible
- Linux (Amazon Linux 2023)
- Apache (httpd)

##  How it Works
1. Ansible control node connects to target EC2 via SSH
2. Apache package is installed using Ansible playbook
3. Apache service is started and enabled
4. Custom index.html is deployed
5. Web server becomes accessible via browser

##  Files
- inventory.ini → Target server details
- install_apache.yml → Ansible playbook

## running Ansible Playbook -

[ec2-user@ip-172-31-6-192 ansible-apache-deployment]$ ansible-playbook -i inventory.ini install_apache.yml PLAY [Install and configure Apache web server] ************************************************************************************************************************* TASK [Gathering Facts] ************************************************************************************************************************************************* [WARNING]: Platform linux on host 172.31.25.177 is using the discovered Python interpreter at /usr/bin/python3.9, but future installation of another Python interpreter could change the meaning of that path. See https://docs.ansible.com/ansible-core/2.15/reference_appendices/interpreter_discovery.html for more information. ok: [172.31.25.177] TASK [Install Apache package] ****************************************************************************************************************************************** changed: [172.31.25.177] TASK [Start and enable Apache service] ********************************************************************************************************************************* changed: [172.31.25.177] TASK [Deploy custom index page] **************************************************************************************************************************************** changed: [172.31.25.177] PLAY RECAP ************************************************************************************************************************************************************* 172.31.25.177 : ok=4 changed=3 unreachable=0 failed=0 skipped=0 rescued=0 ignored=0 [ec2-user@ip-172-31-6-192 ansible-apache-deployment]$

##  Access
http://<target-ec2-public-ip>



<img width="1341" height="378" alt="image" src="https://github.com/user-attachments/assets/a6e62c20-3725-4381-b5d4-6d874e33f2bb" />



##  Author
Narayana KS
