# Experiment 6: User Account Management in Linux

## **Objective**  
Create and manage user accounts (`operator1`, `operator2`, `operator3`), set passwords, modify user metadata, and remove users using Linux commands.

---

## **Commands and Concepts Used**

### 1. **`useradd`**  
   - **Description**: Creates new user accounts.  
   - **Example**:  
     ```bash  
     sudo useradd operator1  
     ```  

### 2. **`passwd`**  
   - **Description**: Sets or updates user passwords.  
   - **Example**:  
     ```bash  
     sudo passwd operator1  
     ```  

### 3. **`usermod`**  
   - **Description**: Modifies user account properties (e.g., comments).  
   - **Example**:  
     ```bash  
     sudo usermod -c "Primary Operator" operator1  
     ```  

### 4. **`userdel`**  
   - **Description**: Deletes user accounts.  
   - **Example**:  
     ```bash  
     sudo userdel operator3  
     ```  

### 5. **`id` / `getent`**  
   - **Description**: Verifies user existence in the system.  
   - **Example**:  
     ```bash  
     id operator1  
     getent passwd operator2  
     ```  

---

## **Approach**  

### Step 1: Create Users and Set Passwords  
1. **Create `operator1`**:  
   ```bash  
   sudo useradd operator1  
Set password for operator1:


sudo passwd operator1  
Enter and confirm the password when prompted.

Repeat for operator2 and operator3:


sudo useradd operator2  
sudo passwd operator2  

sudo useradd operator3  
sudo passwd operator3  
### Step 2: Verify User Creation
Check if users exist:


id operator1      # Verify UID/GID for operator1  
getent passwd operator2  # Confirm operator2's entry in /etc/passwd  
### Step 3: Update Comment for operator1
Modify the user comment (metadata):


sudo usermod -c "Primary System Operator" operator1  
Verify the update:


grep operator1 /etc/passwd  
Output Example:
operator1:x:1001:1001:Primary System Operator:/home/operator1:/bin/sh

### Step 4: Remove operator3
Delete the user account:


sudo userdel operator3  
Confirm removal:


id operator3  # Should show "no such user" 
![1](https://github.com/user-attachments/assets/fa373c5c-af98-419b-b292-5ec63d0df254)
