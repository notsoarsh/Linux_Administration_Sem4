# Experiment 7: File Ownership and Permissions Management

## **Objective**  
Learn to modify file/directory ownership with `chown` and adjust permissions with `chmod`, including common options and use cases.

---

## **Commands and Concepts Used**

### 1. **`chown` (Change Owner)**  
   - **Description**: Changes the owner and/or group of files/directories.  
   - **Common Options**:  
     - `-R`: Recursively apply changes to directories and their contents.  
     - `-v`: Verbose mode (displays actions performed).  
   - **Syntax**:  
     ```bash  
     chown [options] <user>:<group> <file/directory>  
     ```  

### 2. **`chmod` (Change Mode)**  
   - **Description**: Modifies file/directory permissions using symbolic or octal notation.  
   - **Common Options**:  
     - `-R`: Recursive permission changes.  
     - `-v`: Verbose output.  
   - **Permission Types**:  
     - **Symbolic**: `u` (user), `g` (group), `o` (others), `a` (all).  
     - **Operators**: `+` (add), `-` (remove), `=` (set).  
     - **Octal**: `0-7` (e.g., `755` = `rwxr-xr-x`).  

---

## **Approach**  

### Step 1: Create Test Files/Directories  
1. Create a sample file and directory:  
   ```bash  
   touch test_file.txt  
   mkdir test_directory  
### Step 2: Use chown
Change ownership of a file:


sudo chown operator1:consultants test_file.txt  
Verify with ls -l:


-rw-r--r-- 1 operator1 consultants 0 Aug 25 10:00 test_file.txt  
Recursively change ownership of a directory:

sudo chown -R operator1:consultants test_directory  
### Step 3: Use chmod
Symbolic Method:

Add execute permission for the owner:


chmod u+x test_file.txt  
Remove read permission for others:


chmod o-r test_file.txt  
Octal Method:

Set permissions to rwxr-x--- (750):

chmod 750 test_directory  
Recursively set rw-r--r-- (644) for all files in a directory:


chmod -R 644 test_directory  
### Step 4: Verify Changes
Check ownership and permissions:


ls -l test_file.txt  
ls -ld test_directory  
![6](https://github.com/user-attachments/assets/f9edc239-ce14-49c0-aac4-63c2d15047f1)
![5](https://github.com/user-attachments/assets/80d9c440-0c55-496f-b0be-ace6a3aaf80e)
![4](https://github.com/user-attachments/assets/6729a4e2-775e-4ea8-b1ff-bd3ebebb9cfa)
![3](https://github.com/user-attachments/assets/76b853c7-2743-43e5-a312-afe76939fb7f)
![2](https://github.com/user-attachments/assets/eaff38cf-26e0-4950-99b9-15540f427d46)
![1](https://github.com/user-attachments/assets/71b5640e-c9df-4a84-ba19-171ad20610a8)

