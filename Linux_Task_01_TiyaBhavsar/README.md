# Linux Task 01: Linux Environment Setup & Essential Commands

## Objective
[cite_start]The purpose of this task is to become familiar with the Linux operating system, terminal interface usage, directory navigation, and core file management utilities[cite: 181]. [cite_start]Linux serves as a fundamental environment for Cyber Security professionals, System Administrators, and Ethical Hackers[cite: 182, 288].

---

## 🖥️ Part A: Linux Installation & Verification
[cite_start]For this environment setup, **Kali Linux** was successfully deployed inside a virtual machine (VM) container[cite: 186]. 

### System Verification Screenshots
* [cite_start][x] Desktop Environment initialized [cite: 189]
* [cite_start][x] Active Terminal window functional [cite: 190]
* [cite_start][x] Base system parameters verified [cite: 191]

*(Your snapshot `network_config.png` containing terminal logs acts as verification evidence for this deployment.)*

---

## 🧭 Part B: Basic Navigation Commands
The execution metrics for foundational shell traversal commands inside the bash environment are detailed below[cite: 193]:

* [cite_start]**`pwd` (Print Working Directory):** * *Purpose:* Displays the absolute directory path of the current shell shell focus[cite: 194].
  * *Output Example:* `/home/kali`

* [cite_start]**`ls` (List Storage contents):** * *Purpose:* Lists non-hidden files and subdirectories located within the current working folder location[cite: 195].

* [cite_start]**`ls -la` (List All Long Format):** * *Purpose:* Lists all system file elements in long-form details, explicitly unmasking hidden systems configuration items (those prefixed with a dot `.`) alongside their permissions, size scales, ownership tags, and modification timestamps[cite: 196].

* [cite_start]**`cd` (Change Directory):** * *Purpose:* Transitions the current shell operational context to a specified directory location; running it with no parameters defaults back to the user's home path (`~`)[cite: 197].

* [cite_start]**`clear` (Reset Screen):** * *Purpose:* Flushes all previous command feedback rows out of visible range, offering a clean, unobstructed workspace[cite: 198].

* [cite_start]**`history` (Command Log Review):** * *Purpose:* Displays a chronologically ordered index of previously executed commands logged by the current active shell profile[cite: 199].

* [cite_start]**`whoami` (Identity Verification):** * *Purpose:* Prints the active user account context operating the current shell session[cite: 200].
  * [cite_start]*Output:* `kali` 

* [cite_start]**`hostname` (Device Domain ID):** * *Purpose:* Displays the unique logical name assigned to the local device or virtual machine on a network loop[cite: 201].
  * [cite_start]*Output:* `kali` [cite: 8, 241]

---

## 📁 Part C: Directory Management
[cite_start]Using systemic directory building configurations, the structural directory hierarchy was provisioned down the host pathway using the `mkdir` utility[cite: 207, 215]:

```text
Cyber Security_Lab/
├── Networking/
└── Linux/
    ├── Cyber Security/
    │   └── Ethical Hacking/
    └── Reports/
