# Docker

## Dockerfile
Files that contains instructions to build a Docker image.

# Docker Command Reference

## docker images  
Lists all Docker images available locally.

## docker ps  
Shows all currently running containers.

## docker ps -a  
Shows all containers (running and stopped).

## docker pull <image>  
Downloads an image from Docker Hub or another registry.

## docker stop <container>  
Stops a running container by name or ID.

## docker start <container>  
Starts a stopped container.

## docker restart <container>  
Restarts a running or stopped container.

## docker logs <container>  
Displays the logs for a specific container.

## docker container rm <container>  
Removes one or more stopped containers by name or ID.

## docker rmi <image>  
Removes one or more images from the local machine.

## docker network ls  
Lists all Docker networks.

## docker volume ls  
Lists all Docker volumes.

## docker inspect <container or image>  
Displays detailed information about a container or image in JSON format.

## docker build -t myapp .  
Builds a Docker image from the Dockerfile in the current directory and tags it as `myapp`.

## docker run --name myapp_c_nodemon -p 4000:4000 --rm -v /Users/gilles/Documents/dev/perso/docker-course/api:/app -v /app/node_modules myapp:nodemon  
- Starts a container from the `myapp:nodemon` image.
- Names the container `myapp_c_nodemon`.
- Maps port 4000 on the host to port 4000 in the container.
- `--rm` automatically removes the container when it stops.
- Mounts the host directory `/Users/gilles/Documents/dev/perso/docker-course/api` to `/app` inside the container (for code sharing).
- Mounts `/app/node_modules` as an anonymous volume to prevent the container's dependencies from overwriting those on the host.

## docker exec -it <container> <command>  
Runs a command in a running container (for example, `docker exec -it myapp_c_nodemon bash` for an interactive shell).

## docker cp <container>:<path> <host_path>  
Copies files or folders between a container and the host.
