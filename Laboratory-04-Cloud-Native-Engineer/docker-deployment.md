## 1. Check Docker Version

* `docker --version`

This command shows the version of Docker currently installed in the environment.

## 2. Check Docker Environment

* `docker info`

This displays information about Docker and its current configuration. It also helps confirm that Docker is working properly.

## 3. Pull the Nginx Image

* `docker pull nginx`

This downloads the official Nginx image from Docker Hub. The image will be used later to create the Nginx container.

## 4. Run the Nginx Container

* `docker run -d -p 8080:80 --name nginx-server nginx`

This creates and starts the Nginx container in the background. The `-p 8080:80` option connects port 8080 of the host to port 80 inside the container.

## 5. Test the Web Server

* `curl http://localhost:8080`

This checks if the Nginx web server can be accessed through port 8080. If the setup is successful, the command will return the HTML content of the Nginx welcome page.

## 6. List Running Containers

* `docker ps`

This command shows the Docker containers that are currently running.

## 7. Stop the Container

* `docker stop nginx-server`

This stops the Nginx container that is currently running.

## 8. Verify the Container Is Stopped

* `docker ps -a`

This shows all Docker containers, including those that have already been stopped. It can be used to check if the Nginx container is no longer active.

## 9. Remove the Container

* `docker rm nginx-server`

This removes the stopped Nginx container from the Docker environment.

