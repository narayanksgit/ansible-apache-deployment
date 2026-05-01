# 🚀 Ansible Apache Deployment

## 📌 Overview
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

##  Access
http://<target-ec2-public-ip>

<img width="1341" height="378" alt="image" src="https://github.com/user-attachments/assets/a6e62c20-3725-4381-b5d4-6d874e33f2bb" />



##  Author
Narayana KS
