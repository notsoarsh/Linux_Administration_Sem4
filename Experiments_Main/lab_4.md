# Experiment 4: Linux Permissions and umask Configuration

## **Objective**  
Create a directory with specific permissions, manage group access, and configure user umask settings to control default file/directory permissions.

---

## **Commands and Concepts Used**

### 1. **`mkdir`**  
   - **Description**: Creates directories.  
   - **Example**:  
     ```bash  
     sudo mkdir /home/consultants  
     ```  

### 2. **`chmod` (Symbolic Method)**  
   - **Description**: Modifies file/directory permissions using symbols (`u`, `g`, `o`, `+`, `-`).  
   - **Example**:  
     ```bash  
     sudo chmod g+w /home/consultants  
     ```  

### 3. **`chmod` (Octal Method)**  
   - **Description**: Sets permissions numerically (e.g., `755`, `770`).  
   - **Example**:  
     ```bash  
     sudo chmod 770 /home/consultants  
     ```  

### 4. **`usermod` / `groupadd`**  
   - **Assumption**: The `consultants` group and `operator1` user exist.  
   - **Group Assignment**:  
     ```bash  
     sudo groupadd consultants  # If group doesn't exist  
     sudo chgrp consultants /home/consultants  
     ```  

### 5. **`umask`**  
   - **Description**: Sets default permissions for new files/directories.  
   - **Syntax**:  
     ```bash  
     umask 007  # Prohibits "others" from accessing new files  
     ```  

---

## **Approach**  

### Step 1: Create Directory and Assign Group  
1. Create the directory:  
   ```bash  
   sudo mkdir /home/consultants  
Assign ownership to the consultants group:


sudo chgrp consultants /home/consultants  

### Step 2: Set Permissions
Add write permission for the group (symbolic method):


sudo chmod g+w /home/consultants  
Forbid access to "others" (octal method):


sudo chmod 770 /home/consultants  
Result: Permissions become drwxrwx--- (owner: rwx, group: rwx, others: ---).

### Step 3: Configure umask for operator1
Edit the operator1 user’s shell configuration file (e.g., .bashrc):


sudo su - operator1  
echo "umask 007" >> ~/.bashrc  # Append to .bashrc  
source ~/.bashrc               # Apply changes  
Verify the new umask:

umask  
Expected Output: 0007 (others get no permissions).

### Step 4: Test umask Settings
Create a test file and directory as operator1:

touch test_file.txt  
mkdir test_dir  
Check permissions:


ls -l  
Expected Output:

-rw-rw---- for test_file.txt

drwxrwx--- for test_dir


![4](https://github.com/user-attachments/assets/f60f36c5-c34f-4701-b9f2-64e9d59dd80a)
![3](https://github.com/user-attachments/assets/bee0f35e-6cb7-4876-b3d6-9de37c631f0d)
![2](https://github.com/user-attachments/assets/f0a175c0-8d81-4d78-ba06-3d323a217a6b)
![1](https://github.com/user-attachments/assets/8e9a11f3-65d1-4d29-b010-b3f39054fb0c)
