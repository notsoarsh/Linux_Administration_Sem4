# Experiment 5: Process Management and Software Handling in Linux

## **Objective**  
Learn to monitor and manage processes using `ps`, `top`, and `kill`, and perform software installation/updates/removal with `apt-get`.

---

## **Commands and Concepts Used**

### 1. **`ps` (Process Status)**  
   - **Description**: Displays snapshot of active processes.  
   - **Common Options**:  
     - `ps aux`: Lists all running processes with details (user, PID, CPU, memory, etc.).  
     - `ps -ef`: Shows full-format process list.  

### 2. **`top` (Process Monitor)**  
   - **Description**: Real-time dynamic view of system processes (CPU, memory, tasks).  
   - **Key Features**:  
     - Sort by CPU (`P`) or memory (`M`).  
     - Kill processes (`k` + PID).  
     - Exit with `q`.  

### 3. **`kill` (Process Termination)**  
   - **Description**: Sends signals to terminate or manage processes.  
   - **Common Signals**:  
     - `SIGTERM` (15): Graceful termination (default).  
     - `SIGKILL` (9): Forceful termination.  
   - **Usage**:  
     ```bash  
     kill -9 <PID>  # Force-kill a process  
     ```  

### 4. **`apt-get` (Package Management)**  
   - **Description**: Installs, updates, and removes Debian/Ubuntu packages.  
   - **Key Commands**:  
     - `sudo apt-get update`: Updates package lists.  
     - `sudo apt-get upgrade`: Upgrades installed packages.  
     - `sudo apt-get install <package>`: Installs a package.  
     - `sudo apt-get remove <package>`: Removes a package.  

---

## **Approach**  

### Step 1: Monitor Processes  
1. **List processes with `ps`**:  
   ```bash  
   ps aux | grep "firefox"  # Find Firefox processes  
Use top for real-time monitoring:


top  
Press P to sort by CPU usage.

Note the PID of a resource-heavy process.

### Step 2: Terminate Processes
Gracefully stop a process:


kill <PID>  # Replace <PID> with the target process ID  
Force-kill an unresponsive process:


kill -9 <PID>  
### Step 3: Install/Update Software with apt-get
Update package lists:


sudo apt-get update  
Upgrade installed packages:


sudo apt-get upgrade  
Install a package (e.g., htop):


sudo apt-get install htop  
Remove a package:


sudo apt-get remove htop  
Clean up unused dependencies:


sudo apt-get autoremove  
![7](https://github.com/user-attachments/assets/2845f35a-f091-492f-81b9-f2df182ae7fa)
![6](https://github.com/user-attachments/assets/35969a20-abbc-4838-9e30-fb924910131c)
![5](https://github.com/user-attachments/assets/9f0d9365-cde2-4069-868c-e7a01d7660e8)
![4](https://github.com/user-attachments/assets/c0adb981-284e-45e8-97bf-91f321fee8e2)
![3](https://github.com/user-attachments/assets/31fbb092-7a42-4a29-a725-d1b121a11da0)
![2](https://github.com/user-attachments/assets/a4b5c794-8a54-4858-ba47-7b9a9e65c8cc)
![1](https://github.com/user-attachments/assets/d10638ed-3ed1-4079-b853-a4d30ead86dd)
