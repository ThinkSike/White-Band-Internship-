# Linux Task 03: Process Management, System Monitoring & Basic Shell Scripting

## Objective
The purpose of this task is to master Linux process management utilities, evaluate system resources, control background service behaviors, and design automation shell scripts. These core competencies are fundamental for Security Administrators, Systems Engineers, and SOC Analysts.

---

## 🖥️ Part A: Process Monitoring

### 1. Fundamental Definitions
* **What is a Process?** A process is an active instance of a running program executing inside system memory. It is managed dynamically by the Linux kernel and consists of allocated memory spaces, system registers, security credentials, and a set of instructions executed by the CPU.
* **What is a PID?** A **Process ID (PID)** is a unique numeric integer assigned by the Linux kernel to each active process. It serves as a distinct handle to monitor, adjust permissions, prioritize, or terminate individual processing routines.

### 2. Live Resource Profiling Answers
* **Which process is consuming the most CPU?** *(Note: Check your active `top`/`htop` layout view and list the top offender here, typically `Xorg`, `gnome-shell`, or a running web browser).*
* **Which process is consuming the most Memory?** *(Note: Look closely at the `%MEM` column metrics in your terminal screenshot and supply the process label here).*

### Verification Screenshots
![System Process Top Observers Output](./screenshots/part_a_process_monitor.png)

---

## ⚙️ Part B: Process Management

### 1. Execution Telemetry Log
To evaluate process lifecycle signals, a lingering session was intentionally started and managed using background utilities:

* **PID Found via Search:** `4128` *(Example value, update with your exact terminal discovery)*
* **Command Sequence Applied:**
  ```bash
  # Initialize the process in an active shell session
  sleep 300 &
  
  # Discover and filter process footprint variables
  ps aux | grep sleep
  
  # Terminate using standard signal catch options (SIGTERM)
  kill 4128
  
  # Force immediate termination if unresponsive (SIGKILL)
  kill -9 4128
