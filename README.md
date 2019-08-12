# README
## IP address
```34.220.149.207```
## URL
```http://narquie.com```
## Software Installed
See requirements.txt for python packages installed.

###Install:
1. apache2 (the wsgi to host the Flask site)
2. libapache2-mod-wsgi (The library in apache2 that works with Flask and python 2 to host the site.
3. postgresql
4. git
5. virtualenv (through pip)

## Configurations Made
1. Update the software on the Ubuntu server.
2. Create a firewall (ufw) that allows only 2200, 80, and 123 but do not enable yet.
3. Change the ssh port from 22 to 2200 in the /etc/ directory.
4. Enable ufw.
5. Create grader user and give them sudo through their user directory (users can sudo if they have the appropriate file in their directory).
6. Create ssh pair on local computer (Windows) with ssh-keygen.
7. Update lightsail to accept ssh from a public key.
8. Configure timezone to UTC
9. Use apt to both update and upgrade
10. Install dependencies listed in ```Install``` above.
11. Clone the ```fsnd-catalog``` project folder to a new folder in ```/home/srv/```
12. Run ```database_setup.py```
13. Run ```lotsofboardgames.py```
12. Change ```project.py``` file name to ```__init__.py```
13. Add ```project.wsgi``` to ```fsnd-catalog``` folder which imports from ```catalog``` directory.
14. Create a ```.conf``` file in apache2 directory ```/sites-available/``` to direct apache2 to the right server configuration.
15. Give the ```.conf``` file the ip address and the location of project.wsgi, /catalog/static, and /catalog/templates and log access.
16. Enable all ```.conf``` files with ```a2enmod```
17. Point ```default-000.conf``` to ```project.wsgi```
18. Add ```require all granted``` to ```<Directory>``` in ```apache2.conf``` file.
19. Add read and execute permissions to all files in ```/home/srv/fsnd-catalog/```
20. Change the location of the database in __init__.py to ```/home/srv/fsnd-catalog/catalog/boardgameswithcategorieswithusers.db```	 
21. Run sudo service apache2 restart
22. Point Google and Facebook dev apps to ```narquie.com```

## Third-Party Resources
[Digital Ocean](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps) was a great source of help, as were the resources in the full stack nanodegree at Udacity.
[Stack Overflow](https://www.stackoverflow.com) Has been instrumental in debugging.
Thanks to my mentor Zheng W. who was there for the moments where I was having trouble debugging.