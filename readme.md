# Docker Django Project for CSCI-459

### Requirements 
Defined in src/equirements.pip
- Django 1.10  
- gunicorn 19.6.0  
- psycopg2 2.7.5
- celery 4.2.1
- redis 2.10.6

### Basic Usage of Application 
To start the project locally, run these two commands:

With the help of Makerfile:
1. First run `make build` inside root directory.
2. Then run `make up` to start up the project for first time.

### Architechture Behind the Docker-django Web App
I have worked with django several times before and the web framework provides a ModelViewController architectural pattern, making it a fairley easy framework to develop with. I find myself using python for more projects each day and this one is no different. Django when coupled with redis and postgreSQL, presents a microservice architectural pattern. 

Finally, I realized that there is a need to have a fully deployable application without the hassle of having to set up the boilerplate code each time, with the architecture I define. Of course, every project is different and needs a defined architechture but when working with several django projects it can be hard to spin up new instances of differnt applications because of the need to create a virtual environment for development. Docker solves this for us, and provides us with a way to test and develop many applications at one time from a single machine. Additionally, It makes for easier deployment. 



### Makefile Commands
To use this project, run this commands:

1. `make up` to build the project and starting containers.
2. `make build` to build the project.
3. `make start` to start containers if project has been up already.
4. `make stop` to stop containers.
5. `make shell-web` to shell access web container.
6. `make shell-db` to shell access db container.
7. `make shell-nginx` to shell access nginx container.
8. `make logs-web` to log access web container.
9. `make logs-db` to log access db container.
10. `make logs-nginx` to log access nginx container.
11. `make collectstatic` to put static files in static directory.
12. `make log-web` to log access web container.
13. `make log-db` to log access db container.
14. `make log-nginx` to log access nginx container.
14. `make restart` to restart containers.
