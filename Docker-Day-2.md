```
What is Docker?
Why Docker?
How to install Docker?
How to work with Container?
--------------------------------------



Docker architecture
=========================

Human -> Docker client --> Docker Server -> ContainerD --> kernal
	 =====================================
				Docker enginer
								




Docker workflow

Human -> Docker client --> Docker Server -> ContainerD --> kernal
						Check the image
						- local
						download from hub




Docker components
=======================================
1. docker engine

2. Docker image
- version OR layer of file systems
			
			registery(you have repository)
			hub.docker.com
						repo == image name
							image file system

vm image = boot fs + rootfs + app fs + userfs
docker image  = rootfs + app fs + userfs

3. Docker registry
			hub.docker.com
			google registory

4. Docker container
			
				1 USRE + 1 MNT(From image) + 1 NEt + 1PID
				---
				USER get attached to all == container


Container Lifecycle

create + start + stop + restart + pause + unp + kill + rm


PID1
-------------------------------------
PS 					VM 			container
is running of PID1		==> 			=> 

PID1 = systemd			systemd		== ANything	


How to use Container?
==========================

Go inside
		SHELL

Access from outside

		IP / http


RUN
==============================================
pull + create + start + attached to a container(PID1)

RUN -d
==============================================
pull + create + start + DO NOT attached to a container(PID1)


===============================================
  148  docker ps
  149  docker exec eef958b5b633 ls
  150  ls
  151  docker exec eef958b5b633 du
  152  clear
  153  docker exec eef958b5b633 /bin/bash
  154  docker exec -it eef958b5b633 /bin/bash
  155  clear
  156  docker ps
  157  docker exec -it a7b117a5a81a /bin/bash
  158  clear
  159  ls
  160  clear
  161  docker ps
  162  docker inspect eef958b5b633
  163  ping 172.17.0.3
  164  docker ps
  165  clear
  166  curl http://"172.17.0.3"
  167  docker ps
  168  docker attach a7b117a5a81a
  169  docker ps
  170  docker attach eef958b5b633
  171  docker ps
  172  docker ps 0a
  173  docker ps -a
  174  clear
  175  docker run -itd ubuntu
  176  docker run -d https
  177  docker run -d httpd
  178  docker ps
  179  docker run -d -p 81:80 httpd
  180  docker run -d -p 82:80 httpd
  181  hostname
  182  clear
  183  docker network ls
  184  clear
  185  ls
  186  docker network ls
  187  docker run -d --net=host --name deepak httpd
  188  docker ps
  189  clear
  190  ls
  191  docker ps
  192  docker cp puppet7-release-focal.deb b1b364bcbe75:/tmp
  193  docker exec b1b364bcbe75 ls /tmp
  194  docker diff b1b364bcbe75
  195  docker port 039bb1464c71
  196  docker port fc6d2dbed09d
  197  docker rename fc6d2dbed09d rajubangayagen
  198  docker port fc6d2dbed09d
  199  docker ps
  200  clear
  201  docker ps
  202  docker logs d9ba325f46ed
  203  clear
  204  docker stats
  205  ps -eaf | grep containerd
  206  clear
  207  ls
  208  docker ps
  209  docker top 7bdc3fc31dd8
  210  ps -eaf | greo 1173322
  211  ps -eaf | grep 1173322
  212  clear
  213  docker events
  214  history





```
