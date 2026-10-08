# Container Observability

## Application Logs

I checked the Nginx container logs using:

```bash
docker logs client-website
```

The output showed the HTTP requests made to the Nginx web server, including successful requests and one request that returned a 404 error.

### 404 Error Log

The following entry represents the request that resulted in a 404 response:

```text
172.17.0.1 - - [05/Oct/2026:10:16:48 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"
```

Application logs are useful because they record events and activities that occur while users interact with an application. They can help engineers find errors and investigate what happened before an issue occurred.

## Real-Time Container Metrics

I monitored the running container using:

```bash
docker stats
```

The `docker stats` command provides live information about the resource usage of active Docker containers.

During my observation, the `client-website` container showed:

- **CPU:** 0.00%
- **Memory Usage:** 2.723MiB / 1.895GiB

These values show how much CPU and memory the container was using from the available host resources.

## Observability Summary

Logs and metrics provide different information when monitoring an application. Logs contain details about specific events, requests, and errors, while metrics show numerical data about resource consumption and performance. Using both gives Cloud Operations Engineers a clearer picture of the overall condition of a containerized application.
