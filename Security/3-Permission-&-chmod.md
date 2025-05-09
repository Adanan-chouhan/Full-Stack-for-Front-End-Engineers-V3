### **What are Permissions?**  
In Linux/Unix systems, every file and folder has a permission system that determines:  
1. **Who** (user/group/others) can access it.  
2. **How** (read, write, execute) they can interact with it.  

---

### **Types of Permissions**  
1. **Read (r):** Allows you to view the file's contents.  
2. **Write (w):** Allows you to edit or modify the file.  
3. **Execute (x):** Allows you to run the file, like a program or script.  

---

### **Permission Groups**  
Permissions are defined for three groups:  
1. **Owner (u):** The file’s owner or creator.  
2. **Group (g):** A group of users who can access the file.  
3. **Others (o):** All other users.

---

### **How to Check Permissions?**  
Command:  
```bash
ls -l
```

**Example Output:**  
```plaintext
-rwxr-xr-- 1 adnan users 1234 Nov 18 12:00 myfile
```

**Explanation:**  
- `-rwxr-xr--`: This represents permissions:  
  - `rwx` → **Owner**: Read, Write, Execute.  
  - `r-x` → **Group**: Read, Execute (no write).  
  - `r--` → **Others**: Read only.  
- `adnan`: The owner of the file.  
- `users`: The group associated with the file.  

---

### **What is chmod?**  
**chmod** is a command used to change the permissions of a file or folder.  

#### **Syntax:**  
```bash
chmod <permissions> <file-name>
```

---

### **Two Ways to Set Permissions**

#### **1. Symbolic Method**  
Use symbolic letters (`r`, `w`, `x`) to modify permissions.  

**Examples:**  
- Add write permission for the owner:  
  ```bash
  chmod u+w myfile
  ```
- Remove execute permission for the group:  
  ```bash
  chmod g-x myfile
  ```
- Remove all permissions for others:  
  ```bash
  chmod o-rwx myfile
  ```

---

#### **2. Numeric Method (Octal Notation)**  
Permissions are represented by numbers:  
- `r = 4`, `w = 2`, `x = 1`.  
- Add the numbers to calculate permissions:  
  - `rwx` = 4+2+1 = 7  
  - `rw-` = 4+2+0 = 6  
  - `r--` = 4+0+0 = 4  

**Example:**  
To set `rwx` for the owner, `r-x` for the group, and `r--` for others:  
```bash
chmod 754 myfile
```

**Breakdown:**  
- `7` → Owner: rwx (4+2+1).  
- `5` → Group: r-x (4+0+1).  
- `4` → Others: r-- (4+0+0).

---

### **Common chmod Commands**  
1. **Make a file read-only for everyone:**  
   ```bash
   chmod 444 myfile
   ```
2. **Give full access to everyone (rwx):**  
   ```bash
   chmod 777 myfile
   ```
3. **Owner gets full access, others can only read:**  
   ```bash
   chmod 744 myfile
   ```

---

### **Pro Tip:**  
- **Be cautious with 777:** It gives full access to everyone, which can be risky.  
- To restore full access for the owner only:  
  ```bash
  chmod 700 myfile
  ```