 # 📁 Day 09: File Upload Vulnerabilities

## 🔍 Focus Area:
Today was all about one of the most **critical and impactful bug types** —  
**File Upload Vulnerabilities**, with a deep focus on how **unvalidated uploads** can lead to **Remote Code Execution (RCE)** 💀

This was a massive eye-opener — a simple image upload feature, if misconfigured, can turn into a full-blown entry point for attackers.

---

## ✅ What I Learned

### 📂 What are File Upload Vulnerabilities?
- Vulnerabilities that arise when a server **accepts uploaded files without proper validation**, allowing malicious files like `.php` or `.jsp` to slip through.

### 💥 Impact:
- **Complete server compromise** via uploaded shells
- **Stored XSS** through malicious scripts
- Bypassing filters and blacklists

### 🧠 Core Concepts Explored:
- How web servers handle **static file requests**
- MIME type spoofing and **Content-Type header manipulation**
- Blacklist vs. whitelist-based validation
- Uploading via **PUT requests**
- How some vulnerabilities can be exploited **even without code execution** (e.g., client-side JS injection or parser exploitation)

---

## 🧪 Labs Completed (PortSwigger – Apprentice)

- ✅ **Remote code execution via web shell upload**
- ✅ **Web shell upload via Content-Type restriction bypass**

Both were incredibly hands-on. The moment I got a shell uploaded and hit it in the browser — that "⚡️it works!" feeling was awesome.  
Changing the `Content-Type` header in Burp Repeater to sneak past weak checks gave me a better understanding of how easily defenses can be bypassed.

---

## 🛠️ Tools & Techniques Used

- 🔧 **Burp Suite Repeater**
  - Modified request headers like `Content-Type` and filename extensions
- 🧠 Learned how to use:
  - `.php.jpg`, `.php;.jpg`, `.php%00.jpg`
  - PUT method uploads
  - Spoofed file contents to trick servers
- 🗂️ Practiced static content access behavior using fake image uploads

---


## 🎯 Key Takeaway

> “File upload feels innocent… until you realize it’s the fastest path to a reverse shell.”  

<p>Learning how <b>tiny oversights in upload logic</b> can let attackers take over a server really showed me why this is considered a <b>high-severity, high-bounty</b> bug.</p>

---

## ⚠️ Struggles Faced

- Understanding **how MIME type checks work** internally took a bit of time.
- It was confusing at first how **some extensions are allowed**, but still get executed based on server-side misconfig.
- Tried experimenting with **blacklisting edge cases** (e.g., `.phP;.jpg`) and noticed how **some labs didn’t filter capitalized or obfuscated extensions**.

