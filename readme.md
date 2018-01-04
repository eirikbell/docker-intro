# Some handy commands #

## Remove all containers ##
docker rm -a $(docker ps -a -q)

## Remove all images ##
docker rmi $(docker images -q)