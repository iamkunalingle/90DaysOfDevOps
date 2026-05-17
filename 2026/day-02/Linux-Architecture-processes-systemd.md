# Linux Architecture, Processes & Systemd – Cheat Code

# Linux Architecture, Processes & Systemd – Cheat Code 🚀

---

# 1. Core Components of Linux

Linux follows a monolithic layered architecture that separates hardware operations from user applications.

## Architecture Layers

User Space
↓
Kernel Space
↓
Init / systemd (PID 1)
↓
Hardware

---

## Kernel

The Kernel is the core brain of Linux.

### Responsibilities
- Manages CPU
- Manages memory
- Controls hardware devices
- Enforces security

### Important
Runs in privileged Kernel Space.

---

## User Space

Where:
- Applications
- Daemons
- Shells

### Important
Applications must request resources using System Calls.

---

## Init / systemd

The first process started by kernel.

### PID
PID = 1

### Responsibilities
- Initializes user space
- Starts/stops services
- Manages system state

# 2. How Processes Are Created and Managed

Linux manages processes using a parent-child hierarchy.

## Fork-Exec Model

Linux creates new processes using two major system calls.

### 1. fork()

Creates an exact duplicate (child process) of parent process.

### 2. exec()

Replaces child process memory with a new program.

## Process States

| State | Meaning |
|---|---|
| R (Running) | Using CPU |
| S (Sleeping) | Waiting for event/resource |
| Z (Zombie) | Dead process waiting for parent acknowledgement |
| Orphan | Parent died, adopted by systemd |

## Process Management Tools

### View running processes

bash
top
htop

## View process tree
pstree

## Send SIGTERM
kill <PID>

## Force Kill(SIGKILL)
kill -9 <PID>

## What systemd Does and Why It Matters
systemd is the modern Linux init and service manager.

# Core Responsibilities
Parent of all processes (PID 1)
Mounts filesystems
Starts/stops services
Manages system state

# Why systemd is Important for DevOps
Parallel Startup
Starts services in parallel for faster boot.
Dependency Management
Understands service dependencies automatically.
Example: Nginx requires network before startup.

## Essential systemd Commands

# Start Service
Bash
sudo systemctl start <service_name>

# Stop Service
Bash
sudo systemctl stop <service_name>

# Enable on Boot
Bash
sudo systemctl enable <service_name>

# Check Status
Bash
sudo systemctl status <service_name>

# View Logs
Bash
journalctl

# Service Specific Logs
Bash
journalctl -u <service_name>

# Real-Time Logs
Bash
journalctl -f

## Quick Commands Reference

# Boot Time Analysis
Bash
systemd-analyze

# Check Unit File
Bash
systemctl cat <service_name>

## Key Takeaways 🔥
Linux uses layered architecture.
Kernel manages hardware resources.
Processes are created using fork() + exec().
systemd manages services and logs.
systemctl controls services.
journalctl views logs.
## Flow 🔥
User ↓ Shell ↓ System Calls ↓ Kernel ↓ Hardware ↓ Output
