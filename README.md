# Basic Linux Commands 101

## Navigating File System

- `pwd`: Print working directory (shows the current directory you are in).
- `ls`: List directory contents, common options:
    * `ls -1`: long listing format
    * `ls -a`: show hidden files (files beginning with `.`)
    * `ls -h`: Human-readable sizes
- `cd <directory>`: Change directory
- `cd ..`: Go up one directory
- `cd ~`: Go to home directory
- `find <path> -name <file>`: Search for a file by name

## File Operations

- `cat <file>`: Display file contents
- `more <file> / less <file>`: View file contents page by page
- `touch <file>`: Create an empty file or update the timestamp of a file
- `cp <source> <destination>`: Copy files or directories
- `mv <source> <destination>`: Move or rename files
- `rm <file>`: Remove a file. Use `-r` for directories
- `rmdir <directory>`: Remove an empty directory

## File Permissions and Ownerships

- `chmod <permissions> <file>`: Change file permissions
    * Example: `chmod 755 <file>`: Sets read, write, and execute permissions for owner, and
    read and execute for others.
- `chown <user>:<group> <file>`: Change file ownership
    * Example: `chown user:group <file>`: Change file ownership and group
- `chgrp <group> <file>`: Change the group ownership of a file

## File System Management

- `df`: Display disk space usage of file systems
- `du`: Display file space usage within directories
    * Example: `du -sh <directory>`: Show human-readable size of the directory

## System Management Commands

These are useful for managing system resources, processes, and services

### Process Management

- `ps`: Display running process
    * Example `ps aux`: (display all processes)
- `top`: Display real-time process information, including CPU and memory usage.
- `htop`: An improved version of `top` (requires installation)
- `kill <PID>`: Terminate a process by its PID (Process ID)
- `killall <process_name>`: Kill all processes by name
- `bg`: Rename a suspended process in the background
- `fg`: Bring a background process to the foreground

### System Resource Management

- `free`: Display memory usage
- `uptime`: Show how long the system has been running, load averages, and users.
- `vmstat`: Display system memory, processes, and CPU information

### Service Management (System-based systems like Ubuntu, CentOS 7+)

- `systemct1 status <service>`: check the status of a system service
- `systemct1 start <service>`: start a service
- `systemct1 stop <service>`: stop a service
- `systemct1 restart <service>`: restart a service
- `systemct1 enable <service>`: enable a service to start on boot
- `systemct1 disable <service>`: disable a service from starting on boot

### Managing Users and Groups

- `useradd <username>`: Add a new user
- `usermod <username>`: Modify an existing user (e.g. change groups, shell).
- `userdel <username>`: Delete a user
- `groupadd <groupname>`: Add a new group
- `groupdel <groupname>`: Delete a group
- `passwd <username>`: Set or change a user's password

## Networking Commands

Linux offers powerful networking commands for managing and troubleshooting network connections.

### Network Configuration

- `ip addr`: Display IP addresses of all network interfaces
- `ip link`: Display or manage network interfaces.
- `ping <host>`: Check connectivity to another machine (ping a host).
- `ss`: A modern replacement for `netstat`, used to display socket statistics.
- `traceroute <host>`: Trace the route packets take to a network host


### Firewall Configuration:

- `ufw` (Uncomplicated Firewall): An easy-to-use frontend for `iptables`.
    * Example: `ufw allow 80/tcp` (allow HTTP traffic).

### SSH

- `ssh <user>@<host>`: Securely connect to a remote machine.
- `scp <source> <destination>`: Securely copy files between systems
- `sftp <user>@<host>`: Secure file transfer using FTP over SSH

## Advanced System Administration Tools

- Cron Jobs:

Cron jobs are scheduled tasks that run at set intervals or times. They are often used to automate repetitive tasks, such as: Backing up databases, Generating reports, Monitoring disk space, Checking for broken links, and Clearing a site's cache.

Cron jobs are useful for computers that run 24/7, like virtual private servers. They are also a useful concept in back-end development.

- Here are some things to know about cron jobs:

* How they work

A cron job is an entry in a table called the crontab, which contains a schedule and a command to be executed. The cron daemon (crond) looks for entries in the crontab to determine what jobs to run and when.
