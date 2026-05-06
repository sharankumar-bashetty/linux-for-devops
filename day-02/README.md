# Linux Process Management Guide

A process is an instance of a running program. Linux provides multiple utilities to monitor, manage, and control processes effectively.

Each process:
- Has a unique Process ID (PID)
- Belongs to a parent process

---

## Viewing Processes

- `ps aux` – View all running processes  
- `ps -u username` – View processes for a specific user  
- `ps -C processname` – Show a process by name  
- `pgrep processname` – Find a process and return its PID  
- `pidof processname` – Find the PID of a running program  

---

## Managing Processes

- `kill PID` – Terminate a process by PID  
- `pkill processname` – Terminate a process by name  
- `kill -9 PID` – Force kill a process  
- `pkill -9 processname` – Kill all instances of a process  
- `kill -STOP PID` – Stop a running process  
- `kill -CONT PID` – Resume a stopped process  

---

## Background and Foreground Processes

- `command &` – Run a command in the background  
- `jobs` – List background jobs  
- `fg %jobnumber` – Bring a job to the foreground  
- `Ctrl + Z` – Suspend a running process  
- `bg %jobnumber` – Resume a suspended process in the background  

---

## Monitoring System Processes

- `top` – Interactive process viewer  
- `htop` – User-friendly process viewer (requires installation)  
- `nice -n 10 command` – Run a command with a specific priority  
- `renice -n -5 -p PID` – Change priority of an existing process  

---

## Managing Services (Daemon Processes)

- `systemctl list-units --type=service` – List all services  
- `systemctl start service-name` – Start a service  
- `systemctl stop service-name` – Stop a service  
- `systemctl enable service-name` – Enable a service at startup  

---

## Notes

- Avoid using `kill -9` unless necessary  
- Monitor processes before taking action  
- Use `top` or `htop` for real-time debugging  
- Prefer `systemctl` for managing services  

---

### Disk and Storage Management

Managing disks and storage efficiently is crucial for system performance and stability. Linux provides various commands to monitor, partition, format, mount, and manage disk storage.

### View Disk Info

- `lsblk` – Display block devices  
- `fdisk -l` – List disk partitions  
- `blkid` – Show UUIDs of devices  
- `df -h` – Check disk space usage  
- `du -sh /path` – Show size of a directory  

### Partition

- `fdisk /dev/sdX` – Create and manage partitions  
- `parted /dev/sdX` – Alternative to fdisk for GPT disks  
- `mkfs.ext4 /dev/sdX1` – Format a partition as ext4  
- `mkfs.xfs /dev/sdX1` – Format a partition as XFS  

### Mount and Unmount

- `mount /dev/sdX1 /mnt` – Mount a partition  
- `umount /mnt` – Unmount a partition  
- `mount -o remount,rw /mnt` – Remount a partition as read-write  