# Linux Architecture – Cheat Code 

## Linux Architecture Diagram

Applications / Utilities
        ↓
      Shell
        ↓
      Kernel
        ↓
     Hardware

## Easy Memory Trick

A - S - K - H

Application → Shell → Kernel → Hardware

# 1. Hardware 🖥️

The physical base of the system including:

- CPU
- Memory (RAM)
- Storage devices
- Peripheral devices

### Key Point
Hardware is the base layer of the Linux system.

# 2. Kernel 

The Kernel is the brain of the Operating System.

It:
- Manages hardware resources
- Provides services to upper layers
- Runs in privileged Kernel Space

## Main Functions of Kernel

### Process Management
- Schedules and manages running tasks/processes

### Memory Management
- Allocates and tracks RAM usage

### Device Drivers
- Acts as interface to hardware devices

### File System Management
- Handles files and directories

### Security & Permissions
- Controls access and system security

### Important
Kernel directly communicates with hardware.

---

# 3. System Libraries 📚

System libraries contain standard functions used by applications.

### Example
- glibc (GNU C Library)

### Purpose
- Helps applications interact with kernel through system calls

### Flow

Application → Library → Kernel

---

# 4. Shell 💻

Shell is the interface between user and kernel.

It:
- Takes human-readable commands
- Converts them into kernel-understandable format
- Displays output

## Common Shells
- Bash
- Zsh
- Sh

## Example Commands

```bash
ls
cp
pwd
mv
cat
echo   
