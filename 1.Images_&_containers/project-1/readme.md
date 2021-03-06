```
docker build -t project1 .
docker run -it -p 3000:80 -d project1

#  i for input and t for pseudo termianl(tty)

docker ps -a
docker ps

docker start container-name-or-id (attach -> -a flag , -i for input flag)
docker attach container-name-or-id
docker stop container-name-or-id

docker logs -f container-name-or-id (following- future outputs..)


## Deleting containers and images
### Note -> Need to delete the container first before deleting that particular image

docker rm container-a container-b
docker rmi image-id-or-name  image-2

docker image prune -a
docker container prune

docker run --rm image-id  >> removes contaienr automatically once it stops..

## Naming and tagging images and containers

containers - docker run --name server image-id
image - docker build -t server:1.0 .   (name:tag mode)
        docker tag local-image:tag new-name:tag


## Inspecting images and containers
docker image inspect image-id
dokcer inspect container-id

## Copying files from and to running containers

    ### to container
    docker cp source container-name:/~destincation
        docker cp dummy/. project1:~/app/test

    ### from container
    docker cp container-name:~/source destincation

## Sharing images and containers
-- sharing dockerfile and surrounding codes
-- built images..

    docker push user-name/image-name:tag
    docker pull user-name/image-name:tag

by default, without host, it will go for docker-hub, but for private registry, we need to mention host:image-name while pulling and pushing.


docker login
docker logout

```

- Images are read-only and are not meant to run any code. Containers does that job with the help of image.

- With image u can spin up multiple containers and uses cacheble layer to build images unless u chnage docker file.

- docker run command runs in attach mode and docker start cmd runs in detach mode
