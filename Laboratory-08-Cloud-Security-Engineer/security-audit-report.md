# Security Audit Report

## 1. Principle of Least Privilege (PoLP)

The Principle of Least Privilege is a security practice that gives users and applications only the permissions they need to perform their tasks. This helps protect a cloud server from unauthorized access and prevents users from making unnecessary changes. By limiting permissions, the risk of security problems and accidental system damage can be reduced.

## 2. Attack Surface

An attack surface includes all the possible ways an unauthorized person could try to access a server. Examples include open ports, active services, installed applications, and remote access connections. A server with too many exposed services may have a higher security risk. Therefore, unnecessary services should be disabled, and network access should be limited to what is needed.

## 3. Default Deny Policy

The Default Deny policy is a firewall security approach in which incoming connections are blocked unless they are specifically permitted by a rule. This helps protect the server from unwanted network traffic, including connections from unknown sources. Instead of allowing all connections and blocking suspicious ones individually, this policy allows only the services required for normal server operations.

## 4. Server Security Audit

The main objective of this security audit is to examine the server's active network ports and apply firewall rules to control incoming connections.

The server was configured to run an Nginx web application inside a Docker container using port 8080. Before applying the firewall rules, the application was tested using the `curl` command to check whether it could respond to a request.

### Commands Used for Inspection

```bash
sudo ss -tulnp
sudo ufw status verbose
```

The commands above were used for the following purposes:

- **`sudo ss -tulnp`** – Displays listening TCP and UDP ports, along with process information when available. This helps identify services that may be accepting network connections.
- **`sudo ufw status verbose`** – Shows whether UFW is enabled, its default firewall policies, and the rules currently configured on the server.

### Security Findings

Based on the server's intended configuration, SSH access through port 22 is needed for remote administration, while TCP port 8080 is required to access the Nginx web application.

To improve security, incoming connections should be restricted to these required services. Other incoming traffic should remain blocked unless an additional service is necessary. The firewall should follow a Default Deny policy to prevent unnecessary connections from reaching the server.

The actual listening ports and firewall rules must be confirmed using the inspection commands. This ensures that the security report accurately reflects the server's current configuration.

### Conclusion

Performing this security audit helped me understand how important it is to check a server's network services and control incoming connections. I learned that open ports can create security risks when they are not properly managed. Using UFW with restrictive firewall rules helps reduce the attack surface and prevent unauthorized access to unnecessary services.

Overall, applying the Principle of Least Privilege and the Default Deny policy can improve the security of a cloud server. However, firewall rules must be tested carefully to ensure that necessary services, especially SSH and the web application, remain accessible to authorized users. Documenting the commands and their actual results through terminal screenshots also provides evidence that the security checks were performed.

