# Basic Linux Commands

## File and Directory Management

| Command | Description | Example |
| ------- | ----------- | ------- |
| `ls`    | Lists directory contents | `ls -l` (detailed list) |
| `cd`    | Changes the current directory | `cd /var/log` |
| `pwd`   | Prints the current working directory | `pwd` |
| `cp`    | Copies files or directories | `cp file1.txt file2.txt` |
| `mv`    | Moves or renames files or directories | `mv file1.txt /home/user/` |
| `rm`    | Removes files or directories | `rm file1.txt` |
| `mkdir` | Creates a new directory | `mkdir new_directory` |
| `rmdir` | Removes an empty directory | `rmdir empty_directory` |

## File Viewing and Editing

| Command | Description | Example |
| ------- | ----------- | ------- |
| `cat`   | Concatenates and displays file contents | `cat file1.txt` |
| `less`  | Views file contents one screen at a time | `less file1.txt` |
| `more`  | Similar to `less`, but with basic functionality | `more file1.txt` |
| `nano`  | Text editor for editing files | `nano file1.txt` |
| `vim`   | Powerful text editor for editing files | `vim file1.txt` |
| `head`  | Outputs the first part of files | `head -n 10 file1.txt` |
| `tail`  | Outputs the last part of files | `tail -n 10 file1.txt` |

## Searching and Finding Files

| Command | Description | Example |
| ------- | ----------- | ------- |
| `find`  | Searches for files in a directory hierarchy | `find /home/user -name file1.txt` |
| `grep`  | Searches text using patterns | `grep 'search_term' file1.txt` |
| `locate`| Finds files by name | `locate file1.txt` |

## Permissions and Ownership

| Command | Description | Example |
| ------- | ----------- | ------- |
| `chmod` | Changes file modes or Access Control Lists | `chmod 755 file1.txt` |
| `chown` | Changes file owner and group | `chown user:group file1.txt` |
| `chgrp` | Changes group ownership of files | `chgrp group file1.txt` |

## File Compression

| Command | Description | Example |
| ------- | ----------- | ------- |
| `tar`   | Archives multiple files into a single file | `tar -cvf archive.tar file1.txt` |
| `gzip`  | Compresses files | `gzip file1.txt` |
| `gunzip`| Decompresses files | `gunzip file1.txt.gz` |
| `bzip2` | Compresses files using the Burrows-Wheeler block-sorting text compression algorithm | `bzip2 file1.txt` |
| `bunzip2`| Decompresses files | `bunzip2 file1.txt.bz2` |
| `zip`   | Packages and compresses files | `zip archive.zip file1.txt` |
| `unzip` | Extracts compressed files from a ZIP archive | `unzip archive.zip` |

## Filesystem Management

| Command | Description | Example |
| ------- | ----------- | ------- |
| `mount` | Mounts a filesystem | `mount /dev/sda1 /mnt` |
| `umount`| Unmounts a filesystem | `umount /mnt` |
| `df`    | Reports filesystem disk space usage | `df -h` |
| `du`    | Estimates file space usage | `du -sh /home/user/` |
| `fdisk` | Manipulates disk partition table | `fdisk /dev/sda` |
| `parted`| Manages disk partitions | `parted /dev/sda` |
| `lsblk` | Lists information about block devices | `lsblk` |

## User and Group Management

| Command | Description | Example |
| ------- | ----------- | ------- |
| `useradd` | Creates a new user | `useradd newuser` |
| `usermod` | Modifies a user account | `usermod -aG sudo newuser` |
| `userdel` | Deletes a user account | `userdel newuser` |
| `groupadd`| Creates a new group | `groupadd newgroup` |
| `groupdel`| Deletes a group | `groupdel newgroup` |
| `passwd`  | Changes user passwords | `passwd newuser` |
| `chage`   | Changes user password expiry information | `chage -l newuser` |

## Networking Basics

| Command | Description | Example |
| ------- | ----------- | ------- |
| `ifconfig` | Configures a network interface (deprecated) | `ifconfig eth0 up` |
| `ip`       | Shows/manages routing, devices, policy routing, and tunnels | `ip addr show` |
| `ping`     | Sends ICMP ECHO_REQUEST to network hosts | `ping google.com` |
| `traceroute` | Traces the route packets take to a network host | `traceroute google.com` |
| `netstat`  | Prints network connections, routing tables, interface statistics, masquerade connections, and multicast memberships | `netstat -tuln` |
| `ss`       | Another utility to investigate sockets | `ss -tuln` |
| `ssh`      | OpenSSH SSH client (remote login program) | `ssh user@hostname` |
| `scp`      | Securely copies files between hosts | `scp file1.txt user@hostname:/path/to/destination` |
| `sftp`     | Secure file transfer program | `sftp user@hostname` |

## Package Management

| Command | Description | Example |
| ------- | ----------- | ------- |
| `apt-get` | Handles packages for Debian-based distributions (e.g., Ubuntu) | `apt-get install package_name` |
| `yum`     | Handles packages for RPM-based distributions (e.g., CentOS) | `yum install package_name` |
| `dnf`     | Next-generation version of `yum` for RPM-based distributions | `dnf install package_name` |
| `zypper`  | Manages packages for openSUSE and SUSE Linux Enterprise | `zypper install package_name` |

## Process Management

| Command | Description | Example |
| ------- | ----------- | ------- |
| `ps`    | Reports a snapshot of current processes | `ps aux` |
| `top`   | Displays tasks and system information | `top` |
| `htop`  | Interactive process viewer | `htop` |
| `kill`  | Sends a signal to a process | `kill -9 pid` |
| `pkill` | Sends a signal to a process by name | `pkill -f process_name` |
| `killall`| Kills processes by name | `killall process_name` |

## Scheduling Tasks

| Command | Description | Example |
| ------- | ----------- | ------- |
| `cron`  | Daemon to execute scheduled commands | `crontab -e` (to edit cron jobs) |
| `crontab` | Maintains crontab files for individual users | `crontab -l` (to list cron jobs) |
| `at`    | Schedules commands to be executed at a later time | `echo "sh backup.sh" | at 02:00` |

## System Monitoring and Performance Tuning

| Command | Description | Example |
| ------- | ----------- | ------- |
| `vmstat` | Reports virtual memory statistics | `vmstat 2 5` |
| `iostat` | Reports CPU and I/O statistics | `iostat -d 2` |
| `sar`    | Collects, reports, or saves system activity information | `sar -u 2 5` |
| `free`   | Displays the amount of free and used memory in the system | `free -h` |
| `uptime` | Tells how long the system has been running | `uptime` |
| `dstat`  | Versatile resource statistics display tool | `dstat` |
| `journalctl` | Queries and displays messages from the journal | `journalctl -xe` |

## Security

| Command | Description | Example |
| ------- | ----------- | ------- |
| `iptables` | Administers IP packet filter rules | `iptables -L` |
| `firewalld`| Manages firewall with zones | `firewall-cmd --get-default-zone` |
| `ssh-keygen` | Generates an SSH key pair | `ssh-keygen -t rsa` |

## Backup and Recovery

| Command | Description | Example |
| ------- | ----------- | ------- |
| `rsync` | Fast, versatile, remote (and local) file-copying tool | `rsync -avz /source/ /destination/` |
| `tar`   | Archives and extracts files | `tar -cvf backup.tar /path/to/directory` |
| `dd`    | Converts and copies files | `dd if=/dev/sda of=/path/to/backup.img` |

## Shell Scripting

| Command | Description | Example |
| ------- | ----------- | ------- |
| `bash
