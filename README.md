# Django-Todolist

Django-Todolist is a todolist web application with the most basic features of most web apps, i.e. accounts/login, API and (somewhat) interactive UI.

---
CSS | [Skeleton](http://getskeleton.com/)
JS  | [jQuery](https://jquery.com/)

## Explore
Try it out by installing the requirements. (Works only with python >= 3.8, due to Django 4)

    pip install -r requirements.txt

Create a database schema:

    python manage.py migrate

And then start the server (default: http://localhost:8000)

    python manage.py runserver


Now you can browse the [API](http://localhost:8000/api/)
or start on the [landing page](http://localhost:8000/)

## Task
#### Prerequisites
- Fork this repository

#### Requirements

1. Prepare a docker-compose file that will build and start both MySQL db and Todolist app
2. Remove RUN python manage.py migrate as the database is no longer available at the build time
3. Refactor ENTRYPOINT to execute both db migration and application start. Example:
`ENTRYPOINT ["sh", "-c", “command1 && command2”]`
4. The application should work with no issues after running docker-compose up
5. Update the README.md file by adding a new section with instructions on how to run and stop containers with docker-compose
6. Todos should be stored in MySQL Database, with a persistent volume connected
7. Create PR with your changes and attach it for validation on a platform



## Running and Stopping the Application with Docker Compose
### Starting the Application
To start the application and all its dependent services, you can use the following command from the root of the project:
'docker-compose up'. If you prefer to run the containers in the background, you can use the -d flag: 'docker-compose up -d'

### Stopping the Application
To stop the application and all the related services, you can use the following command:
'docker-compose down'





