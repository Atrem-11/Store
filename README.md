# Store Server

#### Development and design of a Django server for an online clothing store.
#### Local development and server deployment.


## Stack

- [Python](https://www.python.org/downloads/)
- [Django](https://www.djangoproject.com/)
- [PostgreSQL](https://www.postgresql.org/)
- [Redis](https://redis.io/)
- [Celery](https://docs.celeryq.dev/en/stable/)

## Software

- [IDE](https://www.jetbrains.com/ru-ru/pycharm/) supported development in python using the django framework
- [PostgreSQL](https://www.postgresql.org/) DBMS
- Non-relational [Redis](https://redis.io/) database
- [Celery](https://docs.celeryq.dev/en/stable/) Asynchronous Task Queue

___

## Local Developing

#### All actions should be executed from the source directory of the project and only after installing all requirements.


1. Firstly, create and activate a new virtual environment:
    ``` python
    python3.9 -m venv ../venv
    source ../venv/bin/activate
    ```
2. Install packages:
    ``` python
    pip install --upgrade pip
    pip install -r requirements.txt
    ```
3. Run project dependencies, migrations, fill the database with the fixture data etc:
    ``` python
    ./manage.py migrate
    ./manage.py loaddata <path_to_fixture_files>
    ./manage.py runserver 
    ```
4. Run Redis Server:
    ``` python
    redis-server
    ```
5. Run Celery:
    ``` python
    celery -A store worker --loglevel=INFO
    ```
___

## Team

- [Артём Тимофеев](https://vk.com/rrtteemm) — Back-End Engineer, Dev-Ops Engineer
- [Екатерина Руденко](https://www.behance.net/f1a683e5) — Interface tester