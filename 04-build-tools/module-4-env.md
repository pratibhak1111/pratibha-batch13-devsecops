**Module 4 – Environment Setup
Installed Development Tools**

**Java**
java -version
openjdk version "17.0.18"
**Maven**
mvn -version
Apache Maven 3.8.7

**Steps :**
sudo apt update
sudo apt upgrade
sudo apt install openjdk-17-jdk -y
sudo apt install maven -y
mvn compile (run where pom.xml is present) (target folder generated)
mvn test 
mvn package (jar generated)
java -jar java-demoapp-1.0.0.jar 

<img width="1907" height="972" alt="image" src="https://github.com/user-attachments/assets/20709430-93eb-43d4-a6b7-f6bb086b6213" />
<img width="1918" height="575" alt="image" src="https://github.com/user-attachments/assets/b8f44ede-3e0c-4fca-8742-730907a1812d" />

***********************************************************
**Node.js**
node -v
v18.17.0
NPM
npm -v
9.6.7
Python
python3 --version
Python 3.10.12
Pip
pip3 --version
pip 22.0.2
Python Virtual Environment
python3 -m venv test-env
.NET SDK
dotnet --version
7.0.401

<img width="1133" height="682" alt="image" src="https://github.com/user-attachments/assets/aab934a2-5781-4362-ad5b-df4afb55c3e6" />
issue i get 
<img width="1595" height="253" alt="image" src="https://github.com/user-attachments/assets/d09d429c-0425-454f-b791-0ae74bec885e" />
This Maven error occurs because Maven does not know where to deploy the artifact.

The maven-deploy-plugin requires a repository configuration in the distributionManagement section of your pom.xml.


