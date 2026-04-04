**MongoDB setup**     
**1. Installing MongoDB**    
To install MongoDB, execute the following commands in your terminal:    
Add MongoDB's GPG key and repository:    

curl -fsSL https://www.mongodb.org/static/pgp/server-7.0.asc | \
sudo gpg -o /usr/share/keyrings/mongodb-server-7.0.gpg \
--dearmor  
echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-7.0.gpg ] https://repo.mongodb.org/apt/ubuntu jammy/mongodb-org/7.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-7.0.list  

Install MongoDB:  
sudo apt update  
sudo apt install -y mongodb-org  

Enable and Start MongoDB service:  
sudo systemctl enable mongod  
sudo systemctl start mongod  

**2. Setting Up MongoDB**  
Install MongoDB Shell:  
Follow the installation guide at MongoDB Shell Installation.  

Access MongoDB Terminal:  
To interact with your MongoDB instance, open the MongoDB shell using:  

mongosh  

Manipulate Databases and Collections:  

Show databases:  
show dbs;  

Use a specific database:  
use db_name;  

Show collections in the database:  
show collections;  

Query the Products collection:  
db.Products.find().pretty();  

**PostgreSQL setup**  
**Installation**  
**1. Setting Up Python Virtual Environment**  
Install the Python 3.12 virtual environment package:  
sudo apt install python3.12-venv -y  

Create a virtual environment:  
python3 -m venv myenv  

Activate the virtual environment:  
source myenv/bin/activate  

Install required Python libraries from requirements.txt:  
First, ensure pip is installed:  
sudo apt install python3-pip -y  

Then, install the required libraries:  
pip3 install -r requirements.txt  

**2. Installing PostgreSQL**    
To install and set up PostgreSQL, follow these steps:  
Install PostgreSQL and additional tools:  
sudo apt-get install postgresql postgresql-contrib  

Start the PostgreSQL service:  
sudo systemctl start postgresql  

Enable PostgreSQL to start on boot:  
sudo systemctl enable postgresql  

**3. Setting Up PostgreSQL Database**  
Switch to the PostgreSQL user:  

sudo -i -u postgres  
psql  

Create a new PostgreSQL user:  
CREATE USER root WITH PASSWORD 'root';  

Create a new PostgreSQL database:  
CREATE DATABASE my_database;  

Grant all privileges on the database to the new user:  
GRANT ALL PRIVILEGES ON DATABASE my_database TO root;  

Connect to the new database:  
\c my_database  

Grant all privileges on the public schema to the user:  
GRANT ALL PRIVILEGES ON SCHEMA public TO root;  

Grant create privileges on the database to the user:  
GRANT CREATE ON DATABASE my_database TO root;  

**List all databases**    
\l  

**Connect to a database**  
\c your_database_name  

**List all schemas**  
\dn  

**List tables in current schema**  
\dt  

**List tables in specific schema**  
\dt schema_name.*  

**Describe table structure**  
\d table_name  

**Show data from table**  
SELECT * FROM table_name;  

Running the Application  
Once the environment and database are set up, you can run the application with the following steps:  

Ensure your virtual environment is activated:  
source myenv/bin/activate  

Run the application:  
python3 run.py  

The application will start, and you can access it via the specified host and port in your configuration.  

**MySQL setup**      
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
