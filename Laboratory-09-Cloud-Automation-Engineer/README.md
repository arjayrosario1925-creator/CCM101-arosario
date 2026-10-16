# Laboratory 09: The Cloud Automation Engineer

## Mission Overview

In this laboratory activity, I learned how to automate simple tasks on a Linux server using Bash scripting and Cron. I created a directory containing sample data, developed a backup script, and used it to generate compressed backup files. I also explored how to schedule tasks so they can run automatically at a specified time.

## Objectives

- Learn the fundamentals of Bash scripting.
- Create and edit shell scripts using the nano text editor.
- Understand how to change file permissions with `chmod`.
- Generate compressed backups using a Bash script.
- Use Cron to schedule recurring tasks.
- Check scheduled jobs and document the completed activity.

## Commands Executed

The following commands were used during the laboratory activity:

```bash
mkdir app-data
echo "This is critical client data." > app-data/data.txt
cat app-data/data.txt
nano backup.sh
chmod +x backup.sh
./backup.sh
ls -l backups/
crontab -l
env EDITOR=nano crontab -e
```

These commands helped me prepare the sample files, create and execute the backup script, inspect the generated backup files, and configure the Cron schedule.

## Skills Learned

- **Bash Scripting:** Writing simple scripts to automate repetitive tasks.
- **File and Directory Management:** Creating directories and managing sample data.
- **File Permissions:** Using `chmod` to make a script executable.
- **Backup Management:** Creating compressed `.tar.gz` archives for storing copies of files.
- **Task Scheduling:** Configuring Cron to run scripts automatically.
- **System Verification:** Checking backup files and reviewing scheduled Cron jobs.
- **Technical Documentation:** Recording commands, procedures, and results using Markdown.

## Conclusion

This laboratory activity helped me understand how automation can make cloud server management easier and more efficient. By creating a Bash backup script, I learned how to reduce the need to perform repetitive tasks manually. I also discovered that Cron can be used to schedule backups regularly without having to execute the script every time.

Overall, this mission introduced me to basic Linux automation techniques that can help maintain files and protect important data. These skills are useful when managing servers because regular backups and properly scheduled tasks can improve the reliability of a system.

