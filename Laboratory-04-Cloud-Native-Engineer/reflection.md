# Reflection

This activity helped me understand how virtual machines and Docker containers are different. A virtual machine requires a complete operating system, which means it usually needs more resources and takes longer to start. Docker containers are more lightweight because they share the host operating system, allowing applications to start much faster. Because of this, I can see why containers are useful when applications need to be deployed quickly.

I also learned more about port mapping while setting up the Nginx web server. The `-p 8080:80` option allows the host machine to communicate with port 80 inside the container through port 8080. The `curl` command was useful for testing if the web server was working correctly.

Another lesson I learned is that deleting a container with `docker rm` also removes the data stored in its writable layer. Because of this, important information should not be stored only inside a container if it needs to be preserved. Docker volumes can be used when data needs to stay available even after a container is removed.

I also realized that containers can make collaboration between developers and IT teams easier. Developers can place an application and its dependencies inside a container, and IT teams can run that same container in different environments. This can help reduce issues caused by differences in system configurations.

Lastly, I was able to improve my GitHub portfolio by documenting the Docker commands, screenshots, VM and container comparison, and reflection. This helped me organize the work I completed during the activity. Overall, the laboratory gave me a better understanding of Docker and how containerization is used in cloud computing.

