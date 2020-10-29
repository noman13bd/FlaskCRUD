# FlaskCRUD

# how to run 
1. clone the repo and cd into that folder
2. `python3 -m venv env`
3. `source env/bin/activate`
4. now run the following commands:
    - `python3 app.py db init`
    - `python3 app.py db migrate`
    - `python3 app.py db upgrade`
5. `sudo docker-compose up --build -d`
6. POST REQUEST
    ```
    curl --location --request POST 'http://127.0.0.1:5000/persons' \
    --header 'Content-Type: application/json' \
    --data-raw '{
        "name": "FT",
        "age": "32"
    }'
    ```
7. GET REQUEST
    ```
    curl --location --request GET 'http://127.0.0.1:5000/persons' \
    --header 'Content-Type: application/json' \
    --data-raw ''
    ```

8. GET a person REQUEST
    ```
    curl --location --request GET 'http://127.0.0.1:5000/person/1' \
    --header 'Content-Type: application/json' \
    --data-raw ''
    ```
9. UPDATE a person REQUEST
    ```
    curl --location --request PUT 'http://127.0.0.1:5000/person/1' \
    --header 'Content-Type: application/json' \
    --data-raw '{
        "name": "FTop",
        "age": "3"
    }'
    ```

10. DELETE a person REQUEST
    ```
    curl --location --request DELETE 'http://127.0.0.1:5000/person/1' \
    --header 'Content-Type: application/json' \
    --data-raw ''
    ```

# how to develop from scratch
1. create directory
2. cd into that directory
3. create virtual environment
4. activate the virtual env
    - `python3 venv env`
5. now install the following
    - `pip install Flask`
    - `pip install Flask-SQLAlchemy`
    - `pip install Flask-Migrate`
    - `pip install Flask-Script`
    - `pip install psycopg2-binary`
6. then create the Dockerfile
7. create docker-compose.yml
8. `pip freeze > requirements.txt`
9. then create the model and necessary CRUD operations
10. now run the following commands:
    - `python3 app.py db init`
    - `python3 app.py db migrate`
    - `python3 app.py db upgrade`