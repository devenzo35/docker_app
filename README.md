# docker_app



## Docker Commands

```bash
docker run imagen         # Runs a container from an image
docker run -d imagen      # Runs a container from an image in the background
docker run -p 5000:5000   # Synchronizes Docker server with local
docker ps                 # Lists active containers
docker ps -a              # Lists all containers
docker stop contenedor    # Stops a container
docker start contenedor   # Starts a stopped container
docker rm contenedor      # Removes a container
docker images             # Lists downloaded images
docker rmi imagen         # Removes an image
docker pull imagen        # Downloads an image from Docker Hub
docker exec -it cont bash # Accesses the container with bash
docker logs contenedor    # Displays container logs
docker build -t nombre .  # Creates an image from a Dockerfile
docker-compose up -d      # Starts services defined in docker-compose
docker-compose down       # Stops and removes the services

# SHARING IMAGES ON DOCKERHUB

docker login
docker tag [image_name] [username/image_name]
docker push image_name

# DOCKER NETWORK

docker network create [network_name]
docker run -d \
--network docker_app --network-alias mysql \
-v postgreSQL_data/var/lib/mysql  \ 'we load the DB volume here'
-e POSTGRES_ROOT_PASSWORD=secret \ 'this image provides these keys for connection'
-e POSTGRES_DATABASE=db_name \
mysql:5.7

# NOW THAT VERSION OF MYSQL (mysql:5.7) IS IN THAT NETWORK (docker_app) AND WE CAN ADD MORE IMAGES TO THE SAME NETWORK TO INTERACT WITH EACH OTHER

# DOCKER-COMPOSE (we do the above but easier and safer)
# - create docker-compose.yaml
# - configure it

# Run docker-compose.yaml file

docker compose up -d 

# Shutdown the docker-compose network

docker compose down
```