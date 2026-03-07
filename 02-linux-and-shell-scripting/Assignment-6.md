# Assignment – Group 6

## Storage, Disk Management, NFS & UFW

*(Detailed · Execution-Heavy · Doc-Aligned)*

---

## Objective

This group trains students to **work safely with storage and shared storage** on Linux.

By the end of this group, students should be able to:

* Identify disks and partitions
* Create partitions and filesystems
* Mount and unmount disks correctly
* Make mounts persistent using `/etc/fstab`
* Share directories using **NFS**
* Control access using **UFW**
* Understand **common failure scenarios**

⚠️ Storage mistakes cause **permanent data loss** — this group enforces caution.

---

## Prerequisites

```bash
whoami
sudo -v
```

**Explanation:**

* `whoami` → confirms current user
* `sudo -v` → confirms sudo access (required for disk, NFS, firewall)

---

# 🔹 PART 1: Disk Observation & Understanding

---

## Task 1: List All Disks and Partitions

```bash
lsblk
```

**Explanation:**

* `lsblk` = list block devices
* Shows:

  * disks (e.g., `sda`, `sdb`)
  * partitions (e.g., `sda1`)
  * mount points
* This is the **first command you run before touching storage**

---

## Task 2: List Filesystems and UUIDs

```bash
lsblk -f
```

**Explanation:**

* `-f` shows:

  * filesystem type (ext4, swap, nfs)
  * UUID
  * mount point
* Helps identify:

  * which partition is formatted
  * which is mounted

---

## Task 3: View Disk Usage

```bash
df -h
```

**Explanation:**

* `df` = disk free
* `-h` = human-readable sizes
* Shows:

  * mounted filesystems only
  * space usage
* Does **not** show unmounted disks

---

## Task 4: Compare `lsblk` vs `df` (Written)

Write answers:

1. Why does `lsblk` show more devices than `df`?
2. Which command shows **unmounted disks**?
3. Which command shows **used disk space**?

---

# 🔹 PART 2: Disk vs Partition (Concept Lock-In)

---

## Task 5: Disk vs Partition (Written)

Explain in simple terms:

* What is a **disk**?
* What is a **partition**?
* Why do we partition disks instead of using them directly?

---

# 🔹 PART 3: Partition Creation (Careful & Controlled)

---

## Task 6: Identify Disk to Work On

```bash
lsblk
```

**Explanation:**

* Identify:

  * OS disk (usually `sda`) → **DO NOT TOUCH**
  * secondary disk (e.g., `sdb`) → can be used
* Choosing wrong disk = OS corruption

---

## Task 7: Start Partition Tool

```bash
sudo fdisk /dev/sdb
```

**Explanation:**

* `fdisk` is a partition editor
* `/dev/sdb` = target disk
* Changes affect disk layout directly

---

### Inside `fdisk` (Write what each does)

| Command | Meaning               |
| ------- | --------------------- |
| `n`     | create new partition  |
| `p`     | primary partition     |
| enter   | accept defaults       |
| `w`     | write changes to disk |

---

## Task 8: Verify Partition Creation

```bash
lsblk
```

**Explanation:**

* New partition appears as `/dev/sdb1`
* Disk → partition mapping confirmed

---

# 🔹 PART 4: Filesystem Creation

---

## Task 9: Create Filesystem

```bash
sudo mkfs.ext4 /dev/sdb1
```

**Explanation:**

* `mkfs` = make filesystem
* `ext4` = filesystem type
* Without filesystem, Linux cannot store files

⚠️ Formatting **erases all data** on the partition

---

## Task 10: Verify Filesystem

```bash
lsblk -f
```

**Explanation:**

* Confirms filesystem exists
* Shows UUID (important for persistence)

---

# 🔹 PART 5: Mounting & Unmounting (Practice Cycles)

---

## Task 11: Create Mount Point

```bash
sudo mkdir /mnt/data
```

**Explanation:**

* Mount point = directory where filesystem appears
* Must exist before mounting

---

## Task 12: Mount the Partition

```bash
sudo mount /dev/sdb1 /mnt/data
```

**Explanation:**

* Attaches filesystem to directory
* Makes data accessible

---

## Task 13: Verify Mount

```bash
df -h
```

**Explanation:**

* Confirms disk is mounted
* Shows size and usage

---

## Task 14: Write Test Data

```bash
cd /mnt/data
touch file1.txt
echo "disk test" > file1.txt
mkdir dir1
ls -l
```

**Explanation:**

* Confirms write access
* Data is stored on mounted disk

---

## Task 15: Unmount Disk

```bash
sudo umount /mnt/data
```

**Explanation:**

* Detaches filesystem
* Required before disk removal
* Prevents data corruption

---

## Task 16: Verify Unmount

```bash
df -h
```

**Explanation:**

* Mounted filesystem disappears
* Files are not deleted — just inaccessible

---

## Task 17: Mount Again

```bash
sudo mount /dev/sdb1 /mnt/data
ls /mnt/data
```

**Explanation:**

* Data reappears
* Confirms persistence on disk

---

# 🔹 PART 6: Persistent Mounting (`/etc/fstab`)

---

## Task 18: Get UUID

```bash
sudo blkid
```

**Explanation:**

* Shows unique identifier for each filesystem
* UUID remains stable across reboots

---

## Task 19: Edit fstab

```bash
sudo vi /etc/fstab
```

Add:

```text
UUID=<uuid>  /mnt/data  ext4  defaults  0  2
```

**Explain columns:**

1. Filesystem identifier
2. Mount point
3. Filesystem type
4. Mount options
5. Dump (backup)
6. fsck order

---

## Task 20: Validate fstab Safely

```bash
sudo mount -a
```

**Explanation:**

* Mounts all fstab entries
* Catches errors **without reboot**

---

## Task 21: fstab Failure Scenario (Written)

Explain:

* What happens if UUID is wrong
* What happens if mount directory missing

---

# 🔹 PART 7: NFS – Network File System

---

## Task 22: NFS Concept (Written)

Explain:

* What NFS is
* Why it is used
* One risk of NFS

---

## Task 23: Install NFS Server

```bash
sudo apt install nfs-kernel-server -y
```

**Explanation:**

* Installs NFS server components
* Enables directory sharing over network

---

## Task 24: Create Shared Directory

```bash
sudo mkdir -p /srv/nfs_share
sudo chmod 777 /srv/nfs_share
```

**Explanation:**

* `/srv` is standard service directory
* `777` allows all access (demo only)

---

## Task 25: Configure Exports

```bash
sudo vi /etc/exports
```

Add:

```text
/srv/nfs_share *(rw,sync,no_subtree_check)
```

**Explanation:**

* Defines exported directories
* Controls access and behavior

---

## Task 26: Apply Export Configuration

```bash
sudo exportfs -ra
sudo exportfs -v
```

**Explanation:**

* Reloads exports
* Confirms active shares

---

# 🔹 PART 8: NFS Client

---

## Task 27: Install Client Tools

```bash
sudo apt install nfs-common -y
```

**Explanation:**

* Required for mounting NFS shares

---

## Task 28: Mount NFS Share

```bash
sudo mkdir /mnt/nfs
sudo mount <server-ip>:/srv/nfs_share /mnt/nfs
```

**Explanation:**

* Remote directory becomes local
* Files written here go to server

---

## Task 29: Verify NFS Mount

```bash
df -h
touch /mnt/nfs/client.txt
```

---

# 🔹 PART 9: UFW – Firewall

---

## Task 30: Check Firewall Status

```bash
sudo ufw status
```

**Explanation:**

* Shows firewall rules
* Confirms if UFW is active

---

## Task 31: Enable Firewall Safely

```bash
sudo ufw allow ssh
sudo ufw enable
```

**Explanation:**

* SSH rule prevents lockout
* Firewall blocks all other traffic by default

---

## Task 32: Allow NFS Traffic

```bash
sudo ufw allow from <client-ip> to any port 2049
```

**Explanation:**

* Port 2049 = NFS
* Restricting IP improves security

---

## Task 33: Delete Firewall Rule

```bash
sudo ufw delete allow 2049
```

**Explanation:**

* Removes rule
* Keeps firewall clean

---

