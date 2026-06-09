# Linux Task 01: Linux Environment Setup & Essential Commands

## Objective

The purpose of this task is to become familiar with the Linux operating system, terminal interface usage, directory navigation, and core file management utilities. Linux serves as a fundamental environment for Cyber Security professionals, System Administrators, and Ethical Hackers.

---

## 🖥️ Part A: Linux Installation & Verification

For this environment setup, **Kali Linux** was successfully deployed inside a virtual machine (VM) container.

### System Verification Screenshots

* [x] Desktop Environment initialized
![Desktop Environment](./Screenshots/Desktop.png)

* [x] Active Terminal window functional
![Active Terminal window](./Screenshots/Terminal.png)

* [x] Base system parameters verified
![Base system parameters verified](./Screenshots/SystemInfo.png)
---

## 🧭 Part B: Basic Navigation Commands

The execution metrics for foundational shell traversal commands inside the bash environment are detailed below:

* **`pwd` (Print Working Directory):**

  * **Purpose:** Displays the absolute directory path of the current shell focus.
  * **Output Example:** `/home/kali`

* **`ls` (List Storage Contents):**

  * **Purpose:** Lists non-hidden files and subdirectories located within the current working folder.

* **`ls -la` (List All Long Format):**

  * **Purpose:** Lists all system file elements in long-form details, including hidden configuration files (those prefixed with a dot `.`), along with permissions, file sizes, ownership information, and modification timestamps.

* **`cd` (Change Directory):**

  * **Purpose:** Changes the current shell context to a specified directory. Running it without parameters returns the user to the home directory (`~`).

* **`clear` (Reset Screen):**

  * **Purpose:** Clears previous terminal output from the visible screen, providing a clean workspace.

* **`history` (Command Log Review):**

  * **Purpose:** Displays a chronological list of previously executed commands in the current shell session.

* **`whoami` (Identity Verification):**

  * **Purpose:** Displays the username of the currently logged-in user.
  * **Output:** `kali`

* **`hostname` (Device Domain ID):**

  * **Purpose:** Displays the logical name assigned to the local device or virtual machine.
  * **Output:** `kali`

---

## 📁 Part C: Directory Management

Using the `mkdir` utility, the following directory hierarchy was created:

```text
Cyber Security_Lab/
├── Networking/
└── Linux/
    ├── Cyber Security/
    │   └── Ethical Hacking/
    └── Reports/
```
