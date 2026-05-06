A process is an instance of a running program. Linux provides multiple utilities to monitor, manage, and control processes effectively. Each process has a unique Process ID (PID) and belongs to a parent process.

Commands used for viewing purpose:
ps aux – View all running processes
ps -u username – View processes for a specific user
ps -C processname – Show a process by name
pgrep processname – Find a process by name and return its PID
pidof processname – Find the PID of a running program


For managing processes:
kill PID – Terminate a process by PID
pkill processname – Terminate a process by name
kill -9 PID – Force kill a process
pkill -9 processname – Kill all instances of a process
kill -STOP PID – Stop a running process
kill -CONT PID – Resume a stopped process

Background process:
command & – Run a command in the background
jobs – List background jobs
fg %jobnumber – Bring a job to the foreground
Ctrl + Z – Suspend a running process
bg %jobnumber – Resume a suspended process in the background

Monitoring system proceses:
top – Interactive process viewer
htop – User-friendly process viewer (requires installation)
nice -n 10 command – Run a command with a specific priority
renice -n -5 -p PID – Change priority of an existing process

Engine processes:
systemctl list-units --type=service – List all system daemons
systemctl start service-name – Start a daemon/service
systemctl stop service-name – Stop a daemon/service
systemctl enable service-name – Enable a service at startup