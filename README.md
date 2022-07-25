# Docker
Introduction to docker

### Definition
* **What is:** docker is an open plataform for developing, shipping and running applications

* **Why docker's so important:** docker enables you to separete your application from your infrastructure, so you can deliver software quickly

* **Also:** whith docker, you can manage you infrastructure in the same ways you can manage your applications. By taking advantage of docker's methodolgies for shipping, testing and depoly code quickly, you can significantly reduce the delay between wrinting code and running it in production


### First steps
* **How to list containers:** docker container ls
* **How to running the first image:** docker container run -ti hello-world
	* **ti =** terminal and interactive

* **First steps of docker run:** 
	* **1:** Docker Client contacted the Docker Daemon;
	* **2:** Docker Daemon pulled the image from the Docker Hub;
	* **3:** Docker Daemon created a new container from that image wich runs the executables that produces the output you are currently reading;
	* **4:** Docker Daemon streamed that output to the Docker Client, wich sent it to you terminal.

* **ctrl+b:** close and kill the container
* **Entrypoint:** the most important process in the container, if this process dies, then the container also die

* **cltr+p+q:** get out of the container but don't kill him

* **How to connect with a container:** docker container attach id
* **How to run a container with Daemon:** docker container run -d nginx
	* But for conect with it you need to use exec: docker container exec -ti id bash
* **How to stop a container:** docker container stop id
* **how to start a container:** docker container start id
* **How to restart a container** docker container restart id
* **How to see details of a container:** docker container inspect id
* **How to pause a container:** docker container pause id
* **How to unpause a container:** docker container unpause id
* **How to kill a container:** docker container rm -f id
* **How to see container resources:** docker container stats id
* **How to show the container process:** docker container top id
* **How to manage the resources of a container:** 
	* **Memory:** docker container run -d -m 128M nginx
	* **CPU:** docker container run -d -m 128M --cpus 0.5 nginx
* **How to update a container:** docker container update --cpu
	* docker container update --cpus 0.2 id

### Images
* **How to show the images:** docker image ls
* **How to create an image:** create a file called dockerfile and write script in it
* **How to build a dockerfile:** docker image build -t name:1.0

