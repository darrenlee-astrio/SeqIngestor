# SeqIngestor

```bash
docker compose up --build // build and create running container instances
docker compose down // stops and deletes the containers
```

# Docker Concepts

## Image

- **Definition:** A packaged application and its dependencies (libraries, binaries, etc.) that runs in isolation on a host system.
- **Usage:** Downloaded from a registry (like Docker Hub) to create and run containers.

## Container

- **Definition:** An instance of an image that runs as a process, isolated from other processes on the host system.
- **Usage:** Created from an image, and can be started, stopped, moved, and deleted.

## Dockerfile

- **Definition:** A text file that contains a list of instructions to build a Docker image.
- **Usage:** Used with the `docker build` command to automate the process of creating Docker images from source code.

## Docker Compose

- **Definition:** A tool for defining and running multi-container Docker applications.
- **Usage:** Allows you to manage multiple containers that work together, defined in a YAML file (`docker-compose.yml`), simplifying complex setups.

## Volumes

- **Definition:** A way to persist data generated and used by Docker containers.
- **Usage:** Ensures that data persists even after containers are stopped or removed, useful for databases, file uploads, and other persistent storage needs.

## Common Commands

```bash
docker ps // shows a list of running containers
docker ps -a // shows all containers (running and stopped)
docker images // shows all images

docker run <image-name>:<image-tag> // pulls the image if doesnt exist locally and run
docker run -p <port-exposed>:<port-internal> -p <port-exposed>:<port-internal> // port mapping
docker run -d <image-name> // run as detached
docker run -e "HELLO=WORLD" // pass in environment variable
docker attach <container-id> // attach back after detached
docker logs <container-id> // show logs

docker stop <container-id> // stops the container
docker rm <container-id> // remove container

docker exec -it <container-id> bash // interactive-terminal to run commands

docker build -f .\folder-name\Dockerfile -t <image-name> . // create an image from Dockerfile
docker run -p 1234:80 <image-name> // run the image

```
