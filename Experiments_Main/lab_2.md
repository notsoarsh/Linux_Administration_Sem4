# Experiment 2: Linux Manual Pages and Brace Expansion

## **Objective**  
Explore Linux manual pages (`man`), search for filesystem-related commands, and understand brace expansion for string generation.

---

## **PROBLEM STATEMENT**
View the gedit man page.
Use the man -k ext4 command to find the command to tune ext4 file-system parameters.
Brace expansion is used to generate discretionary strings of characters. Braces contain a comma-separated list of strings,
or a sequence expression. The result includes the text that precedes or follows the brace definition.
## **Commands and Concepts Used**

### 1. `man` (Manual Pages)  
- **Description**: Displays documentation for commands, utilities, and configuration files.  
- **Example**:  
  ```bash  
  man gedit
## **Approach**
Step 1: View the gedit Manual Page
Open the terminal.

Run man gedit to access the manual page for the gedit text editor.

Navigate the manual using arrow keys or search with / followed by a keyword (e.g., /syntax).

Step 2: Find ext4 Filesystem Tuning Command
Use man -k ext4 to search for commands related to the ext4 filesystem.

Identify tune2fs from the search results.

Run man tune2fs to read about its usage for adjusting ext4 parameters.

Step 3: Practice Brace Expansion
Generate strings with comma-separated lists:


echo {apple,banana,cherry}_fruit  # Output: apple_fruit banana_fruit cherry_fruit  
Create files using sequence expressions:


touch image_{01..05}.png  # Creates image_01.png, image_02.png, ..., image_05.png  
Combine prefixes/suffixes with brace expansion for complex patterns.



![1](https://github.com/user-attachments/assets/3d058b88-ead5-4273-936b-0a4c26a46f79)
![2](https://github.com/user-attachments/assets/198877d7-df45-4fa4-9bb0-4f0500170060)
![3](https://github.com/user-attachments/assets/89c54ddd-9ea3-451b-ad3b-59f5066e25a0)
![4](https://github.com/user-attachments/assets/a9a4f43d-c1d3-4deb-ba7a-31e97a6def30)
![5](https://github.com/user-attachments/assets/2b4a3640-ff61-4a88-aa6d-0136453e3a9b)
![6](https://github.com/user-attachments/assets/e45ce250-5938-4f3a-b5c7-21e8b5c092a5)


  
