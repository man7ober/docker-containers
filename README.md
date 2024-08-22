## Docker Containers

Docker Image = consist of environment, source code and dependencies

Docker Container = consist of docker image + run command

**01 - Run / Start / Stop Container**

```bash
docker run <IMAGE-NAME>
docker start <CONTAINER-ID>
docker stop <CONTAINER-ID>
```

- --name = name the container
- -v = mount the volume into container e.g: /local path : /container path
- --rm = remove the container after completion
- -e = passing the environment variables into container
- -it = interactive shell to access container with /bin/bash
- -p = mapping container port with host port e.g host-port : cont-port
- --network = add the same network to connect multiple containers
- -d = run container in background

**02 - List Containers**

```bash
docker ps
```

- --all = list all containers running / stopped

**03 - Remove Container**

```bash
docker rm <CONTAINER-ID>
```

**04 - List Images**

```bash
docker images
```

**05 - Remove Image**

```bash
docker image rm <IMAGE-ID>
```

**06 - Build Image from Dockerfile**

```bash
docker build -t <MY-IMAGE:TAG> .
```

**07 - Remove all unused containers, networks, images and volumes**

```bash
docker system prune
```

- -a = remove all unused images not just dangling ones

**08 - Network to connect containers**

```bash
docker network create <NETWORK-NAME>
docker network ls
docker network inspect <NETWORK-NAME>
```

**09 - Pulling an image**

```bash
docker pull <IMAGE-NAME>
```

**10 - Pushing images to docker hub**

```bash
docker tag <IMAGE-ID> <USERNAME/IMAGE-NAME>
docker push <USERNAME/IMAGE-NAME>
```

**11 - Volumes of persisting data**

```bash
docker volume create <VOLUME-NAME>
docker volume ls
docker volume rm <VOLUME-NAME>
docker volume inspect <VOLUME-NAME>
```

**12 - Running multiple containers**

```bash
docker compose up
docker compose down
docker compose logs
```
