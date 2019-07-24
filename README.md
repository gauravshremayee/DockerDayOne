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




#push the image in your docker hub

$ docker tag centos:latest kumagaur/centos:witty
$ docker push kumagaur/centos:witty
The push refers to repository [docker.io/kumagaur/centos]
d69483a6face: Mounted fro


#DOCKER REMOVE IMAGES


$docker rmi image_name

docker rmi centos



