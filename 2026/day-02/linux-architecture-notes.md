**This file describes Linux architecture and processes.**

Linux is an operating system that uses a kernel as the core hardware manager.
The kernel is the engine of Linux. It is the central component of the operating system that manages hardware resources and provides essential services to applications through system calls.

The kernel is the heart of Linux.

Linux follows a layered interaction model where applications do not directly access hardware. Instead, they communicate through the shell and system libraries, which interact with the kernel. 
Linux works on "ask" principal.

**Linux Architecture Flow**
User
 ↓
Applications (nginx, docker, kubectl)
 ↓
Shell (bash)
 ↓
System Libraries
 ↓
Linux Kernel
 ↓
Hardware (CPU, RAM, Disk, Network)


A user interacts with applications, and applications execute commands through the shell.
The shell communicates with the kernel using system libraries and system calls.


**Linux Processess:**
init / systemd: 
systemd is responsible for:
Starting system services (network, ssh, cron, etc.)
Managing service dependencies
Monitoring and restarting services
Handling system states (boot, shutdown, reboot)

The PID(processId) for systemd is 1 by default.

**Few basic process commands:**
ps : to check the realtime running processess
top : to check detailed info about the running processess.

systemd commands:
systemctl start nginx:start nginx
systemctl stop nginx: stop nginx
systemctl restart nginx: restat the nginx server
systemctl status nginx: check the status

