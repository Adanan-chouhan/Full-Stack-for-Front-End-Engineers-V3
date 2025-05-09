### **DNS (Domain Name System)**  

**What is DNS?**  
DNS is like the **phonebook of the internet.** It converts human-readable names (like `google.com`) into machine-readable **IP addresses** (like `142.250.185.14`), so computers can locate the server hosting a website.  

---

**How does it work?**  
1. When you type `google.com` into a browser, your device asks the DNS server:  
   **"What is the IP address of this domain?"**  
2. The DNS server responds:  
   **"The IP address is `142.250.185.14`."**  
3. Your browser then uses the IP address to connect to Google’s server and load the website.

---

**Why is DNS important?**  
- Humans find it easier to remember **names** (like `amazon.com`), while computers need **IP addresses** to communicate.  
- DNS acts as a **translator** between human-friendly names and computer-friendly addresses.

---

**Example:**  
Imagine you want to call your friend but don’t know their phone number. Instead, you remember their name. DNS is like a **contact list** that helps you find the phone number when you provide the name.

---

### **URL (Uniform Resource Locator)**  

**What is a URL?**  
A URL is the **address of a specific resource on the internet.** While DNS resolves the domain name to an IP address, a URL tells the browser exactly where to find the specific resource, like a webpage or image.  

---

**Parts of a URL:**  
For example, in this URL:  
```
https://www.google.com/search?q=coding
```

1. **Protocol:** `https` – Specifies how to connect (secure or non-secure).  
2. **Domain Name:** `www.google.com` – The name of the website.  
3. **Path:** `/search` – Specifies the exact page or file location.  
4. **Query:** `q=coding` – Additional parameters (like search terms).  

---

**Example:**  
Think of visiting a friend’s house:  
- **URL:** The full address (e.g., "House No. 23, Blue Street, Jaipur").  
- **DNS:** Like looking up the house name in a phonebook to get the number.  

When you type a URL into a browser, it guides the browser to the specific page or resource.

---

### **Difference Between DNS and URL**  
| **DNS**               | **URL**                          |
|-----------------------|----------------------------------|
| Converts names to IP addresses. | Provides the complete address of a resource. |
| Acts as a translator. | Acts as a locator.              |
