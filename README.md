# Linux-Basics-Part-1


## Overview

Hands-on Linux fundamentals lab completed using an Ubuntu Server virtual machine running locally in VirtualBox.

The lab focused on navigating the Linux filesystem, managing files, working with logs, searching and filtering data, file permissions, and basic troubleshooting.

## Environment

- Ubuntu Server
- VirtualBox
- Bash shell
- Local virtual machine

## Skills Demonstrated

- Linux filesystem navigation
- File and directory management
- `cp`, `mv`, `rm`, `mkdir`, `touch`
- Editing files with Nano
- Reading and monitoring logs
- `cat`, `less`, `tail`, `tail -f`
- Searching with `grep`
- Pipes and command chaining
- `wc`, `sort`, and `uniq`
- Locating files with `find`
- Linux file permissions
- `chmod` and `chown`
- Basic Bash scripting
- Troubleshooting permission errors

## 1. Navigating the File System

Practiced navigating the Linux filesystem using commands including:

- `pwd`
- `ls`
- `ls -la`
- `cd`
- Absolute and relative paths
- Parent and home directories

Important Linux directories explored included `/home`, `/etc`, `/var`, `/tmp`, and `/usr`.

## 2. Creating and Managing Files

Created and manipulated files and directories using:

- `mkdir`
- `mkdir -p`
- `touch`
- `cp`
- `mv`
- `rm`

Created a nested application-style directory structure containing configuration and log files.

## 3. Editing and Reading Logs

Used Nano to create and edit log files and practiced reading files with:

- `cat`
- `less`
- `tail`
- `tail -f`

Used `tail -f` in a second terminal session to monitor a log file while new entries were being generated.

## 4. Searching and Filtering

Used `grep` to search log files and practiced:

- Case-insensitive searches with `grep -i`
- Inverting matches with `grep -v`
- Displaying line numbers with `grep -n`
- Recursive searches with `grep -r`
- Counting results with `wc -l`
- Locating files with `find`

### Example

Used a multi-step pipe chain to identify and count warnings related to memory usage:

```bash
cat app.log | grep -i warning | grep -i memory
