# Docker

## Commands

? `docker-compose down --rmi all`  
Building image: `docker compose build`  
Starting container: `docker-compose up`  
Starting container as background process: `docker-compose up -d`  
Stopping container: `docker-compose stop`  
List docker images: `docker images` OR `docker image ls`  
Run docker image: `docker run hello-docker`  
Run docker image interactive*: `docker run -it hello-docker`  
*opens shell prompt  
See running containers: `docker ps `  
See all containers: `docker ps -a `  
Remove image: `docker rmi <your-image-id>`    
List environment variables: `printenv`  
Stop, build & start container:  
`docker-compose stop && docker-compose build && docker-compose up -d`

