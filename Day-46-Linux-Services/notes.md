# Day 46 - Linux Services

## Service
A service is a background program that provides specific functions for the system or other applications.

## systemd
systemd is the service manager used to control services in modern Linux systems.

## Common Services
- SSH
- Apache
- Nginx
- MySQL
- Docker
- NetworkManager

## Commands

systemctl list-units --type=service
→ List active services

systemctl status <service>
→ Check service status

sudo systemctl start <service>
→ Start a service

sudo systemctl stop <service>
→ Stop a service

sudo systemctl restart <service>
→ Restart a service

sudo systemctl reload <service>
→ Reload configuration

sudo systemctl enable <service>
→ Start automatically at boot

sudo systemctl disable <service>
→ Prevent automatic startup

## Why It Matters

Services are essential background programs. Cybersecurity analysts monitor them to detect failures, unauthorized changes, or malicious services installed by attackers.
