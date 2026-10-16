# Laboratory 08: Cloud Security and Firewall Configuration

**Course:** CCM101 – Cloud Computing  
**Laboratory:** 08 – Cloud Security Engineer  
**Environment:** KillerCoda Ubuntu Playground  
**Date:** October 17, 2026

## Introduction

This laboratory activity focuses on improving the security of a Linux server by configuring its firewall. A server connected to a network may receive unwanted connection attempts if its ports are not properly managed. To reduce this risk, I used the Uncomplicated Firewall (UFW) to control incoming and outgoing network traffic.

The activity helped me understand how firewall rules protect a server and why only necessary network services should be accessible.

## Learning Objectives

After completing this activity, I was able to:

1. Explain the importance of network security in cloud computing.
2. Configure UFW to manage network traffic on Ubuntu.
3. Set the default policy to deny incoming connections and allow outgoing connections.
4. Create a firewall rule that permits SSH access.
5. Activate the firewall and verify its current configuration.
6. Document Linux security commands and their results in a GitHub repository.

## Laboratory Procedures

### Checkpoint 1 – Prepare the Environment

I accessed the Ubuntu environment through the KillerCoda Playground and prepared the terminal for the security configuration activity.

### Checkpoint 2 – Configure the Firewall Rules

Before enabling the firewall, I allowed SSH connections so that remote administration could remain accessible.

```bash
sudo ufw allow ssh
```

Next, I configured the default policies to block incoming connections and permit outgoing connections.

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

These settings help limit unauthorized access while allowing the server to initiate necessary network communications.

### Checkpoint 3 – Enable UFW

After setting the firewall rules, I activated UFW.

```bash
sudo ufw enable
```

Enabling the firewall applies the configured policies and allows UFW to manage network traffic.

### Checkpoint 4 – Verify the Firewall Configuration

To confirm that the firewall was active and the rules were applied, I executed:

```bash
sudo ufw status verbose
```

The expected results include an active firewall status, a default incoming policy of `deny`, a default outgoing policy of `allow`, and an SSH rule allowing traffic on port 22.

## Commands Summary

| Command | Purpose |
|---|---|
| `sudo ufw allow ssh` | Allows SSH connections |
| `sudo ufw default deny incoming` | Blocks incoming traffic by default |
| `sudo ufw default allow outgoing` | Permits outgoing traffic by default |
| `sudo ufw enable` | Activates the firewall |
| `sudo ufw status verbose` | Displays detailed firewall settings |

## Security Concepts Learned

**Firewall:** A security mechanism that filters network traffic according to configured rules.

**Default Deny:** A security policy that blocks incoming connections unless a rule explicitly permits them.

**Principle of Least Privilege:** A practice of granting only the network access necessary for a service or user to perform its intended function.

**SSH Security:** SSH provides encrypted remote administration. Allowing SSH through the firewall makes remote access possible, so authentication and account security remain important.

## Conclusion and Reflection

Through this laboratory activity, I learned how to configure a basic firewall on an Ubuntu server using UFW. I applied a default-deny policy for incoming connections, allowed outgoing traffic, and created a rule for SSH access. I also verified the firewall status to check whether the configuration was successful.

This activity showed me that cloud security begins with properly managing access to a server. Leaving unnecessary ports open can increase security risks, while carefully selected firewall rules help reduce the server's attack surface. In future deployments, I will check the required services before enabling a firewall and document the security settings for easier maintenance and troubleshooting.

## Evidence and Screenshots

Insert your actual terminal screenshots below each section when uploading this README to GitHub.

- **Screenshot 1:** UFW SSH rule configuration.
- **Screenshot 2:** Default incoming and outgoing policies.
- **Screenshot 3:** Firewall activation.
- **Screenshot 4:** Final UFW status showing the applied rules.

## References

- [Ubuntu Server Documentation – Firewall](https://documentation.ubuntu.com/server/how-to/security/firewalls/)
- [UFW Manual](https://manpages.ubuntu.com/manpages/jammy/en/man8/ufw.8.html)
