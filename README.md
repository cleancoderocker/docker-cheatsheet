# 🐳 Docker Cheat Sheet
Useful Docker commands and snippets

## Table of Contents

* [Containers](#containers)
* [Images](#images)
* [Volumes](#volumes)

## 🐳 Containers

### Stop and remove all containers

```
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```

### Print out the logs of a container
```
docker logs <CONTAINER_ID_OR_NAME>
docker logs -f --tail 10 <CONTAINER_ID_OR_NAME>
```

### Bash into a container
```
docker exec -it <CONTAINER_ID_OR_NAME> bash
```

## 🐳 Images
### List images starting with a prefix

```
docker images --filter 'reference=<PREFIX>*'
docker images --filter 'reference=<PREFIX>/*'
```

## 🐳 Volumes

### List all volumes (including host paths) for a container

```
docker inspect -f '{{ .Mounts }}' <CONTAINER_ID_OR_NAME>
```
