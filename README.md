# asynchronus-rest-service-django-celery


## Introduction

This is an example of asynchronus microservice using django and celery. Redis is used as broker.


### Prerequisite

*   Django==1.9.1
*   Celery==3.1.19 (Cipater)
*   Redis==3.0.1

### How to run
To migrate and run the redis server

	$ cd async_service
	$ python manage.py makemigrations
	$ python manage.py migrate
	$ redis-server &
	
To run django server

	$ python manage.py runserver
Curl to the endpoint

	$ curl -i http://localhost:8000/ping/
To view the celeryd log

	$ python manage.py celeryd -l info

To see the list of tasks in Redis

	$ redis-cli
	$ 127.0.0.1:6379> keys *




 
