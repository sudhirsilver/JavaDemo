HealthyMe

This is a personal health tracking web application which provides a single interface for maintaining weight, blood sugar and blood pressure parameters.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

The application uses the below prerequisite softwares to run:
1. Apache Tomcat: This is the web container used to host the web application.
2. MySQL 5.3: This is the database software used to store the details of the users.


### Installing

1. Clone the project from GitLab into a working directory using the command:

git clone http://topgear-training-gitlab.wipro.com/SANGG4/DevOpsProfessional_Batch2_Capstone_HealthyMe.git

2. Create the MySQL docker container using the commands specified in the file "docker commands.txt" under the below folder:

<WORKING_DIRECTORY>/src/main/resources/

3.
a. Once the MySQL container is created, open a bash shell using the command:

     docker exec -it <mysql_container_name> bash

b. Create the MySQL database using the commands specified in the file HealthyMe_mysql_create.sql in the folder:

     <WORKING_DIRECTORY>/src/main/resources/

c. Check if the database is created properly.

4. Open the project cloned in <WORKING_DIRECTORY> as a Maven project in Eclipse IDE.

5. Check and update the db.properties file as required under the folder:

<WORKING_DIRECTORY>/src/main/resources/

6. Check and update the project POM.xml file under <WORKING_DIRECTORY> to suit the local Tomcat server settings.


7. Build and deploy the Maven project using the Run As -> Maven Build option with the below goal:

  tomcat7.deploy -Dtomcat.username=admin -Dtomcat.password=admin

***Modify the username and password as per the local Tomcat settings.

8. Once the project is built and deployed into the Tomcat web container, start the Tomcat server using the command:

  ./<TOMCAT_HOME_FOLDER>/bin/startup.sh

9. Launch the web browser and point the browser to the below URL:
  http://localhost:<tomcat_port>/HealthyMe

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Built With

Java/J2EE 1.8
Apache Tomcat 8.5
MySQL 5.3

## Authors

Sudhir MK
Kiran Kumar
Sangeetha S

## Acknowledgments

Avinash Patel (TT Architect Academy)
Prakash Ramamurthy (TT Architect Academy)
Raghavendran Sethumadhavan (TT Architect Academy)
