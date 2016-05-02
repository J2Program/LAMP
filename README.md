# LAMP

#Install and Configure Apache2
sudo apt-get update
sudo apt-get install apache2

sudo nano /etc/apache2/mods-enabled/dir.conf

<IfModule mod_dir.c>
       DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
</IfModule>

#Install and Configure MySQL Server
sudo apt-get install mysql-server libapache2-mod-auth-mysql php5-mysql
sudo mysql_install_db
sudo mysql_secure_installation

#Install and Configure PHP5
sudo apt-get install php5 php5-mysql php-pear php5-gd  php5-mcrypt php5-curl

#Testing PHP5 and MySQL
In order to test PHP script you need to create simple PHP script in directory /var/www/html. in this case I’ll create phpinfo.php:

sudo touch /var/www/html/phpinfo.php
sudo nano  /var/www/html/phpinfo.php
Add the following line into file /var/www/html/phpinfo.php

<?php phpinfo(); ?>
Save and exit ( Ctrl + O, Ctrl + X)


http://ubuntuserverguide.com/2014/06/how-to-install-lamp-in-ubuntu-server-14-04-lts.html

#Start Service

/opt/lampp/lampp start
nautilus


