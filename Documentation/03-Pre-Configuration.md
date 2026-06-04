# Ubuntu Server Pre-Configuration

Before deploying osTicket, the Ubuntu server was prepared with the required web, database, and PHP components to support the application.

# Server Details:

Hostname: VM-Ticket01

Operating System: Ubuntu Server 22.04 LTS

IP Address: 192.168.10.20


# System Update

sudo apt update

sudo apt upgrade -y

- Updated the operating system and installed the latest security updates.


# Apache Installation & Verification

sudo apt install apache2 -y

sudo systemctl status apache2

- Installed and validated Apache web server for hosting the osTicket application.


# MariaDB Installation & Verification

sudo apt install mariadb-server -y

sudo systemctl status mariadb


Security configuration:

sudo mysql_secure_installation

- Installed and secured MariaDB database server for osTicket data storage.


# PHP Installation & verification

sudo apt install php php-mysql php-imap php-apcu php-intl php-common php-gd php-curl php-xml php-mbstring php-ldap php-zip php-bcmath -y
php -v

- Installed PHP runtime and required modules to support osTicket functionality.


# Service Validation

systemctl status apache2

systemctl status mariadb

php -v

- Validated all required services prior to application deployment.

