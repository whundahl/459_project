# Docker Django Project for CSCI-459 

<p align="center">
  <a href="https://travis-ci.org/standard/standard"><img src="https://img.shields.io/travis/standard/standard/master.svg" alt="travis"></a>
  <a href="https://www.npmjs.com/package/standard"><img src="https://img.shields.io/npm/v/standard.svg" alt="npm version"></a>
  <a href="https://www.npmjs.com/package/eslint-config-standard"><img src="https://img.shields.io/npm/dm/eslint-config-standard.svg" alt="npm downloads"></a>
  <a href="https://tidelift.com/subscription/pkg/npm-standard?utm_source=npm-standard&utm_medium=readme"><img src="https://img.shields.io/badge/-dependencies%20ok-brightgreen.svg?colorA=58595b&style=flat&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABEAAAAOCAYAAADJ7fe0AAAAAXNSR0IArs4c6QAAAAlwSFlzAAAWJQAAFiUBSVIk8AAAAVlpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IlhNUCBDb3JlIDUuNC4wIj4KICAgPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4KICAgICAgPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIKICAgICAgICAgICAgeG1sbnM6dGlmZj0iaHR0cDovL25zLmFkb2JlLmNvbS90aWZmLzEuMC8iPgogICAgICAgICA8dGlmZjpPcmllbnRhdGlvbj4xPC90aWZmOk9yaWVudGF0aW9uPgogICAgICA8L3JkZjpEZXNjcmlwdGlvbj4KICAgPC9yZGY6UkRGPgo8L3g6eG1wbWV0YT4KTMInWQAAAVhJREFUKBV1kj0vBFEUhmd2sdZHh2IlGhKFQuOviEYiNlFodCqtUqPxA%2FwCjUTnDygkGoVERFQaZFlE9nreO%2BdM5u5wkifvuee892Pu3CyEcA0DeIc%2B9IwftJsR6Cko3uCjguZdjuBZhhwmYDjGrOC96WED41UtsgEdGEAPlmAfpuAbFF%2BFZLfoMfRBGzThDtLgePPwBIpdddGzOArhPHUXowbNptE2www6a%2Fm96Y3pHN7oQ1s%2B13pxt1ENaKzBFWyWzaJ%2BRO0C9Jny6VPSoKjLVbMDC5bn5OPuJF%2BBSe95PVEMuugY5AegS9fCh7BedP45hRnj8TC34QQUe9bTZyh2KgvFk2vc8GIlXyTfsvqr6bPpNgv52ynnlomZJNpB70Xhl%2Bf6Sa02p1bApEfnETwxVa%2Faj%2BW%2FFtHltmxS%2FO3krvpTtTnVgu%2F6gvHRFvG78Ef3kOe5PimJXycY74blT5R%2BAAAAAElFTkSuQmCC"></a>
  <a href="https://standardjs.com"><img src="https://img.shields.io/badge/code_style-standard-brightgreen.svg" alt="Standard - JavaScript Style Guide"></a>
</p>

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
