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