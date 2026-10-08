# System Baseline Report

## Host System Baseline

Before running the client website, I checked the Linux server's basic resources to determine its current condition and available capacity.

### Memory

The Linux server has approximately **1.9Gi** of total RAM.

I used the following command:

```bash
free -h
```

### Disk Storage

The root (`/`) file system has a total capacity of **19G**.

I checked this using:

```bash
df -h /
```

### CPU and Processes

To monitor the active processes and CPU activity, I used:

```bash
top
```

This command displays running processes and allows me to observe CPU usage and other system activity in real time.

### Why Disk Space Is Important

Monitoring available disk space is important before a large increase in traffic because applications may need additional storage for logs, temporary files, cache data, and other system activities. When the disk becomes full, applications and system services may experience errors or stop functioning correctly.
