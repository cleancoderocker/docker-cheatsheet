# docker-cheatsheet
Useful Docker commands and snippets

## Containers

### Stop and remove all containers

```
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```

### Bash into a container
```
docker exec -it <CONTAINER_ID_OR_NAME> bash
```

## Volumes

### List all volumes (including host paths) for a container

```
docker inspect -f '{{ .Mounts }}' <CONTAINER_ID_OR_NAME>
```
