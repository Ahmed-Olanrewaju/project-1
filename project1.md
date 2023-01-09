## Awesome Documentation of project 1

# INSTALLING APACHE AND UPDATING THE FIREWALL

`sudo apt update`

![sudo apt update](./Images/sudo-apt-update.png)

`sudo install apache2`

![sudo install apache2](./Images/sudo-apt-install-apache2.png)

`sudo systemctl apache2`

![apache status](./Images/apache-status.png)

`sudo systemctl enable apache2`

![sudo systemctl enable apache2](./Images/sudo-systemctl-enable-apache2.png)

`curl localhost`

`apache2 default page`

![apache2 default page](./Images/apache2-detault-page.png)

![curl localhost](./Images/curl-localhost.png)

# INSTALLING MYSQL

using ‘apt’ to acquire and install this software

`sudo apt install mysql-server`

![sudo apt install mysql-server](./Images/sudo-apt-install-mysql-server.png)

`sudo mysql`

![sudo mysql](./Images/sudo-mysql.png)

`ALTER USER root`

![ALTER USER root](./Images/ALTER-USER-root.png)

`mysql> exit`

![mysql> exit](./Images/mysql-exit.png)

`sudo mysql secure installation`

![sudo mysql secure installation](./Images/sudo%20mysql_secure_installation.png)

`sudo mysql -p`

![sudo mysql -p](./Images/sudo-mysql-p.png)


# INSTALLING PHP

You have Apache installed to serve your content and MySQL installed to store and manage your data. PHP is the component of our setup that will process code to display dynamic content to the end user. In addition to the php package, you’ll need php-mysql, a PHP module that allows PHP to communicate with MySQL-based databases. You’ll also need libapache2-mod-php to enable Apache to handle PHP files. Core PHP packages will automatically be installed as dependencies.

To install these 3 packages at once, run:

`sudo apt install php libapache2-mod-php php-mysql`

![sudo apt install php libapache2-mod-php php-mysql](./Images/sudo-apt-install-php-libapache2-mod-php-php-mysql.png)

`php v`

![php v](./Images/php-v.png)

# CREATING A VIRTUAL HOST FOR YOUR WEBSITE USING APACHE

In this project, you will set up a domain called projectlamp, but you can replace this with any domain of your choice.

Apache on Ubuntu 20.04 has one server block enabled by default that is configured to serve documents from the /var/www/html directory.
We will leave this configuration as is and will add our own directory next next to the default one.

Create the directory for projectlamp using ‘mkdir’ command as follows:

`sudo mkdir var www projectlamp`

![sudo mkdir var www projectlamp](./Images/sudo-mkdir-var-www-projectlamp.png)

`echo` 

![echo](./Images/echo.png)

`var www`

![var www](./Images/var-www.png)

`project lamp`

![project lamp](./Images/project-lamp.png)

`echo 1`

![echo 1](./Images/echo-1.png)

` sudo chown -R $USER:$USER /var/www/projectlamp`

![sudo chown R $USER](./Images/sudo-chown-R-%24USER.png)


`sudo vi /etc/apache2/sites-available/projectlamp.conf`

![udo vi /etc/apache2/sites-available/projectlamp.conf](./Images/sudo-vi%20-etc-apache2-sites-available-projectlamp.conf.png)

![`sudo vi`](./Images/sudo%20vi.png)

`VirtualHost`

![VirtualHost](./Images/VirtualHost.png)

`sudo ls etc apache2 sites available`

![sudo ls etc apache2 sites available](./Images/sudo-ls-etc-apache2-sites-available.png)

`sudo a2ensite projectlamp`

![sudo a2ensite projectlamp](./Images/sudo-a2ensite-projectlamp.png)

`sudo a2dissite 000-default`

![sudo a2dissite 000-default](./Images/sudo-a2dissite-000-default.png)

`sudo apache2ctl configtest`

![sudo apache2ctl configtest](./Images/sudo-apache2ctl-configtest.png)

`sudo systemctl reload apache2`

![sudo systemctl reload apache2](./Images/sudo-systemctl-reload-apache2.png)

`sudo echo 'Hello LAMP from hostname`

![sudo echo 'Hello LAMP from hostname](./Images/sudo-echo-Hello-LAMP-from-hostname.png)

# ENABLE PHP ON THE WEBSITE

With the default DirectoryIndex settings on Apache, a file named index.html will always take precedence over an index.php file. This is useful for setting up maintenance pages in PHP applications, by creating a temporary index.html file containing an informative message to visitors. Because this page will take precedence over the index.php page, it will then become the landing page for the application. Once maintenance is over, the index.html is renamed or removed from the document root, bringing back the regular application page.

`IfModule mod_dir.c>`

![IfModule mod_dir.c>](./Images/IfModule-mod-dir.c.png)

`sudo systemctl reload apache2`

![sudo systemctl reload apache2](./Images/sudo-systemctl-reload-apache-2.png)

`php`

![php](./Images/php.png)

`PHP server`

![PHP server](./Images/PHP-server.png)

`Hello LAMP from hostname`

![Hello LAMP from hostname](./Images/Hello-LAMP-from-hostname.png)