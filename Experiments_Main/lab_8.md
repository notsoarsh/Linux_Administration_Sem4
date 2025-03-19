# Experiment 8: Shell Scripting and Redirection Operators

## **Objective**  
Create shell scripts to display system information, perform mathematical calculations, and use redirection operators to manage command outputs.

---

## **Commands and Concepts Used**

### 1. **Shell Scripting Basics**  
   - **Shebang Line**: `#!/bin/bash` to specify the interpreter.  
   - **Variables**: Store data for reuse (e.g., `sys_info=$(uname -a)`).  
   - **Command Substitution**: `$(command)` to capture output.  

### 2. **Mathematical Operations**  
   - **`expr`**: Evaluates integer arithmetic (e.g., `expr 5 + 3`).  
   - **`bc`**: Handles floating-point calculations (e.g., `echo "5.5 + 3.2" | bc`).  

### 3. **Redirection Operators**  
   - **`>`**: Redirects output to a file (overwrites).  
   - **`>>`**: Appends output to a file.  
   - **`2>`**: Redirects error messages.  

---

## **Approach**  

### Task 1: Script to Print System Information  
1. Create a script `system_info.sh`:  
   ```bash  
   #!/bin/bash  
   echo "===== System Information ====="  
   echo "OS: $(uname -s)"  
   echo "Hostname: $(hostname)"  
   echo "Kernel Version: $(uname -r)"  
   echo "Memory Usage: $(free -h | grep Mem | awk '{print $3 "/" $2}')"  
   echo "Date/Time: $(date)"  
Make it executable and run:


chmod +x system_info.sh  
./system_info.sh  
### Task 2: Script for Basic Mathematical Calculations
Create math_calculator.sh:


#!/bin/bash  
read -p "Enter first number: " num1  
read -p "Enter second number: " num2  

echo "Addition: $(expr $num1 + $num2)"  
echo "Subtraction: $(expr $num1 - $num2)"  
echo "Multiplication: $(expr $num1 \* $num2)"  
echo "Division (integer): $(expr $num1 / $num2)"  
echo "Division (floating): $(echo "scale=2; $num1 / $num2" | bc)"  
Execute the script:


chmod +x math_calculator.sh  
./math_calculator.sh  
### Task 3: Redirection Operators
Redirect Output to a File:

ls -l > file_list.txt  # Saves directory listing to file_list.txt  
Append Output:


echo "===== System Info =====" >> system_log.txt  
uname -a >> system_log.txt  
Redirect Errors:


grep "error" /var/log/syslog 2> error_log.txt  
![7](https://github.com/user-attachments/assets/9c67dd03-219b-4a82-a93b-08a01e2dab16)
![6](https://github.com/user-attachments/assets/a347aee4-b82c-437a-b634-71fc2353ef4c)
![5](https://github.com/user-attachments/assets/f62a7a92-b116-4478-afde-cf5a85fcb60e)
![4](https://github.com/user-attachments/assets/e819ebae-1bfd-4300-a097-4cf729c687db)
![3](https://github.com/user-attachments/assets/64bb7869-3348-49b7-8274-69cb31a01ac2)
![2](https://github.com/user-attachments/assets/177869fb-413c-481a-896c-c6ef2b62874c)
![1](https://github.com/user-attachments/assets/d19f0f22-4d2f-4700-b358-3ca36e630635)
