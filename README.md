# Linux Basics Part 1


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
```
```bash
cat app.log | grep -i warning | grep -i memory | wc -l
```

## 5. Linux File Permissions

Practiced interpreting and modifying Linux file permissions using `ls -l`, `chmod`, and `chown`.

Reviewed the three permission categories:

- Owner
- Group
- Others

And the three permission types:

- Read
- Write
- Execute

Also practiced numeric permissions including:

- `755` — `rwxr-xr-x`
- `644` — `rw-r--r--`
- `000` — `---------`

## 6. Permission Troubleshooting

Created a Bash script and intentionally attempted to execute it without execute permissions.

The resulting `Permission denied` error was diagnosed by inspecting the file permissions:

```bash
ls -l test.sh
```

Execute Permission was added with:

```bash
chmod +x test.sh
```



## Key Takeaways

This lab provided hands-on practice with common Linux tasks used in IT support and system administration, including:

- Navigating the Linux filesystem
- Creating, moving, copying, and deleting files and directories
- Editing and reading files
- Monitoring and analyzing logs
- Searching and filtering information with `grep`
- Using pipes to chain commands together
- Locating files with `find`
- Understanding Linux file permissions
- Using `chmod` and `chown`
- Troubleshooting permission-related errors

The lab reinforced a practical troubleshooting approach:

**Observe the problem → gather information → identify the cause → apply a targeted fix → verify the result**

## Screenshots / Evidence

### Filesystem Navigation

![Filesystem Navigation](screenshots/filesystem-navigation.png)

### File and Directory Management

![File and Directory Management](screenshots/file-management.png)

### Live Log Monitoring

![Live Log Monitoring](screenshots/log-monitoring.png)

### Log Searching and Filtering

![Log Searching and Filtering](screenshots/log-filtering.png)

### Permission Troubleshooting

![Permission Troubleshooting](screenshots/permissions-before.png)

![Permission Troubleshooting - Fixed](screenshots/permissions-after.png)

## Conclusion

This lab strengthened my foundational Linux command-line skills and provided hands-on experience with common tasks involved in IT support and system administration.

The exercises provided practical experience working with files, logs, command-line filtering, and Linux permissions while reinforcing a structured approach to troubleshooting.

