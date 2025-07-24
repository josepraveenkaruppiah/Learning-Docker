## What is docker? 
- A docker is a layer of images that is stored in docker hub which a team of dev can pull for a development. 
- A docker image and container.
1. docker image is an offline docker
2. docker container is when an DKer image is being run using a port

## Cmds

1. pull - used to pull a docker image from docker hub
2. start - used to create a container using a docker image

3. Rrun - Buinds both pull and start
4. -d - run a container in a detached mode (background) logs and replies are not binded to the bash that is being used
5. stop - stop a container
6. ps - shows the running container
7. ps -a - shows the container history
8. -p<porta:portb> - port forwarding from PC to container.
9. logs - shows the log of a container
10. --name - used to give a name to a container while creating it.
11. exec -it - in terminal, used to open a terminal of a detached docker container.

## Docker project

run a backend, boot up the frontend, and crete a docker network. so containers can communicate with eachother in that network. 

_docker network_

docker network is a network to create for a container(s) to communicate with other container(s) and nodes using container name. 

## Docker compose
A docker compose is a YAML file where all the executable cmd is stored in a formate (syntax) so instead we run the file to up and down a container/netwwork. 

_to run_

docker-compose -f "filename" up/down

up is to host it, down is to go offline. 

## Docker file (Dockerfile)

Docker file is similar to compose file, where this file is used to create an image. the file is written using a certain syntax. 

    FROM <base image>

    ENV <environment variables>

    RUN mkdir -p /home/app (where you want the cmds to be running inside a container)

    COPY . /home/app (the files that is copied into an image)

    CMD ["image","file"] (any exec that has to be running on the host "outside the container")


_to run_

    docker build -t <name of the image:tag> <dir>
    docker rm <container id/name> (to remove a container)
    docker rmi <image id/name> (to remove a image)

    