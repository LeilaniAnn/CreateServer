# CreateServer

How will I complete this project?
This project is linked to the Configuring Linux Web Servers course.

Launch your Virtual Machine with your Udacity account. Please note that upon graduation from the program your free Amazon AWS instance will no longer be available.
Follow the instructions provided to SSH into your server
#Create a new user named grader
```adduser grader sudo```
Give the grader the permission to sudo
```adduser grader sudo```
Update all currently installed packages
```apt-get upgrade```
Change the SSH port from 22 to 2200
```nano /etc/ssh/sshd_config ```
Configure the Uncomplicated Firewall (UFW) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123)
(http://askubuntu.com/questions/59458/error-message-when-i-run-sudo-unable-to-resolve-host-none)
Turn UFW on with the default set of rules:
```$ sudo ufw enable```
*Check the status of UFW:
```$ sudo ufw status verbose```
Allow incoming TCP packets on port 2200 (SSH):
```$ sudo ufw allow 2200/tcp```
Allow incoming TCP packets on port 80 (HTTP):
```$ sudo ufw allow 80/tcp```
Allow incoming UDP packets on port 123 (NTP):
```$ sudo ufw allow 123/udp```
Configure the local timezone to UTC
Install and configure Apache to serve a Python mod_wsgi application
Install and configure PostgreSQL:
Do not allow remote connections
Create a new user named catalog that has limited permissions to your catalog application database
Install git, clone and setup your Catalog App project (from your GitHub repository from earlier in the Nanodegree program) so that it functions correctly when visiting your server’s IP address in a browser. Remember to set this up appropriately so that your .git directory is not publicly accessible via a browser!
You may also find this Getting Started Guide helpful when working on Project 5.
