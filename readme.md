# Some handy commands #

## Remove all containers ##
docker rm -a $(docker ps -a -q)

## Remove all images ##
docker rmi $(docker images -q)

## Check container standard out ##
docker logs -f <container id>

## Enter container ##
docker exec -it <container id> /bin/bash

## Perform any command against a running container ##
docker exec -it <container id> sudo ls /var/log/

## Get info about a running container ##
docker inspect <container id>