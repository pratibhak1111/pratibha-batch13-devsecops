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
<img width="1905" height="968" alt="image" src="https://github.com/user-attachments/assets/a565624f-a8db-4645-9dc2-1ad54d8f026c" />    
<img width="1918" height="768" alt="image" src="https://github.com/user-attachments/assets/97a4b2dd-5069-450c-bb5e-44253565325b" />  
<img width="1918" height="963" alt="image" src="https://github.com/user-attachments/assets/c9e0f719-d59c-4e5d-9399-f0b9a0384475" />  
<img width="478" height="662" alt="image" src="https://github.com/user-attachments/assets/3c963626-8eb4-465f-974e-10d160bf27ec" />  
