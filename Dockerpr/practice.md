## What is Docker ?

* Docker (dock worker) is used to create containers which is standard way of packaging any application
* Docker is an open-source project that automates the deployment of
applications inside software containers



#### create instance
* To install docker
* docker script:- 
curl -fsSL https://get.docker.com -o install-docker.sh
sudo sh install-docker.sh
exit
relogin

#### check docker config
#### docker --version
clint will be conneting to server
* then start working
#### installing tomcat

#### commands
```
sudo apt update
sudo apt install net-tools openjdk-11-jdk tomcat9 -y
# to check network
ifconfig
# to check java
java -version
# to check tomcat
sudo systemctl status tomcat9
```
![Peview](./Images/docker1.png)

## Springpetclinc application
* This is spring pet clinic application
* Lets try to run this application on linux
* 
# commands 
```
sudo apt update
sudo apt install openjdk-17-jdk maven -y
git clone https://github.com/spring-projects/spring-petclinic.git
cd spring-petclinic
# java package
mvn package
java -jar target/spring-petclinic-3.0.0-SNAPSHOT.jar
```
![Priview](./Images/docker2.png)
![Priview](./Imagaes/Docker3.png)
![Preview](./Images/docker4.png)


* vi docker
by writing docker file we can run number of container

### Containerization
* For containerization I did 3 things to run the application
1. what we required to run application
2. What are the steps to start the application
2. What are the ports  our application can be access 

* Inside the container we never run a sever side application not for clinet side application

* Docker containers are meant for server side applications not for client side applications 
* -it means Interactive with Terminal

### Commands:-
* docker container ls -a 
=> shows all the containers
* docker container ls -a -q
=> shows all the containers Id
* rm stands for remove
* -f stands for forcefully
* To remove the all the containers at a time. We have to use this command.
* docker container rm -f $(docker container ls -a -q) 


 docker container run --name myhttpd1
 docker container run --name -d myhttpd1
 docker container run --name myhttpd2 -p 32000:80 -d httpd

* docker images doesn't having running or stopig state
* Lets remove all the images docker image rm -f $(docker image ls -q)

* docker image 
=> Lets create a container and login into that during running the container. Lets use alpine and ubuntu docker image

* Docker container can be executed in 3 ways
  1.detached
  2.attached
  3.interactive

 * Lets create the nginx container in detached mode -d 
 * in attached mode we can see standard input,output,error.
 * IN detached mode the container will be started in the backgroung
  $docker container run -d --name nginxd nginx
![Preview](./Images/docker5.png)

* Lets create the nginx container in attached mode.
* it runs in the background 
* In attaches the container will exited when we entier ctrl+c
  * $ docker container run --name nginxa nginx
![Preview](./Images/docker6.png)

 * Let create some images in interactive mode -it
 * interactive mode where we inside the container and try to execute something
   * $ docker container run -it --name alpint alpine /bin/sh
   * $ docker container run -it name ubnint ununtu /bin/bash
![Preview](./Images/docker7.png)

* Use exec of the docker container command 
![preview](./Images/docker8.png)



