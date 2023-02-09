# Project 1: BridgeDb 3 Docker

* Lead: Marvin Martens

## Description
Up until the end of 2019, the BridgeDb service was made available as a Docker image. Since then, the new releases stopped and the code required major revision to work for newer versions of BridgeDb. This project is focused on making Docker images available for the latest version of BridgeDb, creating deployment guidelines and instructions how to build Docker images for the newer versions of BridgeDb. 
Also we want to automate the building of new Docker images and improve the documentation of deployments.

## Participants
* Marvin Martens
* Ozan Cinar
* Helena

## Notes
The GitHub repository for the BridgeDb Docker files: https://github.com/bridgedb/docker

The Docker build works, and the service works as intended, but only the API and not the user interface. 

Step 1 was the creation of a working Docker image with the new BridgeDb version and newest ID mapping files, and pushing it to Dockerhub, which was done, but without UI. 

After the first version without UI, with help of Egon and Helena we now have the new swagger UI as part of the Docker image. There were 2 issues with the swagger.json file at the start:
- The URL was hardcoded to a localhost URL, which made deployments elsewhere (server, or on other ports) not work
- There were internal CORS issues, stopping the connection between the UI and the webservice

The first issue was resolved by including an environment variable in the "startup.sh" which can be entered through the `docker run` command (see below)
The second issue was resolved by Helena and Ammar, adding a "*" somewhere. 

Automation of the Docker image building and pushing to DockerHub:
A GitHub action is created to make new builds and push these to DockerHub. It pushes the Image with 2 different tags: 1 with "latest" and 1 with the current BridgeDb version, which is automatically parsed from the "setup.sh" file. The action is automatically started if the Dockerfile, setup.sh or startup.sh files are updated, or if the ID mapping files in https://github.com/bridgedb/data are updated, which then sends out a ping to the build action. 

To pull the latest version of the Docker image:
```
sudo docker pull bigcatum/bridgedb:latest
```

To run the image:
```
sudo docker run --name bridgedb -p [PORT1]:8080 -p [PORT2]:8183 -e SERVER_URL='[SERVER_URL]:[PORT2]' bigcatum/bridgedb:3.0.14
```


Remaining goals (future):
- add automatic download of bridgedb-webservice-X.X.X.jar instead of copy
- make the URL in swagger.json automatically filled out, without environment variable


