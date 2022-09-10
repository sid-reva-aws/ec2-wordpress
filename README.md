# ec2-wordpress
Deploying a WordPress website on AWS EC2:
This link provides information on how EC2 and RDS configuration is done on wp-config file once wordpress code is downloaded and extracted on EC2. The sample snapshots can be reviewed on below link:
https://www.linkedin.com/pulse/integration-aws-ec2-wordpress-using-rds-pratik-kohad

Step 1 - First, we need to launch an ec2 instance on AWS.
Step 2: we need to configure Apache WebServer.
  1. login to the EC2 instance.
  2. yum install httpd -y 
Step 3 -  Now install MYSQL.
Step 4 -  Now install php7.2 (amazon-linux-extras install php7.2 ).
Step 5 - Now Download WordPress.
  wget https://wordpress.org/latest.tar.gz
Step 6 - Now Extract the package.
  tar -xvzf latest.tar.gz -C  /var/www/html/
Step 7 - Setting up the /etc/httpd/conf/ httpd.conf file
  Making AllowOverride None to AllowOverride All
Step 8 - Setting Up the Amazon RDS instance.
  Setting Up name and password for the instance to access.
Step 9 - Now connect to the database using following command.
  mysql -h <endpoints of RDS INSTANCE> -u admin -p
Step 10 - Starting Httpd using CLI.
Step 11 - Use the following command to open WordPress.
  <IP>/wordpress
  after clicking on let's go it will direct you to the below page.
  After clicking on submit you will be directed towards contents to be copied to wp-config.php file.
  Copy the content from here and paste it into the wp-config.php file.
Step 12 - Copying content from WordPress to wp-config.php file.
  cat > /var/www/html/wordpress/wp-config.php
  cat /var/www/html/wordpress/wp-config.php
  Now click on Run the installation.
  You will be directed to the below page where you will be allowed to put the name and password.
Step 13 - Click on Install WordPress and then you will be directed towards the below page.
Step 13 - Now log in using credentials entered before.
  So our WordPress Application is Successfully Deployed.



