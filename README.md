# News Crawler
---

# Description
---
This Project crawls new articles from https://hackernews.api-docs.io via the publicly available endpoints.

# Getting Started
---
1. This project heavily depends on redis and postgres. Hence make sure both are installed and running on your machine
2. Start a project in your desired IDE and create a virtual environment.
3. activate your virtual environment and run `pip install -r requirements.txt` to install the environmental dependencies
4. create an env file and input values for
   1. SECRET_KEY
   2. DB_USER
   3. DB_PASS
   4. DB_NAME
   
   for example, DB_USER=postgres
5. run `python manage.py migrate` to apply database schema
6. run `python manage.py runserver` to make sure the app is running
7. To begin task scheduling, run the two commands in separate terminals
   1. `celery -A config beat -l info`
   2. `celery -A config worker -l info`
8. After a little while, open you application on a browser (`127.0.0.1:8000`), you should start seeing news entries being populated.


