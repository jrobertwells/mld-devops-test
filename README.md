# MLD DEV/INFRA-OPS CONTAINER TASK
### Introduction

This is my solution for running a java application that is dependent on a CouchDB database via containers. 
It uses docker-compose and a dockerfile to build the containers.

To build the project:

* Clone the project with ```git clone https://github.com/jrobertwells/mld-devops-test.git```.
* Navigate to the project path: ```cd <project path>/gradlew clean build```
* Start the containers: ```docker-compose up```
* Connect to the Swagger UI via browser: ```http://<machineip>:8080/swagger-ui.html```

Thank you

Jonathan
