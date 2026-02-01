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
init / systemd: it is the very 1st process started during the boot.systemd is the init system.
Starts system services (network, ssh, nginx, docker) and can do Start / stop / restart services.
systemd is responsible for:
Starting system services (network, ssh, cron, etc.)
Managing service dependencies
Monitoring and restarting services
Handling system states (boot, shutdown, reboot)

The PID(processId) for systemd is 1 by default.

**Few basic process commands:**
ps : to check the realtime running processes.
top : to check detailed info about the running processes.

**Process types:** 
Running process(R): the process that is currecntly in running on cpu and can be check using ps or top command.
Sleeping process(S): process is waiting for an event, user input, disk space or network response.
Uninterruptible Sleep (D): can not be interupted or kill easily.Many D state processes usually indicate storage or network problems.
Zombie (Z): process has finished the execution but not exited.consuming no cpu/memory but still has pid.
ps aux | grep Z

systemd commands:
systemctl start nginx:start nginx
systemctl stop nginx: stop nginx
systemctl restart nginx: restat the nginx server
systemctl status nginx: check the status

