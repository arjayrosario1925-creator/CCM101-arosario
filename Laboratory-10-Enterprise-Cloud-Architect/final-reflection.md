# Final Reflection

Completing this mission helped me understand how different cloud infrastructure components work together to create a private cloud environment. I used Ubuntu Server 24.04 inside VirtualBox and configured SSH so I could manage the server through Windows Terminal. I also installed Docker and Docker Compose to deploy Nextcloud and MariaDB.

One of the main things I learned was how containers communicate with each other. I configured Nextcloud to connect to MariaDB through a Docker network and used persistent volumes to keep application and database data even when containers are restarted. I also learned how important it is to configure network access and firewall rules properly.

During the implementation, I encountered some problems with Docker image downloads and accessing the Nextcloud web interface. I had to check the network connection, container status, and VirtualBox port forwarding settings to identify the issues. Another challenge was making the backup script work correctly. At first, the script had problems with Docker commands and automatic execution because of sudo authentication. I fixed this by configuring Docker group access and updating the script so it could run without an interactive password prompt.

I also created a backup script that exports the MariaDB database and archives the Nextcloud files. The script enables maintenance mode during the backup, verifies the generated archive, and removes old backups after seven days. I configured cron to run the script every day at 2:00 AM UTC.

Overall, this activity improved my understanding of virtualization, containerization, networking, storage, security, and server automation. I realized that deploying a cloud application is not only about making it accessible through a browser. It is also important to protect the data, monitor the services, and prepare backups in case something goes wrong.

This project gave me practical experience in managing a small cloud infrastructure. The skills I learned will be useful in future cloud computing activities and other IT projects.
