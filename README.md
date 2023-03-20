Hello this Flask api simply represents some room temperature concept.

http://127.0.0.1:5051/api/room (POST)
http://127.0.0.1:5051/api/temperature (POST)
http://127.0.0.1:5051/api/average (GET)
http://127.0.0.1:5051/api/room/1 (GET)

Before you creating Postgresql you can dockerize or creating from your host. 

But I simply creating try https://www.elephantsql.com/ 

- Create an account
- Create postgresql free version.
- Copied expected postgresql connection string.

# Create .env file

touch .env

# Create value DATABASE_URL 

DATABASE_URL = {Expected postgresql connection string}

# Create .flaskenv file

* must enter app

FLASK_APP=app 

* Chose True or False

FLASK_DEBUG={True/False} 

# For building Dockerfile preapre expected environment

docker build -t flaskapp:0.1.4 . 

# For up your docker container

docker run -d -p 5051:5000 flaskapp:0.1.4

GO http://127.0.0.1:5051 ! 