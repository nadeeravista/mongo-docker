# Overview
This is a simple docker file for you to spin up a MongoDB server

## Installation steps

##### Prerequests
You must have installed Docker in your system. If you are using a Mac, the Docker Desktop is the ideal tool [Docker Desktop](https://www.docker.com/products/docker-desktop)

##### Set the settings and Install
- You may specify the port you need to run the mongodb. Also you can sepcify the volume location if you nee persistant data each time when you spinup the docker
docker-compose.yml
```
    ports:
        - '27017:27017'
    volumes: 
        - ./data/mongo:/data/db
```
- If you have specified a volumes, then share the host computer volume directory using Docker Desktop 
Settings -> Resources -> File Sharing -> Add your host file directory

- Run the following command inside the directory
```
docker-compose build && docker-compose up -d
```

Your can then access the database server on localhost:27017
