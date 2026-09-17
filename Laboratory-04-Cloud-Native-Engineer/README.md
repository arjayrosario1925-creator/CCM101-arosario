# Laboratory 04 – The Cloud-Native Engineer

## Mission Overview

Congratulations! After successfully guiding our clients through multi-cloud evaluations, you have been promoted to the Cloud-Native Engineering Team at CloudNova Technologies. 
Modern cloud computing is no longer just about renting Virtual Machines (VMs) from AWS or Azure. Today's enterprise applications are built using lightweight, portable, and lightning-fast technologies called Containers. 
Your new mission is to understand the shift from traditional virtualization to containerization. 
Using the KillerCoda Playground, you will step into the shoes of a Cloud-Native Engineer. You will research the 
differences between VMs and containers, execute your very first Docker commands, and deploy a live, containerized web server in seconds. 

## Mission Objectives

At the end of this laboratory activity, you should be able to: 
* Differentiate between traditional Virtual Machines (VMs) and Containers. 
* Access a Docker-enabled cloud environment using KillerCoda. 
* Execute fundamental Docker CLI (Command Line Interface) commands. 
* Pull, run, manage, and terminate a containerized application (Nginx). 
* Create professional technical documentation of container operations using Markdown. 
* Continue developing a well-organized GitHub Cloud Computing Portfolio. 

## Required Resources

* KillerCoda Playground (Ubuntu or Docker environment)
* GitHub Account
* Modern Web Browser
* Stable Internet Connection

## Docker Commands Executed

* docker --version
* docker info
* docker pull nginx
* docker run -d -p 8080:80 --name nginx-server nginx
* curl http://localhost:8080
* docker ps
* docker stop nginx-server
* docker ps -a
* docker rm nginx-server

## Skills Learned

In this laboratory activity, I learned how to use basic Docker commands through the command line. I practiced downloading images, creating and running containers, checking container status, stopping containers, and removing them. I also learned that Docker can provide a faster and more resource-efficient way to deploy applications compared to traditional virtual machines.

## Challenges Encountered

One of the challenges I faced was remembering the different Docker commands and understanding their purpose. I also had to learn how port mapping works when connecting to a web server inside a container. By performing each command one at a time and checking the results in the terminal, I became more familiar with the Docker container lifecycle and was able to successfully run the Nginx web server.

