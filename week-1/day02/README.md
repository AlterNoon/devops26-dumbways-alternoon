# Day 2 - Basic Shell & Networking

## Diagram

Buat sebuah diagram sebuah jaringan komputer dengan 4 device dengan kondisi :
- IP Class C : 192.168.4.xxx
- CIDR Block : 192.168.4.0/24

![1](/week-1/day02/images/topo.drawio.png)

## Perbedaan antara SH (Shell) dan BASH (Bourne-Again Shell)

Shell secara sederhana adalah program yang menyediakan traditional text only user interface for linux/unix/mac, biasanya digunakan in older system untuk running basic shell script. 
Sedangkan bash menyediakan lebih banyak fitur dan user-friendly environment.
Perbedaan yang mencolok adalah shell menyediakan fitur basic (biasanya untuk simple scripting), syntax yang dipakai lebih simple, dan didesign untuk kompatible di semua unix system.
sedangkan bash menyediakan fitur array, function, serta syntax yang dipakai lebih advanced, dan tidak selalu compatible dengan unix system.


## Basic Command
| Command    | Description                | How to use             |
| ---------- | -------------------------- | ---------------------- |
| `echo`     | Write/add text             | `echo`                 |
| `pwd`      | Show current directory     | `pwd`                  |
| `ls`       | List directory contents    | `ls -la`               |
| `tree`     | Show folder structure      | `tree`                 |
| `cd`       | Change directory           | `cd /var/www`          |
| `cd ..`    | Go up one level            | `cd ..`                |
| `mkdir`    | Create directory           | `mkdir project`        |
| `rmdir`    | Remove empty directory     | `rmdir folder`         |
| `rm`       | Remove file                | `rm file.txt`          |
| `rm -r`    | Remove directory           | `rm -r folder`         |
| `cp`       | Copy file                  | `cp a.txt b.txt`       |
| `cp -r`    | Copy directory             | `cp -r src dst`        |
| `mv`       | Move / rename              | `mv old.txt new.txt`   |
| `basename` | Extract filename from path | `basename /home/a.txt` |
| `dirname`  | Extract directory path     | `dirname /home/a.txt`  |

## File View & Edit
| Command      | Description             | How to use            |
| ------------ | ----------------------- | --------------------- |
| `cat`        | Show file content       | `cat file.txt`        |
| `tac`        | Reverse cat             | `tac file.txt`        |
| `less`       | View file page by page  | `less file.txt`       |
| `more`       | View file (older pager) | `more file.txt`       |
| `head`       | First lines             | `head -n 20 file.txt` |
| `tail`       | Last lines              | `tail -n 20 file.txt` |
| `tail -f`    | Live log monitoring     | `tail -f app.log`     |
| `nano`       | Simple editor           | `nano file.txt`       |
| `vi` / `vim` | Advanced editor         | `vim file.txt`        |

## Search
| Command   | Description                | How to use                |
| --------- | -------------------------- | ------------------------- |
| `grep`    | Search text                | `grep "error" log.txt`    |
| `grep -r` | Recursive search           | `grep -r "db" .`          |
| `find`    | Find files                 | `find . -name "*.js"`     |
| `locate`  | Fast file search           | `locate nginx.conf`       |
| `which`   | Program location           | `which python`            |
| `whereis` | Binary & man page location | `whereis bash`            |
| `awk`     | Text processing            | `awk '{print $1}' file`   |
| `sed`     | Stream editor              | `sed 's/a/b/' file`       |
| `sort`    | Sort lines                 | `sort file.txt`           |
| `uniq`    | Remove duplicates          | `uniq file.txt`           |
| `wc`      | Word/line count            | `wc -l file.txt`          |
| `cut`     | Extract columns            | `cut -d: -f1 /etc/passwd` |

## Process Management
| Command   | Description          | How to use       |
| --------- | -------------------- | ---------------- |
| `top`     | Process monitor      | `top`            |
| `htop`    | Better top           | `htop`           |
| `ps`      | List processes       | `ps aux`         |
| `kill`    | Stop process         | `kill 1234`      |
| `kill -9` | Force kill           | `kill -9 1234`   |
| `bg`      | Resume in background | `bg`             |
| `fg`      | Resume in foreground | `fg`             |
| `jobs`    | Show jobs            | `jobs`           |
| `nice`    | Set priority         | `nice -n 10 cmd` |
| `uptime`  | System uptime        | `uptime`         |

## Networking
| Command      | Description          | How to use               |
| ------------ | -------------------- | ------------------------ |
| `ping`       | Test connectivity    | `ping google.com`        |
| `curl`       | Transfer data        | `curl api.site.com`      |
| `wget`       | Download file        | `wget file.zip`          |
| `ifconfig`   | Network config (old) | `ifconfig`               |
| `ip a`       | Show IP info         | `ip a`                   |
| `netstat`    | Network stats        | `netstat -tuln`          |
| `ss`         | Socket stats         | `ss -tuln`               |
| `traceroute` | Network path         | `traceroute google.com`  |
| `nslookup`   | DNS query            | `nslookup google.com`    |
| `ssh`        | Remote login         | `ssh user@ip`            |
| `scp`        | Secure copy          | `scp file user@ip:/home` |


## Storage
| Command    | Description     | How to use         |
| ---------- | --------------- | ------------------ |
| `df -h`    | Disk usage      | `df -h`            |
| `du -sh`   | Folder size     | `du -sh *`         |
| `mount`    | Mounted disks   | `mount`            |
| `umount`   | Unmount disk    | `umount /dev/sdb1` |
| `lsblk`    | Block devices   | `lsblk`            |
| `fdisk -l` | Disk partitions | `fdisk -l`         |

## Permission
| Command   | Description       | How to use          |
| --------- | ----------------- | ------------------- |
| `chmod`   | Change permission | `chmod 755 file`    |
| `chown`   | Change owner      | `chown user file`   |
| `chgrp`   | Change group      | `chgrp dev file`    |
| `sudo`    | Run as root       | `sudo apt update`   |
| `whoami`  | Current user      | `whoami`            |
| `id`      | User identity     | `id`                |
| `adduser` | Add user          | `sudo adduser john` |
| `passwd`  | Change password   | `passwd`            |

## Good to know
| Command       | Description      | How to use              |
| ------------- | ---------------- | ----------------------- |
| `tar -cvf`    | Create tar       | `tar -cvf a.tar folder` |
| `tar -xvf`    | Extract tar      | `tar -xvf a.tar`        |
| `gzip`        | Compress         | `gzip file`             |
| `gunzip`      | Decompress       | `gunzip file.gz`        |
| `zip`         | Zip file         | `zip a.zip file`        |
| `unzip`       | Extract zip      | `unzip a.zip`           |
| `history`     | Command history  | `history`               |
| `clear`       | Clear terminal   | `clear`                 |
| `watch`       | Repeat command   | `watch df -h`           |
| `apt update`  | Update repo      |                         |
| `apt upgrade` | Upgrade packages |                         |
| `apt install` | Install package  |                         |
| `apt remove`  | Remove package   |                         |
| `yum install` | Install package  |                         |
| `yum update`  | Update packages  |                         |
| `Ctrl + C`    | Stop process     |                         |
| `Ctrl + Z`    | Suspend process  |                         |
| `Ctrl + D`    | Exit terminal    |                         |
| `Ctrl + L`    | Clear screen     |                         |
