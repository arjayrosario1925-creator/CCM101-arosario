# Firewall Configuration Guide

This document describes the firewall rules applied to an Ubuntu server using Uncomplicated Firewall (UFW). The configuration is intended to reduce unauthorized network access while keeping the required remote administration service available.

## 1. Permit SSH Connections

Run the following command:

```bash
sudo ufw allow ssh
```

**Purpose:** This command adds a firewall rule that permits incoming SSH traffic, typically through TCP port 22. It allows authorized administrators to connect to the server remotely, subject to the server's SSH authentication settings.

## 2. Set the Default Traffic Policies

Execute these commands separately:

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

**Purpose:**

- **Incoming traffic:** Connections are blocked by default unless an applicable firewall rule allows them.
- **Outgoing traffic:** Connections initiated by the server are permitted by default.

Using these policies helps reduce unnecessary exposure to external connections while maintaining normal outbound communication.

## 3. Activate UFW

Enter the following command:

```bash
sudo ufw enable
```

**Purpose:** This activates the firewall and applies the configured rules.

**Security reminder:** Allow SSH before enabling UFW when you rely on SSH for remote administration. Otherwise, you could lose remote access if no suitable SSH rule exists.

## 4. Inspect the Firewall Settings

Run:

```bash
sudo ufw status verbose
```

**Purpose:** This command displays the firewall's current state, logging configuration, default traffic policies, and active rules.

A successful configuration should report `Status: active`, with incoming traffic denied by default and outgoing traffic allowed.

## 5. Permit the Web Application Port

If the laboratory requires a web application that listens on port 8080, execute:

```bash
sudo ufw allow 8080/tcp
```

**Purpose:** This creates a rule permitting incoming TCP connections to port 8080. The application must also be running and listening on the appropriate network interface for clients to access it.

Only add this rule when port 8080 is required. Opening a firewall port does not automatically install or start the application.

## 6. Review Individual Firewall Rules

Use the following command:

```bash
sudo ufw status numbered
```

**Purpose:** This displays the configured firewall rules with assigned numbers. Numbered rules make it easier to identify individual permissions when reviewing or maintaining the firewall.

Check that each allowed port corresponds to a necessary service.

## 7. Recommended Security Practices

- Apply a default-deny policy to incoming traffic.
- Permit only the ports needed by the server's services.
- Restrict SSH access to trusted sources when practical.
- Use strong authentication and disable unnecessary remote-access methods.
- Avoid exposing database ports directly to the public internet.
- Review firewall rules after adding or removing services.
- Verify the firewall status after making configuration changes.

## Conclusion

Configuring UFW is an important step in securing an Ubuntu server. By establishing default traffic policies, permitting SSH for remote administration, and allowing application-specific ports only when necessary, administrators can better control network access.

Regularly reviewing the firewall rules helps maintain a smaller attack surface and supports the Principle of Least Privilege. These practices provide a useful foundation for managing security in cloud computing environments.
