### **Setting Up Proxy Pass in Nginx: Step-by-Step Guide**

---

**What is Proxy Pass?**  
Proxy Pass allows Nginx to act as a **middleman**. When a client (like a browser) sends a request, Nginx forwards it to a backend server (e.g., Node.js, Python, or PHP).  
- **Example:**  
  A user requests `http://example.com`, and Nginx forwards it to `http://localhost:3000`, where the backend server is running.

---

### **Steps to Set Up Proxy Pass in Nginx**

#### **1. Install Nginx**  
Make sure Nginx is installed and running on your system:  
```bash
sudo apt update
sudo apt install nginx
sudo systemctl start nginx
```  

---

#### **2. Edit the Nginx Configuration File**  
To set up a proxy pass, edit the Nginx configuration file:  

1. Open the default configuration file:  
   ```bash
   sudo nano /etc/nginx/sites-available/default
   ```  

2. Add the following lines inside the `server` block:  
   ```nginx
   server {
       listen 80;
       server_name example.com;

       location / {
           proxy_pass http://localhost:3000;  # Address of your backend server
           proxy_set_header Host $host;
           proxy_set_header X-Real-IP $remote_addr;
           proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
       }
   }
   ```  

   - **proxy_pass:** This forwards requests to the backend server (e.g., `http://localhost:3000`).  
   - **proxy_set_header:** These headers ensure that the backend server receives information like the client's IP address and the original host.  

---

#### **3. Test the Nginx Configuration**  
Before reloading, check if the configuration is correct:  
```bash
sudo nginx -t
```  
- If you see "syntax is ok," the configuration is valid.

---

#### **4. Reload Nginx**  
Apply the changes by reloading Nginx:  
```bash
sudo systemctl reload nginx
```  

---

#### **5. Test Your Setup**  
1. Open your browser and visit `http://example.com` or your server's IP address.  
2. Nginx will forward the request to the backend server (e.g., Node.js app running on `http://localhost:3000`), and you will see the backend's response.  

---

### **Example Use Case**  
- Your backend server is running on `http://localhost:3000` (e.g., a Node.js app).  
- Nginx is configured to receive requests at `http://example.com` and forward them to the backend server.  
- The user accesses the backend service through Nginx, and the backend server’s IP remains hidden.

---

### **Summary**  
1. **Install Nginx:** `sudo apt install nginx`.  
2. **Edit Config File:** Add `proxy_pass` in `/etc/nginx/sites-available/default`.  
3. **Test Config:** Run `sudo nginx -t`.  
4. **Reload Nginx:** Apply changes with `sudo systemctl reload nginx`.  
5. **Test in Browser:** Open the website and confirm the backend is accessible.  
