# Reflection

This activity helped me understand how Docker Compose can make it easier to manage applications that use multiple containers. Instead of creating and configuring each container one by one, I can place all the required settings inside a `docker-compose.yml` file and start the application with a single command. This makes the deployment process more organized and saves time when the same setup needs to be used again.

I also learned that YAML formatting needs to be handled carefully, especially when it comes to indentation. Using incorrect spacing or a Tab can cause Docker Compose to return an error. At first, I did not think indentation would be a major issue, but I realized that even a small formatting mistake can prevent the configuration file from working properly.

Another thing I learned was how environment variables help configure the containers. Settings such as `MYSQL_PASSWORD`, `MYSQL_DATABASE`, and `MYSQL_USER` give Nextcloud the information it needs to connect to MariaDB. Having these values in the Compose file makes the setup more organized because the required configuration is provided when the containers are created.

I also found it interesting that I was able to run a private cloud storage application like Nextcloud with only a few configuration steps. Before doing this activity, I expected setting up a cloud storage system to require more complicated procedures. Docker Compose showed me that a well-prepared configuration file can simplify the deployment of multiple services.

Since starting Mission 1, I can see that my understanding of cloud computing has improved. I started with basic Linux commands and cloud infrastructure concepts, and I have now practiced using Docker, containers, object storage, and multi-container applications. I also have a better understanding of how these technologies can work together. These activities have also made me more comfortable using the Linux terminal and organizing my laboratory work through GitHub.
