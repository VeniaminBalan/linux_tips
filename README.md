# Useful Linux Commands

A collection of useful Linux commands for daily use, system administration, and development.

---

## 🖥️ System Information
- `uname -r`  
  Show Linux kernel version.
- `lsb_release -a`  
  Show OS version and details.
- `uptime`  
  Show how long the system has been running.
- `hostnamectl`  
  Show or change the hostname.
- `whoami`  
  Show current logged-in user.
- `who`  
  Show all logged-in users.

---

## 💁️ User Management
- `id`  
  Show user ID and group ID.
- `who`  
  Show who is logged in.
- `users`  
  Show currently logged-in users.
- `sudo useradd newuser`  
  Create a new user.
- `sudo passwd newuser`  
  Set a password for a user.
- `sudo userdel -r username`  
  Delete a user and their home directory.
- `sudo usermod -aG groupname username`  
  Add a user to a group.
- `groups username`  
  Show groups a user belongs to.
- `sudo deluser username groupname`  
  Remove a user from a group.

---

## 🔧 Managing Users in Docker
- `sudo groupadd docker`  
  Create the Docker group if it doesn't exist.
- `sudo usermod -aG docker $USER`  
  Add the current user to the Docker group.
- `newgrp docker`  
  Apply changes without logging out.
- `sudo systemctl restart docker`  
  Restart Docker to apply changes.
- `docker ps`  
  Verify the user can run Docker commands without `sudo`.

---

## 📁 File and Directory Management
- `ls -la`  
  List all files and directories (including hidden) with details.
- `pwd`  
  Show current directory path.
- `cd /path/to/dir`  
  Change directory.
- `mkdir newdir`  
  Create a new directory.
- `rm filename`  
  Delete a file.
- `rm -r dirname`  
  Delete a directory and its contents.
- `mv old new`  
  Rename/move a file or directory.
- `cp file1 file2`  
  Copy a file.
- `cp -r dir1 dir2`  
  Copy a directory.
- `find / -name "file.txt"`  
  Find a file by name.

---

## 🛠️ File Permissions and Ownership
- `chmod 755 file`  
  Change file permissions (rwxr-xr-x).
- `chown user:group file`  
  Change file owner.
- `ls -l`  
  View permissions of files.

---

## 💪 Disk and Storage
- `df -h`  
  Show disk usage in human-readable format.
- `du -sh dir`  
  Show size of a directory.
- `lsblk`  
  List available disk partitions.
- `mount /dev/sdX /mnt`  
  Mount a device.
- `umount /mnt`  
  Unmount a device.

---

## 📶 Network
- `ip a`  
  Show all network interfaces and IP addresses.
- `ping google.com`  
  Test network connectivity.
- `netstat -tulnp`  
  Show open ports and listening services.
- `curl ifconfig.me`  
  Get public IP address.
- `traceroute google.com`  
  Show the route to a server.

---

## 🛠️ Process and System Monitoring
- `top`  
  Show real-time system processes.
- `htop`  
  Interactive process viewer (if installed).
- `ps aux`  
  Show all running processes.
- `kill PID`  
  Kill a process by its PID.
- `killall process`  
  Kill a process by name.
- `free -h`  
  Show available RAM.
- `uptime`  
  Show system uptime and load average.

---

## 🐩 Docker
- `docker ps`  
  Show running containers.
- `docker images`  
  List all Docker images.
- `docker stop container_id`  
  Stop a container.
- `docker rm container_id`  
  Remove a container.
- `docker rmi image_id`  
  Remove an image.
- `docker exec -it container bash`  
  Enter a running container.

---

## 💬 SSH and File Transfer
- `ssh user@server`  
  Connect to a remote server via SSH.
- `scp file user@server:/path`  
  Securely copy file to server.
- `rsync -avz /source/ user@server:/destination/`  
  Sync files between machines.

---

## 💪 Compression & Archiving
- `tar -cvf archive.tar file_or_dir`  
  Create a tar archive.
- `tar -xvf archive.tar`  
  Extract a tar archive.
- `zip -r archive.zip dir`  
  Create a zip archive.
- `unzip archive.zip`  
  Extract a zip archive.
- `7z x archive.7z`  
  Extract a .7z archive (if p7zip installed).

---

## ⚡ Package Management
**Ubuntu/Debian (APT)**  
- `sudo apt update`  
  Update package lists.
- `sudo apt upgrade`  
  Upgrade installed packages.
- `sudo apt install pkg`  
  Install a package.
- `sudo apt remove pkg`  
  Remove a package.

---

## 🔥 Miscellaneous
- `history`  
  Show command history.
- `alias ll="ls -la"`  
  Create a shortcut for commands.
- `echo "text" > file.txt`  
  Write text to a file.
- `cat file.txt`  
  View file contents.
- `nano file.txt`  
  Open file in a simple text editor.
- `wget URL`  
  Download a file from a URL.

---

## Notes
- Use `sudo` before commands that require administrative privileges.
- The `htop` command provides a more user-friendly, interactive version of `top`, and can be installed via `sudo apt install htop` (on Debian-based systems).
- `docker exec` allows you to interact with containers without stopping them.

