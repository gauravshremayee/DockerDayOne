# DockerDayOne
Docker Day One 


#Docker #pull #push #customimages


$docker pull centos

#Run command and check filesystem in centos 


$ docker run -p 5003:5003 centos ls /

#tag the image

$ docker tag centos:latest centos:witty

$docker images

ubuntu                        latest              4c108a37151f        4 weeks ago         64.2MB
centos                        latest              9f38484d220f        4 months ago        202MB
centos                        witty               9f38484d220f        4 months ago        202MB
registry                      2                   f32a97de94e1        4 months ago        25.8MB
node                          7-onbuild           3de424ca76d2        23 months ago       660MB
richxsl/rhel7                 latest              9c7b3825758a        4 years ago         245MB




#DOCKER PUSH THE IMAGE IN YOUR DOCKER HUB 

$ docker tag centos:latest kumagaur/centos:witty
$ docker push kumagaur/centos:witty
The push refers to repository [docker.io/kumagaur/centos]
d69483a6face: Mounted fro


#DOCKER REMOVE IMAGES


#Purging All Unused or Dangling Images, Containers, Volumes, and Networks
#Docker provides a single command that will clean up any resources — images, containers, volumes, and networks — that are dangling (not associated with a container):

$docker system prune

#To additionally remove any stopped containers and all unused images (not just dangling images), add the -a flag to the command:

$docker system prune -a


$docker rmi image_name

docker rmi centos


#DOCKER CREATE NEW IMAGES 

$docker run -dP webdevops/php-nginx

#find the container id from docker ps and exec it 

$docker exec -it  2884e5cac184  /bin/bash

#exec vs run 


#docker pause container id to stop the container
$docker ps
$docker pause 2884e5cac184


