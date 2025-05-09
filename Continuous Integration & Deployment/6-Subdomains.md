A **subdomain** is a part of a parent domain (main domain) used to organize different sections or services of a website. Subdomains help logically separate content, features, or services, such as blogs, stores, or support systems, under the same main domain.

---

### **Structure of a Subdomain**
The structure of a subdomain looks like this:  
```
subdomain.maindomain.com
```

Here:  
- **`subdomain`**: The name of the subdomain (e.g., `blog`, `support`, `shop`).  
- **`maindomain`**: The main domain name (e.g., `example.com`).  
- **`.com`**: The Top-Level Domain (TLD), or domain extension.  

#### Examples:
- **Main Domain**: `example.com`  
- **Subdomains**:  
  - `blog.example.com` → For blogging purposes.  
  - `shop.example.com` → For an e-commerce section.  
  - `support.example.com` → For customer support.

---

### **Why Use Subdomains?**
1. **Manage Different Services:**  
   A company might use subdomains to organize its services under one domain:  
   - `blog.example.com` → Blog section.  
   - `store.example.com` → Online store.  
   - `forum.example.com` → Community forum.  

2. **For Testing and Development:**  
   - Subdomains are useful for creating testing environments like `test.example.com` or `dev.example.com`.  
   - They allow development and testing without affecting the live website.

3. **Localization (Regional Content):**  
   - Subdomains can serve region-specific content:  
     - `us.example.com` → For U.S. users.  
     - `in.example.com` → For Indian users.  

4. **SEO Optimization:**  
   - Subdomains like `blog.example.com` help in SEO by organizing content into distinct categories.

---

### **How to Create a Subdomain?**
1. **Access the Domain Control Panel (DNS Settings):**  
   - Go to your domain registrar's DNS settings.

2. **Add a Subdomain:**  
   - Enter the subdomain name (e.g., `blog`, `shop`).  
   - Set the target server's IP address or CNAME record.

3. **Configure the Web Server:**  
   - Use a web server like Nginx or Apache to configure the subdomain. Example Nginx configuration:  
     ```nginx
     server {
         listen 80;
         server_name blog.example.com;
         root /var/www/blog;
         index index.html;
     }
     ```

---

### **Difference Between Subdomain and Subdirectory**
- **Subdomain:** `blog.example.com`  
- **Subdirectory:** `example.com/blog`  

#### **Comparison:**
| **Feature**         | **Subdomain**          | **Subdirectory**         |
|----------------------|------------------------|--------------------------|
| **SEO Impact**       | Treated as a separate entity | Part of the same website  |
| **Configuration**    | Requires DNS changes  | Simpler, uses same domain |
| **Use Case**         | For separate services or regions | For sections within the same service |

---

### **Examples in Real Life:**
1. **Google:**
   - **Mail:** `mail.google.com`  
   - **Drive:** `drive.google.com`  
   - **Docs:** `docs.google.com`  

2. **Amazon:**
   - **Shopping:** `www.amazon.com`  
   - **AWS:** `aws.amazon.com`  

---

### **Conclusion**
Subdomains are highly useful for dividing a website into multiple parts, each with its own purpose or audience. They are particularly helpful for SEO, testing environments, localization, and managing distinct services under a single main domain.