# Backup Script Guide

## 1. Backup Script Code

This Bash script is designed to create a compressed backup of the `app-data` directory. It uses the current date and time in the filename so that each backup can be identified separately. The script also creates the backup directory automatically if it does not exist yet.

### Script: `backup.sh`

```bash
#!/bin/bash

# Automated Backup Script

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Starting the backup process..."

# Create the backup directory when needed
mkdir -p "$BACKUP_DIR"

# Compress the source directory
tar -czf "$BACKUP_DIR/backup_$TIMESTAMP.tar.gz" "$SOURCE_DIR"

echo "Backup process finished at $TIMESTAMP!"
```

### Explanation

- `#!/bin/bash` specifies Bash as the script interpreter.
- `SOURCE_DIR` stores the directory that contains the files to back up.
- `BACKUP_DIR` identifies where the backup archives will be stored.
- `TIMESTAMP` generates a date and time string for the backup filename.
- `mkdir -p` creates the backup directory if it is missing.
- `tar -czf` compresses the source directory into a `.tar.gz` archive.
- `echo` displays messages in the terminal.

## 2. File Permissions

Before running the script, execute the following command:

```bash
chmod +x backup.sh
```

This command grants execute permission to `backup.sh`. After changing the permission, the script can be started using:

```bash
./backup.sh
```

To check whether the backup file was created, use:

```bash
ls -lh backups/
```

The directory should contain a compressed backup file with a timestamp in its name if the script runs successfully.

## 3. Cron Job Configuration

Cron can be used to execute the backup script automatically every day at 2:00 AM. The following schedule specifies this daily execution:

```cron
0 2 * * * /root/backup.sh
```

**Important:** The path `/root/backup.sh` is only correct if the script is actually saved in `/root/backup.sh`. Use the script's real absolute path in your Cron configuration.

### Breakdown of the Five Time Fields

| Field | Value | Meaning |
|---|---|---|
| Minute | `0` | At minute zero |
| Hour | `2` | At 2:00 AM |
| Day of Month | `*` | Every day of the month |
| Month | `*` | Every month |
| Day of Week | `*` | Every day of the week |

### Configure and Verify Cron

Open the current user's Cron configuration:

```bash
env EDITOR=nano crontab -e
```

Add the schedule below, using the correct absolute path to your script:

```cron
0 2 * * * /root/backup.sh
```

Save the file and exit the editor. Then verify the scheduled task:

```bash
crontab -l
```

The command displays the Cron jobs configured for the current user.

## Conclusion

This guide demonstrates how Bash scripting and Cron can be combined to automate file backups on a Linux server. The script compresses important data into timestamped archives, while Cron provides a way to run the backup automatically at a scheduled time. These techniques help reduce repetitive manual work and support better file management.

For reliable backups, the script's output should be checked, and the generated archives should be verified to confirm that the data can be accessed when needed.

