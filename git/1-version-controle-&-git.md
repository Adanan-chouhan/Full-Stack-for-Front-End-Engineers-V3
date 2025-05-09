### 1. **Create a Git Repository**  
A Git repository is like a folder where all your code changes are tracked. To create one:

1. Create a folder for your project:  
   ```bash
   mkdir my-project
   cd my-project
   ```

2. Initialize the folder as a Git repository:  
   ```bash
   git init
   ```
   This creates a hidden `.git` folder inside your project that tracks all changes.

---

### 2. **Generate an SSH Key on Your Server (gh_key)**  
An SSH key is a secure way to connect to GitHub.

1. To generate an SSH key:  
   ```bash
   ssh-keygen -t ed25519 -C "your-email@example.com"
   ```
   
2. When prompted to name the key, type `gh_key` and press Enter:  
   ```plaintext
   Enter file in which to save the key (/home/user/.ssh/id_ed25519): /home/user/.ssh/gh_key
   ```

3. Set a passphrase (password) or leave it blank and press Enter.

---

### 3. **Add the SSH Key to GitHub**  
Now, let’s add the SSH key to GitHub:

1. Copy the public key:  
   ```bash
   cat ~/.ssh/gh_key.pub
   ```
   This will display your public key on the terminal. Copy it.

2. Go to GitHub:  
   - **Settings** → **SSH and GPG keys** → **New SSH Key**.
   - Give it a title (e.g., `My Server Key`) and paste the copied key into the key field. Click **Add SSH Key**.

---

### 4. **Ensure the New SSH Key Is Used**  
To ensure that GitHub uses this new `gh_key`:

1. Open the `~/.ssh/config` file (create it if it doesn’t exist):  
   ```bash
   nano ~/.ssh/config
   ```

2. Add the following configuration:  
   ```plaintext
   Host github
       HostName github.com
       User git
       IdentityFile ~/.ssh/gh_key
   ```
   This tells your system to use `gh_key` when connecting to GitHub.

3. Save and exit the file.

4. Test the connection to ensure the key is working:  
   ```bash
   ssh -T git@github.com
   ```
   If everything is set up correctly, you’ll see a message:  
   ```plaintext
   Hi username! You've successfully authenticated, but GitHub does not provide shell access.
   ```

---

### 5. **Add the Remote Repository**  
Now, link your local project to the remote repository on GitHub:

1. Create a new repository on GitHub (don’t initialize it with `README.md`).

2. Copy the repository’s SSH URL, and link it to your local repository:  
   ```bash
   git remote add origin git@github.com:username/repository.git
   ```
   Replace `username/repository.git` with your actual repository URL.

---

### 6. **Push the Local Repository to GitHub**  
Finally, push your local project to GitHub:

1. Stage your files:  
   ```bash
   git add .
   ```

2. Commit the changes:  
   ```bash
   git commit -m "My first commit"
   ```

3. Push the files to the GitHub repository:  
   ```bash
   git push origin main
   ```