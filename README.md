# dissertation
#Installing the control website for my dissertation project

#The site uses a simple LAMP stack to facilitate login.

1. Create Ubuntu 18.04 box in Azure.
2. Add Public IP as A record in AWS R53.
3. SSH to box and install LAMP - https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-ubuntu-18-04
4. Add correct virtual hosts entry - https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-18-04#step-5-%E2%80%94-setting-up-virtual-hosts-(recommended)
5. Connect to DB and insert statement - 
  CREATE TABLE users (
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    username VARCHAR(50) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL,
    created_at DATETIME DEFAULT CURRENT_TIMESTAMP
);

6. Use Wget on get-php-files.sh and run script.

#HTTPS

7. Add LetsEncrypt Certificate - https://www.digitalocean.com/community/tutorials/how-to-secure-apache-with-let-s-encrypt-on-ubuntu-18-04

#HSTS

8. Add STS header - https://itigloo.com/security/how-to-configure-http-strict-transport-security-hsts-on-apache-nginx/
