## Docker Containers

**Docker :**

<code>docker init</code>
- pre-generated docker files

<code>docker compose watch</code>
- watch the service/container of an app

**Images :**

<code>docker images</code>
- list all images

<code>docker build -t [image_name] .</code>
- create an image from dockerfile

<code>docker pull [image_name:tag]</code>
- pull an image from docker hub

<code>docker rm [image_id]</code>
- remove a local image

<code>docker tag [source_image:tag] [new_image:tag]</code>
- tag an image

<code>docker push [image_name:tag]</code>
- push an image to docker hub

<code>docker image prune</code>
- prune unused images

**Containers:**

<code>docker ps</code> 
- list all containers

<code>docker run [image_name]</code> 
- run the container

<code>docker stop [container_id]</code> 
- stop the container

<code>docker start [container_id]</code> 
- start the stopped container

<code>docker rm [container_id] -f</code> 
- remove the container

<code>docker container prune</code> 
- delete all stopped containers

<code>docker logs [container_id]</code> 
- view container logs

<code>docker inspect [container_id]</code> 
- inspect details of a container

**Flags :**

- n - named container

- f - forcefully remove

- a - list all containers

- it - run the container in interactive mode

- p - for exposing port

- v - volumes for store/mount data


**Volumes :**

<code>docker volume ls</code> 
- list all volumes


<code>docker create volume [volume_name]</code> 
- create a named volume


<code>docker volume rm [volume_name]</code> 
- remove a volume


<code>docker volume inspect [volume_name]</code> 
- inspect details of a volume

**Networks :**

<code>docker network ls</code> 
- list all networks

<code>docker network inspect [network_name]</code> 
- inspect details of a network

<code>docker create network [network_name]</code> 
- create a user-defined bridge network

<code>docker connect network [network_name] [container_name]</code> 
- connect a container to a network

<code>docker disconnect network [network_name] [container_name]</code> 
- disconnect a container from a network


**Docker Compose :**

<code>docker compose ps</code> 
- list containers for specific docker compose project

<code>docker compose up</code> 
- create and start containers

<code>docker compose down </code>
- stop and remove containers

<code>docker compose build</code> 
- build or rebuild services

<code>docker compose watch</code> 
- watch services

<code>docker compose logs</code> 
- view logs for services


**Security :**

<code>docker scout</code>
- find vulnerabilities in services
