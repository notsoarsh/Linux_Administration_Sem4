# Experiment 3: Text File Editing with Vim and Nano

## **Objective**  
Edit the `editing_final_lab.txt` file using **Vim** and **nano**, leverage a shell variable, and perform precise text manipulation in Vim’s visual mode.

---

## **Commands and Concepts Used**

### 1. **Text Editors**  
   - **`nano`**: Simple terminal-based text editor with intuitive controls.  
   - **`vim`**: Advanced modal editor with features like visual mode for block editing.  

### 2. **Shell Variable**  
   - **Description**: Store the filename in a variable for reusable reference.  
   - **Example**:  
     ```bash  
     lab_file="editing_final_lab.txt"  
     ```  

### 3. **Vim Visual Mode**  
   - **Description**: Allows selection of text blocks for editing.  
   - **Commands**:  
     - Enter visual block mode: `Ctrl+V` (or `V` for line-wise selection).  
     - Delete selected text: `d`.  
     - Save and exit: `:wq`.  

---

## **Approach**  

### Step 1: Set the Shell Variable  
1. Define the filename in the terminal:  
   ```bash  
   lab_file="editing_final_lab.txt"  

### Step 2: Edit with Nano
Open the file in nano:


nano $lab_file  
Make basic edits (e.g., add/remove text) using nano’s interface.

Save changes: Ctrl+O, then exit: Ctrl+X.

### Step 3: Edit with Vim (Advanced)
Open the file in vim:



vim $lab_file  
Enter Visual Block Mode:

Navigate to the first line, first column.

Press Ctrl+V to start visual block selection.

Delete Last 7 Characters of the First Column:

Move the cursor 7 characters to the right (e.g., press l 7 times).

Press d to delete the selected block.

Result: Only the first 4 characters of the first column remain.

Save and exit:

Press Esc, then type :wq and press Enter.

![3](https://github.com/user-attachments/assets/8bdcda22-aff4-45d6-992f-0bb1719835b7)
![2](https://github.com/user-attachments/assets/3124acd1-e3d6-4b0e-9f14-62172f782379)
![1](https://github.com/user-attachments/assets/c4acac95-4f47-4cc6-877b-85651bd56003)
