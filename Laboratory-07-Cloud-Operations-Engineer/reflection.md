# Reflection

This activity helped me understand why it is important to monitor the host server even when the Docker containers appear to be working properly. A container may be running without errors while the host system is experiencing high CPU usage, low memory, or insufficient disk space. Checking these resources helps a Cloud Operations Engineer determine whether the server has enough capacity for additional workloads.

I also learned that the `docker logs` command is useful when investigating application problems. For example, if a user reports that a website is not working properly, I can check the container logs for errors, failed requests, or other useful information. Instead of immediately guessing the cause, the logs provide evidence that can help identify the problem.

Another thing I learned is that logs and metrics serve different purposes in monitoring. Logs provide details about individual events, such as HTTP requests and error responses. Metrics, on the other hand, provide numerical information such as CPU and memory usage. Combining these two sources can give a more complete view of an application's condition.

For organizations running a large number of containers, checking each container manually would take too much time. Monitoring platforms such as Prometheus and Grafana can be used to collect and display information from multiple systems. This allows engineers to monitor larger environments and identify possible issues more efficiently.

My Linux troubleshooting skills have also improved since I started the first mission. I am now more familiar with checking system resources, managing Docker containers, sending test requests, and viewing application logs. I learned that troubleshooting involves more than simply looking for an error. It also requires gathering information, examining the results, and using the available data to understand the problem. Overall, this activity made me more comfortable working with Linux and Docker.
