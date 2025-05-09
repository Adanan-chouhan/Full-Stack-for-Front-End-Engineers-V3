### **1. Virtual Server**  
A **virtual server** is a server running on shared physical hardware but behaves like an independent, dedicated server. It is created using virtualization technology, which divides a single physical server into multiple isolated virtual servers.  

---

#### **Types of Virtual Servers:**  
1. **VPS (Virtual Private Server):**  
   A portion of a shared physical server with dedicated resources like CPU, RAM, and storage.  
   **Example:** Hosting websites or deploying applications.

2. **Cloud Servers:**  
   Virtual servers hosted in the cloud, offering scalability and resource flexibility based on demand.

---

#### **Advantages of Virtual Servers:**  
- **Cost-Effective:** Cheaper than dedicated servers.  
- **Scalable:** Resources (like RAM and CPU) can be adjusted as needed.  
- **Secure and Isolated:** Each virtual server operates in its own environment, ensuring that one server's issues don't affect others.

---

### **2. PM2 (Process Manager 2)**  
**PM2** is a powerful process manager used to manage Node.js applications. It ensures your application runs smoothly, even if the server crashes or restarts.

---

#### **Key Features of PM2:**  
1. **Application Monitoring:** Provides real-time statistics like CPU and memory usage.  
2. **Auto-Restart:** Automatically restarts the app if it crashes.  
3. **Load Balancing:** Handles high traffic by running multiple app instances.  
4. **Log Management:** Helps view and manage application logs.

---

#### **How to Install and Use PM2:**  
1. **Install PM2:**  
   ```bash
   npm install -g pm2
   ```  

2. **Start Your App with PM2:**  
   ```bash
   pm2 start app.js
   ```  

3. **Check Running Apps:**  
   ```bash
   pm2 list
   ```  

4. **Stop an App:**  
   ```bash
   pm2 stop app
   ```  

---

### **Example Use Case:**  
- You have a Node.js app (`app.js`).  
- By running it with PM2:  
  - The app will automatically restart if it crashes.  
  - After a server reboot, PM2 ensures the app starts again automatically.  

---

### **Summary:**  
- **Virtual Server:** A server running on shared hardware but behaves like an independent server.  
- **PM2:** A tool to manage, monitor, and ensure the stability of Node.js applications.
