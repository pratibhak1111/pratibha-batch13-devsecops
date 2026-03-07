# Module 2 – Tasks | Linux & Shell Scripting

This module focuses on building **real Linux server skills**
required for DevOps and Cloud roles.

Tasks combine **hands-on execution** with **necessary understanding**
to prepare you for real production environments.

Complete tasks in sequence.

---

## Task 1 – Linux Introduction & OS Details

### Objective
Understand Linux as an operating system.

### What You Need to Do
- Check Linux distribution and version
- Check kernel version
- Explain why Linux is preferred for servers

### Deliverables
- Command outputs
- Short explanation

### Interview Connect
- Why Linux dominates DevOps environments?

---

## Task 2 – Basic Linux Navigation

### Objective
Navigate the Linux filesystem confidently.

### What You Need to Do
- Use `pwd`, `ls`, `cd`
- Create directories and files
- Remove files and directories

### Deliverables
- Command outputs

### Interview Connect
- Difference between relative and absolute paths?

---

## Task 3 – File Operations

### Objective
Manage files like a DevOps engineer.

### What You Need to Do
- Copy and move files
- Rename files
- Use wildcard operations

### Deliverables
- Command outputs

### Interview Connect
- How do you safely move files on servers?

---

## Task 4 – Viewing Files

### Objective
Read files efficiently on servers.

### What You Need to Do
- Use `cat`, `less`, `more`
- Use `head` and `tail`

### Deliverables
- File viewing output

### Interview Connect
- Why is `less` preferred over `cat` for logs?

---

## Task 5 – File Editing (Vim & Nano)

### Objective
Edit files on Linux servers.

### What You Need to Do
- Edit a file using `nano`
- Edit the same file using `vim`
- Save changes safely

### Deliverables
- File before/after proof

### Interview Connect
- Why vim is commonly used in production?

---

## Task 6 – Linux Directory Structure

### Objective
Understand Linux filesystem layout.

### What You Need to Do
- Explore `/bin`, `/sbin`, `/etc`
- Explore `/var`, `/var/log`
- Explore `/home`, `/opt`, `/tmp`, `/proc`

### Deliverables
- Directory listings

### Interview Connect
- Where do logs and configs live?

---

## Task 7 – Log Monitoring

### Objective
Monitor logs in real time.

### What You Need to Do
- Identify a system log file
- Monitor it using `tail -f`

### Deliverables
- Log monitoring output

### Interview Connect
- How do you debug issues using logs?

---

## Task 8 – Virtual Machine Basics

### Objective
Understand VM components.

### What You Need to Do
- Identify CPU, RAM, Disk, Network of VM
- Explain ports and networking at high level

### Deliverables
- VM details output

### Interview Connect
- VM vs physical server?

---

## Task 9 – SSH Access

### Objective
Access Linux servers securely.

### What You Need to Do
- Connect to VM using SSH
- Verify SSH port

### Deliverables
- SSH login proof

### Interview Connect
- What is SSH?

---

## Task 10 – SSH Key-Based Authentication

### Objective
Secure server access.

### What You Need to Do
- Configure SSH key-based authentication
- Disable password login (if possible)

### Deliverables
- SSH config proof

### Interview Connect
- Why key-based auth is more secure?

---

## Task 11 – Elastic IP Association

### Objective
Understand static IPs in cloud.

### What You Need to Do
- Allocate Elastic IP
- Associate with instance
- Verify connectivity

### Deliverables
- Elastic IP proof

### Interview Connect
- Why Elastic IP is used?

---

## Task 12 – curl Usage

### Objective
Test HTTP endpoints.

### What You Need to Do
- Use `curl` to check website status
- Fetch headers

### Deliverables
- curl output

### Interview Connect
- How do you test APIs from server?

---

## Task 13 – wget Usage

### Objective
Download files on Linux.

### What You Need to Do
- Download a file using `wget`
- Verify download

### Deliverables
- Download proof

### Interview Connect
- wget vs curl?

---

## Task 14 – Process Listing

### Objective
View running processes.

### What You Need to Do
- Use `ps`
- Use `top` or `htop`

### Deliverables
- Process outputs

### Interview Connect
- How do you find high CPU processes?

---

## Task 15 – Process Control

### Objective
Manage running processes.

### What You Need to Do
- Run process in background
- Kill process gracefully
- Kill process forcefully

### Deliverables
- Kill command proof

### Interview Connect
- kill vs kill -9?

---

## Task 16 – Disk Usage Analysis

### Objective
Analyze disk usage.

### What You Need to Do
- Use `df`
- Use `du`
- Identify large directories

### Deliverables
- Disk usage output

### Interview Connect
- How do you debug disk full issues?

---

## Task 17 – Disk Mounting

### Objective
Work with disks and filesystems.

### What You Need to Do
- Mount a filesystem
- Unmount it

### Deliverables
- Mount output

### Interview Connect
- What is mounting?

---

## Task 18 – Persistent Mounts

### Objective
Persist disk mounts.

### What You Need to Do
- Configure `/etc/fstab`
- Verify persistent mount

### Deliverables
- fstab entry proof

### Interview Connect
- Why persistent mounts matter?

---

## Task 19 – NFS Setup

### Objective
Share storage across servers.

### What You Need to Do
- Configure NFS server
- Configure NFS client

### Deliverables
- NFS mount proof

### Interview Connect
- When is NFS used?

---

## Task 20 – Linux Networking Basics

### Objective
Understand network configuration.

### What You Need to Do
- Check IP address
- Check interfaces
- Check open ports

### Deliverables
- Networking output

### Interview Connect
- How do you debug network issues?

---

## Task 21 – DNS & Connectivity

### Objective
Understand name resolution.

### What You Need to Do
- Use `ping`
- Use `nslookup` or `dig`
- Test DNS resolution

### Deliverables
- DNS lookup output

### Interview Connect
- What happens when you hit a URL?

---

## Task 22 – Firewall Management (UFW)

### Objective
Secure Linux servers.

### What You Need to Do
- Install and enable UFW
- Allow SSH, HTTP, HTTPS
- Deny unused port

### Deliverables
- UFW rules output

### Interview Connect
- Firewall vs security group?

---

## Task 23 – Linux Error: Permission Denied

### Objective
Fix permission issues.

### What You Need to Do
- Create permission denied scenario
- Fix using correct permissions

### Deliverables
- Error and fix proof

### Interview Connect
- Why permission issues occur?

---

## Task 24 – Linux Error: Resource Issue

### Objective
Troubleshoot resource issues.

### What You Need to Do
Fix **any one**:
- High CPU usage
- High memory usage
- Disk full issue

### Deliverables
- Before/after proof

### Interview Connect
- How do you approach production issues?

---

## Task 25 – Shell Scripting & Automation

### Objective
Automate operational tasks.

### What You Need to Do
- Write a shell script using:
  - Variables
  - Conditions
  - Loops
- Monitor website or service
- Schedule script using cron

### Deliverables
- Script file
- Cron job proof

### Interview Connect
- Why automation is critical in DevOps?

---

## 🌍 Learn in Public (Mandatory)

After completing this module:

1. Push your work to your forked GitHub repo  
2. Post your learning on LinkedIn explaining:
   - What you worked on
   - What issues you faced
   - How you fixed them
3. Tag:
   - **Aditya Jaiswal**
   - **DevOps Shack**

Once you tag, your **task and repository will be reviewed**.

Use hashtags:

```
#Batch13 #Linux #DevOps #ShellScripting #LearnInPublic #devopsshack
```

---

## 🎯 Outcome of Module-2

After completing Module-2, you should be able to:
- Work confidently on Linux servers
- Secure and manage VMs
- Handle users, permissions, and processes
- Automate basic operational tasks
- Troubleshoot real production issues
- Answer Linux interview questions confidently

