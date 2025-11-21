Below is a **FULL 3-hour RHCSA simulation exam**, designed to be as close as possible to the real exam in difficulty, length, and structure — without using any copyrighted content or real exam questions.

This is **NOT** a multiple-choice test.
This is a **hands-on, task-driven exam**, exactly like RHCSA.

You should complete it in **3 hours or less**, without internet, just like the real thing.

If you want, I can also grade your results afterward.

---

# 🟥 **RHCSA Full 3-Hour Simulation Exam**

**Total sections:** 10
**Total tasks:** 50
**Passing score target:** ~70%
(You don’t need to perfect every section — same as the real exam.)

---

# 🔵 **SECTION 1 — User & Group Administration (6 tasks)**

1. Create users: `alice`, `bob`, `carol`, and `dave`.
2. Create a group named `staffgrp`.
3. Add `alice` and `bob` to `staffgrp`.
4. Create directory `/projectA`, owned by `staffgrp`.
5. Set SGID bit so files inherit the group.
6. Apply ACLs so:

   * `alice` has **rwx**
   * `carol` has **rx**
   * `others` have **no access**

---

# 🔵 **SECTION 2 — Permissions, ACLs, SELinux (6 tasks)**

1. Create directory `/securedata`.
2. Give `dave` **rw** ACL access (and default ACL).
3. Create a file `/securedata/info.txt` with text of your choice.
4. Label the directory with type `httpd_sys_rw_content_t`.
5. Restore SELinux contexts system-wide.
6. Verify SELinux is set to **Enforcing**.

---

# 🔵 **SECTION 3 — Networking (5 tasks)**

1. Create a static connection profile: `corpnet`

   * Interface: `ens33`
   * IP: `192.168.50.20/24`
   * Gateway: `192.168.50.1`
   * DNS: `8.8.8.8`
2. Ensure `corpnet` autoconnects at boot.
3. Create a secondary DHCP profile `dhcpnet` that does NOT autoconnect.
4. Change system hostname to `server1.example.com`.
5. Make sure the primary connection is active and the system can ping the gateway.

---

# 🔵 **SECTION 4 — Software Repositories & Packages (5 tasks)**

1. Mount the provided ISO at `/mnt/repo`.
2. Create a local repo file `/etc/yum.repos.d/local.repo`.
3. Install package `vim-enhanced`.
4. Install a specific version of `bash` (any version available).
5. Create a script `/root/install_tools.sh` that installs: `git`, `wget`, `tree`.

---

# 🔵 **SECTION 5 — Storage: LVM, Swap, VDO (8 tasks)**

You are given **three blank disks**: `/dev/sdb`, `/dev/sdc`, `/dev/sdd`

### **A. LVM**

1. Create PVs on `/dev/sdb` and `/dev/sdc`.
2. Create VG `vgdata`.
3. Create LV `lvdata` size **8G**.
4. Format as **XFS**.
5. Mount persistently at `/data`.

### **B. Resizing**

6. Extend the LV by **+4G**.
7. Grow the filesystem online.

### **C. Swap**

8. Create a **2G swap file** `/swapfile` and make it persistent.

---

# 🔵 **SECTION 6 — Boot Process & System Services (6 tasks)**

1. Fix a broken boot caused by an incorrect `/etc/fstab` entry.
2. Reboot into rescue mode and reset the root password.
3. Create a custom systemd service: `/usr/local/bin/cleanup.sh`
4. The service should print “cleanup complete” to `/var/log/cleanup.log`.
5. Enable the service at boot.
6. Investigate & fix a failing service named `demoapp.service`.

---

# 🔵 **SECTION 7 — Firewalld (4 tasks)**

1. Open port **8080/tcp** permanently.
2. Enable HTTP service.
3. Block IP `192.168.50.99`.
4. Reload the firewall and verify rules.

---

# 🔵 **SECTION 8 — Apache HTTP Server (4 tasks)**

1. Install `httpd` and enable it.
2. Create a custom document root at `/webroot`.
3. Put an `index.html` file inside it.
4. Configure Apache to use `/webroot` and serve the file.

---

# 🔵 **SECTION 9 — autofs (3 tasks)**

1. Create autofs map so that:

   * Visiting `/misc/data` mounts `localhost:/webroot`.
2. Start and enable autofs.
3. Verify the autofs mount works automatically.

---

# 🔵 **SECTION 10 — Scripting (3 tasks)**

1. Write script `/root/mkdocs.sh` that creates directories from arguments:
   Example:

   ```
   ./mkdocs.sh /opt/app1 /opt/app2
   ```
2. Write script `/root/checksvc.sh` that:

   * Accepts a service name
   * Prints “running” or “stopped”
3. Write script `/root/userbatch.sh` that creates users from `/root/userlist.txt`.

---

# 🟩 **END OF EXAM**

---
