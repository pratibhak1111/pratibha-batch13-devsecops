**MYSQL**  
1. Update and Upgrade Packages  
sudo apt update  
sudo apt upgrade -y  
This ensures your system has the latest package information and security patches.  
________________________________________  
2. Install MySQL Server  
sudo apt install mysql-server -y  
This installs the latest MySQL server package available in Ubuntu’s repository.  
________________________________________  
3. Check MySQL Service Status  
systemctl status mysql  
If not running, start it with:  
sudo systemctl start mysql  
sudo systemctl enable mysql  
________________________________________  
4. Secure the MySQL Installation [OPTIONAL FOR LOCAL]  
Run the included security script:  
sudo mysql_secure_installation  
It will ask you to:  
•	Configure the VALIDATE PASSWORD PLUGIN (you can choose strength level).  
•	Set a root password (if not already set).  
•	Remove anonymous users.  
•	Disallow remote root login.  
•	Remove test database.  
•	Reload privilege tables.  
________________________________________  
5. Log into MySQL  
sudo mysql -u root -p  
Enter the password you set during the secure installation.  
________________________________________

6. Create a Database  
CREATE DATABASE bankappdb;  
________________________________________
7. Create a User and Grant Privileges  
CREATE USER 'adi'@'localhost' IDENTIFIED BY 'Test@123';  
ALTER USER 'adi'@'localhost' IDENTIFIED WITH mysql_native_password BY 'Test@123';   
FLUSH PRIVILEGES;  

GRANT ALL PRIVILEGES ON bankappdb.* TO 'adi'@'localhost';  
FLUSH PRIVILEGES;  

<img width="1918" height="966" alt="image" src="https://github.com/user-attachments/assets/2db61801-23e7-4f29-903c-09f58380d177" />  
<img width="1917" height="970" alt="image" src="https://github.com/user-attachments/assets/1534fcf0-c39e-4bdf-86ad-8bbc5c292c4e" />  
<img width="1912" height="830" alt="image" src="https://github.com/user-attachments/assets/4ba9b2ec-23d7-41b9-88d6-85bb59d88ca3" />
<img width="1008" height="727" alt="image" src="https://github.com/user-attachments/assets/57c25767-870d-4f5c-ac99-239d19350774" />


