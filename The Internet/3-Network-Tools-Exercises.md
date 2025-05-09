Here are some useful **network tools exercises** for practice, especially if you're learning about networking concepts or working with network troubleshooting and monitoring tools:

---

### **1. Ping Command**
**Objective:** Test connectivity between your machine and a remote server.

- Use the `ping` command to check the latency of popular websites like:
  ```bash
  ping google.com
  ping github.com
  ```
- **Exercise:** Analyze the response time and packet loss.  
  **Bonus:** Try pinging a non-existent domain (e.g., `ping nonexistentwebsite.com`) and observe the output.

---

### **2. Traceroute (tracert)**
**Objective:** Trace the route packets take to a destination.

- Run the `traceroute` (Linux/macOS) or `tracert` (Windows) command to analyze the hops a packet takes:
  ```bash
  traceroute google.com
  tracert google.com
  ```
- **Exercise:** Identify bottlenecks or high-latency nodes in the network path.

---

### **3. nslookup**
**Objective:** Query DNS records for a domain.

- Use `nslookup` to get information about a domain:
  ```bash
  nslookup google.com
  nslookup facebook.com
  ```
- **Exercise:** Find the IP address of your favorite website.  
  **Bonus:** Check both `A` (IPv4) and `AAAA` (IPv6) records.

---

### **4. Netstat**
**Objective:** View active connections and open ports.

- Run the following command to see network connections:
  ```bash
  netstat -an
  ```
- **Exercise:** Identify all `ESTABLISHED` connections on your system.  
  **Bonus:** Use `netstat` with additional flags to find listening ports.

---

### **5. Curl**
**Objective:** Fetch HTTP/HTTPS headers and content.

- Use `curl` to make a GET request to a website:
  ```bash
  curl -I https://example.com
  ```
- **Exercise:** Fetch and analyze HTTP response headers (like `Content-Type` and `Server`).  
  **Bonus:** Use `curl` to test a REST API endpoint.

---

### **6. Wireshark**
**Objective:** Capture and analyze network traffic.

- **Exercise:** Open Wireshark, capture traffic for a few seconds, and filter for HTTP traffic.
- **Task:** Analyze:
  - Source and destination IP addresses.
  - Protocols in use (e.g., TCP, UDP, HTTP).

---

### **7. IP Configuration**
**Objective:** View and modify your IP settings.

- Run `ipconfig` (Windows) or `ifconfig`/`ip` (Linux/macOS):
  ```bash
  ipconfig
  ifconfig
  ip addr show
  ```
- **Exercise:** Identify your local IP address, subnet mask, and default gateway.  
  **Bonus:** Try renewing your DHCP lease.

---

### **8. FTP/SSH**
**Objective:** Access a remote server.

- Use `ssh` to connect to a remote machine (if you have access):
  ```bash
  ssh user@remote_server_ip
  ```
- Use `ftp` to list files on a remote server:
  ```bash
  ftp ftp.gnu.org
  ```
- **Exercise:** Navigate through files and test basic commands like `ls`, `get`, and `put`.

---

### **9. Nmap**
**Objective:** Scan open ports and services.

- Run `nmap` to scan a local machine or remote server:
  ```bash
  nmap localhost
  nmap -sV google.com
  ```
- **Exercise:** Identify open ports and their associated services.  
  **Bonus:** Perform a ping sweep on your local network.

---

### **10. Speed Test**
**Objective:** Test your internet speed.

- Use `speedtest-cli` (install if necessary):
  ```bash
  speedtest
  ```
- **Exercise:** Compare speeds at different times of the day.

---

### **Advanced Tools:**
- **Netcat (nc):** Test open ports or create a simple chat server.
- **TCPdump:** Capture and analyze packets on the command line.
- **Pathping:** Combines `ping` and `traceroute` to measure latency and packet loss.

---
