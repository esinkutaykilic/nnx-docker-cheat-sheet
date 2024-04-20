# 🐳 Docker cheat sheet

## Docker basics 
{collapsible="true" default-state="collapsed"}

#### Check docker version
```Shell
docker --version
```
-or-
```Shell
docker -v
```

#### Display sistem-wide information about Docker
```Shell
docker info
```

#### Download an image from Docker Hub
```Shell
docker pull <image_name>
```

#### List local Docker images
```Shell
docker images
```
-or-
```Shell
docker image ls
```

#### List running containers
```Shell
docker ps
```
-or-
```Shell
docker container ls
```

#### List all containers (including stopped ones)
```Shell
docker ps -a
```
-or-
```Shell
docker container ls -a
```

#### Create and start a new container form an image
```Shell
docker run <options> <image_name>
```

## Container lifecycle 
{collapsible="true" default-state="collapsed"}

#### Start a stopped container
```Shell
docker start <container_name/id>
```

#### Stop a running container gracefully
```Shell
docker stop <container_name/id>
```

#### Forcefully stop a running container
```Shell
docker kill <container_name/id>
```

#### Restart a container
```Shell
docker restart <container_name/id>
```

#### Remove a stopped container
```Shell
docker rm <container_name/id>
```


## Images
{collapsible="true" default-state="collapsed"}

#### Build a Docker image from a Dockerfile
```Shell
docker build -t <image_name> <path_to_Dockerfile>
```

#### Remove an image
```Shell
docker rmi <image_name>
```

#### Remove all unused images
```Shell
docker image prune
```

## Docker Compose
{collapsible="true" default-state="collapsed"}

#### Start services defined in a Docker Compose file 
```Shell
docker-compose up
```

#### List services in a Docker Compose file and their status
```Shell
docker-compose ps
```

#### View logs for a specific service 
```Shell
docker-compose logs <service_name>
```

#### Run a command in a running service container
```Shell
docker-compose exec <service_name> <command>
```

## Volumes
{collapsible="true" default-state="collapsed"}

#### Create a named volume
```Shell
docker volume create <volume_name> 
```

#### Mount a volume to a container
```Shell
docker run -v <volume_name>:<container_path> 
```

#### List volumes
```Shell
docker volume ls 
```

#### Remove a volume
```Shell
docker volume rm <volume_name>
```

## Docker registry and Hub
{collapsible="true" default-state="collapsed"}

#### Log in to a Docker registry
```Shell
docker login 
```

#### Push an image to a registry
```Shell
docker push <image_name> 
```

#### Pull an image from a registry
```Shell
docker pull <image_name> 
```

## Networks
{collapsible="true" default-state="collapsed"}

#### Create a user-defined network
```Shell
docker network create <network_name> 
```

#### Connect a container to a network
```Shell
docker network connect <network_name> <container_name/id> 
```

#### Disconnect a container from a network
```Shell
docker network disconnect <network_name> <container_name/id> 
```

## Logs and debugging
{collapsible="true" default-state="collapsed"}

#### View container logs
```Shell
docker logs <container_name/id> 
```

#### Start an interactive Shell in a running container
```Shell
docker exec -it <container_name/id> /bin/bash 
```

#### Display real-time container resource usage
```Shell
docker stats <container_name/id> 
```

## Cleanup
{collapsible="true" default-state="collapsed"}

#### Remove all stopped containers, unused networks, and images
```Shell
docker system prune 
```

#### Remove all stopped containers
```Shell
docker container prune 
```

#### Remove all unused images {id="cleanup__remove-all-unused-images"}
```Shell
docker image prune 
```

#### Remove all unused volumes
```Shell
docker volume prune 
```

---

## -
Thanks to [the post of @Zeeshan Skaheel](https://www.linkedin.com/feed/update/urn:li:activity:7187133018866696193?utm_source=share&utm_medium=member_desktop)