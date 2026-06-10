# Linux Task 02: Users, Groups & File Permissions

## Objective
[cite_start]The purpose of this task is to master Linux user administration, multi-tenant group provisioning, resource ownership modification, and absolute/symbolic system file permissions configurations[cite: 293].

---

## 👥 Part A: Understanding Users

### 1. Diagnostic Questions & Answers
* [cite_start]**What is your current username?** Based on local environment values, the active user context is `kali`[cite: 200].
* **What is UID?** The **User Identifier (UID)** is a unique numeric integer assigned by the Linux kernel to each system user account to manage security policies and trace session activities. The `root` account is dynamically tied to `0`, while standard service or interactive users use values $\ge 1000$.
* **What is GID?** The **Group Identifier (GID)** is a distinct numeric flag pointing to a primary group profile inside the file system. It helps pool separate user authorization bounds under one group permission matrix.
* [cite_start]**What information does `/etc/passwd` contain?** The `/etc/passwd` database stores core system attributes for localized user accounts[cite: 299, 304]. [cite_start]Each entry holds colons-separated text strings detailing the: `Username`, `Password Placeholder (x)`, `UID`, `Primary GID`, `User Info/GECOS description`, `Home Directory Path`, and default `Command Shell Interface`[cite: 304].

### Verification Screenshots
![User Account Status Output](./screenshots/part_a_user_status.png)

---

## 🛠️ Part B: Create Users & Groups

### 1. System Engineering Sequence
[cite_start]To set up isolated execution contexts for distinct teams, modern administrative utilities were used to construct groups and individual client profiles[cite: 306, 307]:

```bash
# Provisioning target group resources
sudo groupadd interns
sudo groupadd cyberteam

# Initializing distinct student profiles with custom parameters
sudo useradd -m -s /bin/bash student1
sudo useradd -m -s /bin/bash student2
sudo useradd -m -s /bin/bash student3

# Mapping student assignments to respective group configurations
sudo usermod -aG interns student1
sudo usermod -aG interns student2
sudo usermod -aG cyberteam student3
