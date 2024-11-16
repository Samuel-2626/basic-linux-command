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