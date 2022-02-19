# Resume module service module

This is a module to manage resume from employees, it is possible to view, create and edit resume. 
The official swagger documentation related to the endpoints is found in http://localhost:8080/swagger-ui.html

## How to run it

### 1. Install Docker and Docker Desktop
It is neccesary to have docker installed in your computer in order to run the container 

### 2. Open a command prompt in the main root
In the main root, run the command "docker-compose up" in order to create the container, wait until finished

### 3. Connect to database server
Once the container is up, the next step is to go to the Pgadmin container in http://localhost:5050
The password for pgadmin is "admin". Once loaded, connect to server with the following parameters

HOST: resume-db
PORT: 5432
User: resume_module_user
Password: resume_itk

### 4. Load the database 
Once connected, load the database specified in the "resume-module-db.sql" using the query tool

### 5. Test endpoints
Now, to test the endpoints use http://localhost:8080/

## ENDPOINTS 

#### GET --> /employees/resumes
#### GET --> /employees/{employeeId}/resume
#### POST --> /employees/{employeeId}/resume
#### PUT --> /employees/{employeeId}/resume
#### PATCH --> /employees/{employeeId}/resume
#### 
#### GET --> /employees/{employeeId}/resume/technologies
#### GET --> /employees/{employeeId}/resume/technologies/{technologyId}
#### POST --> /employees/{employeeId}/resume/technologies
#### PUT --> /employees/{employeeId}/resume/technologies/{technologyId}
#### 
#### GET --> /employees/{employeeId}/resume/skills
#### GET --> /employees/{employeeId}/resume/skills/{skillId}
#### POST --> /employees/{employeeId}/resume/skills
#### PUT --> /employees/{employeeId}/resume/skills/{skillId}
#### 
#### GET --> /employees/{employeeId}/resume/education
#### GET --> /employees/{employeeId}/resume/education/{educationId}
#### POST --> /employees/{employeeId}/resume/education
#### PUT --> /employees/{employeeId}/resume/education/{educationId}
#### 
#### GET --> /employees/{employeeId}/resume/work-experience
#### GET --> /employees/{employeeId}/resume/work-experience/{workId}
#### POST --> /employees/{employeeId}/resume/work-experience
#### PUT --> /employees/{employeeId}/resume/work-experience/{workId}