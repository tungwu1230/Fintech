# 需放入user data的部分
---
#!/bin/bash
sudo yum update -y  
sudo amazon-linux-extras install -y lamp-mariadb10.2-php7.2 php7.2  
cat /etc/system-release  
sudo yum install -y httpd mariadb-server  
sudo systemctl start httpd  
sudo systemctl enable httpd  
sudo systemctl is-enabled httpd  
sudo usermod -a -G apache ec2-user  
groups  
sudo chown -R ec2-user:apache /var/www  
sudo chmod 2775 /var/www && find /var/www -type d -exec sudo chmod 2775 {} \;  
find /var/www -type f -exec sudo chmod 0664 {} \;  
echo "<?php phpinfo(); ?>" > /var/www/html/phpinfo.php  
sudo yum list installed httpd mariadb-server php-mysqlnd  
sudo systemctl start mariadb  
sudo yum install php-mbstring -y  
sudo systemctl restart httpd  
sudo systemctl restart php-fpm  
cd /var/www/html  
wget https://files.phpmyadmin.net/phpMyAdmin/4.9.7/phpMyAdmin-4.9.7-all-languages.tar.gz  
mkdir phpMyAdmin && tar -xvzf phpMyAdmin-4.9.7-all-languages.tar.gz -C phpMyAdmin --strip-components 1  

---
## 最後手動執行的部分
缺密碼  
sudo mysql_secure_installation  
Y  
Y  
Y  
