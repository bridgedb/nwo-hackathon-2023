# Project 1: BridgeDb 3 Docker

* Lead: Marvin Martens

## Description
Up until the end of 2019, the BridgeDb service was made available as a Docker image. Since then, the new releases stopped and the code required major revision to work for newer versions of BridgeDb. This project is focused on making Docker images available for the latest version of BridgeDb, creating deployment guidelines and instructions how to build Docker images for the newer versions of BridgeDb. 

## Participants
* Marvin Martens
* Ozan Cinar
* Helena

## Notes
The GitHub repository for the BridgeDb Docker files: https://github.com/bridgedb/docker

The Docker build works, and the service works as intended, but only the API and not the user interface. 

First full Docker image pushed to DockerHub with all newest mapping files, but without Swagger UI: https://hub.docker.com/layers/bigcatum/bridgedb/3.0.14-ni/images/sha256-46752a7311985451b482500250278ecfa2a52b42b3f19c5631dfaa2538522206?context=explore

To-do: add automatic download of bridgedb-webservice-X.X.X.jar
To-do: add swagger configuration. Old code requited org.bridgedb.server.jar, and executed dist/bridgedbServer.jar within startup.sh

