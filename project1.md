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

First full Docker image pushed to DockerHub with all newest mapping files, but without Swagger UI: https://hub.docker.com/layers/bigcatum/bridgedb/3.0.14-ni/images/sha256-46752a7311985451b482500250278ecfa2a52b42b3f19c5631dfaa2538522206?context=explore

After the first version without UI, with help of Egon and Helena we now have the new swagger UI as part of the Docker image.

Also, a GitHub action is created to make new builds and push these to DockerHub. --> todo: make the naming with version. (update GH action)
- push "latest" and with version
- version dynamic --> based on variable or input read from other file (Dockerfile or setup.sh)
- Activate action upon new ID mapping file release

To-do: add automatic download of bridgedb-webservice-X.X.X.jar instead of copy. 


