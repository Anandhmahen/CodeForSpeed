# Docker Basic commands

## Create and run docker

```bash
sudo docker run -it -p 80:80 docker/getting-started
```

> `-it`:  interactive, tty. this will provide the interactive terminal session inside the running container.
> `-p`: binds the container's port to the machine's port. (local port:container port)
> `docker/getting-started`: name of the image to run

```bash
sudo docker run -it -p 3001:80 "/bin/bash" ubuntu:20.04
```

> `-p`: binds the container's port to the machine's port.
> `ubuntu:20.04`: name of the image to run
> `/bin/bash`: command to execute in the container
> `3001`: local port to bind
> `80`: container's port to bind

This will create a docker container with ubuntu 20.04 and bind local port 3001 to container's port 80.

## list all docker containers

```bash
sudo docker ps -a
sudo docker container ls -a
```

> Both commands lets you can see the list of containers (in all state)

## stop a running container

```bash
sudo docker stop <container_id>
sudo docker stop 20df1d11a596
```

> `20df1d11a596`: container id

## Start a Stopped Docker Container

```bash
sudo docker start <container_id>
sudo docker start 20df1d11a596
```

> `20df1d11a596`: container id

## Remove (Delete) a stopped container

```bash
sudo docker container rm <container_id>
sudo docker container rm 20df1d11a596
```

> `20df1d11a596`: container id

## Execute a Command in a Container

```bash
sudo docker exec -it <container_id> <command>
sudo docker exec -it youthful_feist apt install tree
```

> `youthful_feist`: container name
> `apt install tree`: command to execute in the container

This will open the bash shell in the container in interactive mode.

```bash
sudo docker exec -it youthful_feist /bin/bash
```

## Run Docker from Local Build

```bash
docker run  -it --rm <image_name>
```

> `-it`: interactive, tty. this will provide the interactive terminal session inside the running container.
> `--rm`: removes the container after it exits.
> `<image_name>`: name of the image to run

This will run the docker container from the local build image.

## Remove all Stopped Containers, Dangling Images, and Unused Networks

```bash
docker system prune
```

> This will remove all stopped containers, dangling images, and unused networks.
