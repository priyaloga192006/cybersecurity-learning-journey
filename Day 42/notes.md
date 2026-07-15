1. Processes
What is a Process?

Definition (One Line):

A process is a program that is currently running in memory.

Real-Life Example

You open:

Chrome
VS Code
Calculator

Each running application becomes a process.

Why It Matters in Cybersecurity

Suppose your computer suddenly becomes slow.

A SOC analyst checks:

Which process is using 100% CPU?
Is it malware?
Is it a legitimate program?

Processes are often the first thing checked during an investigation.

Important Commands
View Running Processes
ps
Detailed Process List
ps -ef
Live Process Monitor
top

Shows:

CPU usage
RAM usage
Running processes
Kill a Process
kill PID

Example

kill 2548

Stops process 2548.

2. Services
What is a Service?

Definition (One Line):

A service is a background program that starts automatically and performs specific tasks.

Unlike normal programs:

You don't open them.
They run continuously.
Examples
SSH
MySQL
Apache
Nginx
Docker
Real-Life Example

Your Wi-Fi works because the networking service is running.

Your website works because the web server service is running.

Commands

Show services

systemctl list-units --type=service

Start service

sudo systemctl start apache2

Stop service

sudo systemctl stop apache2

Restart service

sudo systemctl restart apache2

Check status

systemctl status apache2
Cybersecurity Example

If SSH suddenly stops,

A SOC analyst checks:

systemctl status ssh

to determine whether it crashed or was intentionally stopped.

3. Logs
What is a Log?

Definition (One Line):

A log is a record of system activities and events.

You already learned logs in Windows.

Linux stores logs too.

Common Log Directory
/var/log
Common Log Files

Authentication

/var/log/auth.log

System

/var/log/syslog

Kernel

/var/log/kern.log
Commands

View log

cat /var/log/syslog

View recent lines

tail /var/log/syslog

Watch logs live

tail -f /var/log/syslog
Cybersecurity Example

Someone fails to log in 20 times.

The evidence is stored inside:

/var/log/auth.log
4. Linux Networking

Linux also has networking commands.

Check IP Address
ip addr
Test Internet
ping google.com
Show Routing Table
ip route
DNS Test
nslookup google.com
Network Connections
ss -tuln

Shows:

Open ports
Listening services
Cybersecurity Example

If malware opens a secret port,

A SOC analyst can detect it using:

ss -tuln
5. Package Management
What is Package Management?

Definition (One Line):

Package management is the process of installing, updating, and removing software.

Instead of downloading installers like Windows,

Linux uses package managers.

Ubuntu uses

APT
Update Package List
sudo apt update
Upgrade Installed Software
sudo apt upgrade
Install Software
sudo apt install nmap
Remove Software
sudo apt remove nmap
Search Software
apt search wireshark
Cybersecurity Example

Need Wireshark?

Instead of opening a browser:

sudo apt install wireshark
