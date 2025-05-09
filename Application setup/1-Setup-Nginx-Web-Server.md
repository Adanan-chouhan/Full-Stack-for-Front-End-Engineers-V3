### **What is Nginx?**  
Nginx (pronounced **"engine-x"**) is a popular and fast **web server** used to run websites and applications. It is capable of:  
- Serving static content like HTML, CSS, and JavaScript files.  
- Acting as a **reverse proxy** to handle backend communication.  
- Balancing traffic across multiple servers (**load balancing**).  

Nginx is widely used to make websites faster, handle high traffic efficiently, and secure backend servers.

---

### **How to Set Up Nginx?**  
Follow these steps to install and configure Nginx on a Linux-based system (e.g., Ubuntu):

---

#### **Step 1: Update Your System**  
Before installing anything, update your system to ensure all packages are up-to-date:  
```bash
sudo apt update
sudo apt upgrade
```  
- **Why?** This ensures that your system's tools and libraries are the latest versions.

---

#### **Step 2: Install Nginx**  
Install Nginx by running the following command:  
```bash
sudo apt install nginx
```  
- **Why?** This command downloads and installs Nginx on your system.

---

#### **Step 3: Start the Nginx Service**  
Once installed, start the Nginx service:  
```bash
sudo systemctl start nginx
```  
- **Why?** This command starts the Nginx server, enabling it to handle web requests.

---

#### **Step 4: Test in a Browser**  
Open your browser and type `http://localhost` or your server's IP address.  
- If you see a "Welcome to Nginx" page, the installation was successful.

---

#### **Step 5: Allow Nginx in the Firewall (Optional)**  
If your system has a firewall enabled, allow Nginx traffic:  
```bash
sudo ufw allow 'Nginx HTTP'
```  
- **Why?** This ensures that incoming web requests are not blocked by the firewall.

---

#### **Step 6: Configure Nginx**  
To customize your website settings, edit the Nginx configuration file:  
```bash
sudo nano /etc/nginx/sites-available/default
```  
- Here, you can set your domain name, port, and custom directory.  

After making changes, reload Nginx:  
```bash
sudo systemctl reload nginx
```  

---

#### **Step 7: Upload Website Files**  
Place your website files (HTML, CSS, JS) in Nginx's root directory:  
```bash
/var/www/html/
```  
- This is where Nginx serves your website content from.

---

### **Example Use Case**  
1. Create a simple `index.html` file for your website.  
2. Place it in `/var/www/html/`.  
3. Open `http://localhost` in a browser to view your website.  

---

### **Summary**  
1. **Update your system:** `sudo apt update && sudo apt upgrade`.  
2. **Install Nginx:** `sudo apt install nginx`.  
3. **Start the service:** `sudo systemctl start nginx`.  
4. **Test in a browser:** Open `http://localhost`.  
5. **Edit configurations:** Modify `/etc/nginx/sites-available/default` as needed.  
6. **Upload your website files:** Place them in `/var/www/html/`.  

