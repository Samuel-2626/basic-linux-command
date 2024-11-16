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