**Java + Maven Application Build and Run**
sudo apt update
sudo apt upgrade
sudo apt install openjdk-17-jdk -y
sudo apt install maven -y
mvn compile (run where pom.xml is present) (target folder generated)
mvn test 
mvn package (jar file generated)
java -jar java-demoapp-1.0.0.jar 

![java-build](java-build.png)
![java-test](java-test.png)
![java-package](java-package.png)
![java-output1](java-output1.png)
![java-output2](java-output2.png)
![java-output3](java-output3.png)