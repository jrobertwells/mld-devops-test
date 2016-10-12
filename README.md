# MLD DEV-OPS CONTAINER TASK
### Introduction

The task is run a java application that is dependent on CouchDB database via containers. 
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

The 'notes' application will provide basic logging while running to help you solve any problems you may encounter.

###The task
We would like see the 'notes' application running in a docker container, along with CouchDB as its backend, with a solution provided to enable us to start and run the 'notes' appliation with CouchDB on our machine. Please provide any supporting documentation.

We will check the files/solutions provided, and if this meets the required standard you'll be invited to an interview. We may then discuss your solution in more detail.

Thank you

MLD Development Team