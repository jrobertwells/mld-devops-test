# MLD DEV/INFRA-OPS CONTAINER TASK
### Introduction

The task is to run a java application that is dependent on a CouchDB database via containers. 
We have prepared a project called 'notes' that can save and retrieve notes from a database. 

The java project provides a Rest API frontend to test against.

To build the project:

* Clone the project with ```git clone https://github.com/MyLifeDigital/mld-devops-test.git```.
* Build the project using gradle: ```<project path>/gradlew clean build``` or ```<project path>/gradlew.bat clean build``` if on windows.
* The jar will now be located in: ```<project path>/build/lib```
* to start the jar from the command line: ```java -jar notes-1.0-SNAPSHOT.jar```

The 'notes' project requires CouchDB to run, it will attempt connect to ```http://couchdb:5984/``` without a username/password (CouchDB starts with no authentication enabled). It will create the required database if it does not exist. It is best to initially run against a clean CouchDB.

CouchDB ```http://couchdb.apache.org/``` is a simple to run NOSQL database, further information can be found on the site, a number of docker images already exist on Docker Hub.

Upon starting the application (which requires an available database) you can navigate to ```http://<machineip>:8080/swagger-ui.html``` to see a detailed description of the API using Swagger.

To test, in the 'POST' section type in a string (anything) and press try, you should see a 200 and a GUID/ID as the response. Take the GUID and paste into the 'GET' section to retrive the details.

The 'notes' application will provide basic logging while running to help you solve any problems you may encounter.

### The task
We would like see a solution to run the 'notes' application using docker with CouchDB as its backend, the solution provided should enable us to run the 'notes' application as a container along with CouchDB on our machine. Please provide any supporting documentation.

If you go and look at ```https://docs.docker.com/install/linux/docker-ee/ubuntu/``` for Linux or ```https://docs.docker.com/docker-for-windows/install/``` for Windows
Google around on how to 'build a container in docker' and I would suggest pushing to dockerhub as the repo.

We will check the files/solutions provided, and if this meets the required standard you'll be invited to an interview. We may then discuss your solution in more detail. Solutions can be provided as a git repo, a zip or any other means.

Thank you

MLD Development Team
