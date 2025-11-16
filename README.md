# RHCSA (Red Hat Certified System Administrator)
The RHCSA is a performance-based certification from Red Hat that validates your ability to handle real system-administration tasks on Red Hat Enterprise Linux. You’re not answering multiple-choice questions—you’re working on a live system and solving tasks exactly like you would in a real job. 

Here’s a **practice-task list** built to mirror the actual style and pressure of the RHCSA exam. These aren’t theory prompts—they’re the kinds of real, hands-on tasks you’d need to complete successfully **on a live system**.

If you can perform every task below without searching the web or notes—and repeat them quickly—you’re exam-ready.

---

# **RHCSA-Style Practice Task List**

## **1. User & Group Administration**

1. Create a user with a specific UID.
2. Create a group and add multiple users to it.
3. Set a password expiration policy (max days, warning days).
4. Configure a system so a user has a restricted shell.
5. Create a user with a primary group and two secondary groups.
6. Lock and unlock user accounts.
7. Configure directory **/project** so:

   * owned by a group
   * group members can collaborate
   * others have no access

---

## **2. Permissions, ACLs & SELinux**

1. Apply ACLs so a specific user has read-only access to a directory.
2. Set default ACLs on a project folder.
3. Diagnose and fix a permission denied issue caused by SELinux.
4. Change the SELinux context of a directory so Apache can read it.
5. Temporarily set SELinux to permissive, then restore enforcing mode.
6. Restore default SELinux contexts using `restorecon`.

---

## **3. Storage & LVM**

1. Create a new physical volume.
2. Create a volume group from two disks.
3. Create a logical volume and format it as XFS.
4. Mount the filesystem persistently via `/etc/fstab`.
5. Extend a logical volume AND the filesystem.
6. Reduce an LVM volume safely (requires unmount + resize2fs + lvreduce if ext4).
7. Create and activate a swap partition or swap file.

---

## **4. Networking**

1. Set a static IP, gateway, DNS using `nmcli`.
2. Change the hostname and ensure it persists after reboot.
3. Create an additional network connection profile.
4. Enable and verify network autoconnect behavior.

---

## **5. System Services & Boot Process**

1. Enable a service to start on boot.
2. Mask a service so it cannot start at all.
3. Boot the system into rescue mode.
4. Reset the root password from the GRUB menu.
5. Fix a broken boot caused by an incorrect `/etc/fstab` entry.
6. Investigate service failures using `journalctl`.

---

## **6. Software Management**

1. Configure a new software repository (local or remote).
2. Install a specific version of a package.
3. Remove a package and verify all dependencies.
4. Query which package a file belongs to.
5. Create a simple bash script that installs a package list automatically.

---

## **7. Firewalld & Security**

1. Open a port permanently and reload firewall rules.
2. Allow a predefined service (like http or ssh) through firewalld.
3. Create and enable a rich rule allowing a specific IP.
4. Configure SSH so root login is disabled and password auth is optional.

---

## **8. File Sharing & Transfer (often included indirectly)**

1. Configure a basic **VDO volume** if your exam version includes it.
2. Set up a simple **autofs** mount.
3. Create a tar archive and extract it to a precise location.

---

## **9. Scripting (Lightweight Tasks)**

1. Write a script that:

   * Accepts an argument
   * Creates a directory if it doesn’t exist
   * Logs output to `/var/log/custom.log`
2. Write a script using conditional checks to start or stop a service.
3. Automate the creation of 10 users from a text file.

---

# **10. Exam-Style Comprehensive Scenarios**

Try combining tasks like these into a single session:

### **Scenario A**

* Create an LVM volume
* Create a filesystem on it
* Mount it persistently
* Set ACLs so user1 has full access, user2 has read-only
* Ensure SELinux permits access

### **Scenario B**

* Configure a static network profile
* Enable an HTTP server
* Allow HTTP through the firewall
* Change SELinux context so Apache can serve files from a custom directory

### **Scenario C**

* Fix a boot failure caused by a typo in `/etc/fstab`
* Reset the root password
* Fix a misconfigured service
* Create a script that configures users and groups

---
