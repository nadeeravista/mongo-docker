# Overview
This is a simple docker file for you to spin up a mongodb server

## Installation steps

###### Prerequests
You must have installed Docker in your system. If you are using a Mac, the Docker Desktop is the ideal tool [Docker Desktop](https://www.docker.com/products/docker-desktop)

###### Installation
Clone or download the code

Run the following command inside the directory
```
docker-compose build && docker-compose up -d
```

###### Server settings
You may specify the port you need to run the mongodb. Also you can sepcify the volume location if you nee persistant data each time when you spinup the docker
docker-compose.yml
```
    ports:
        - '27017:27017'
    volumes: 
        - ./data/mongo:/data/db
```
Your can then access the database server on localhost:27017
