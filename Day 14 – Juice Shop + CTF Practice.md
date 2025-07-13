# 📅 Day 14 – Juice Shop + CTF Practice  
 



## 🔥 Today's Goal
- **Practice realistic bug chains on OWASP Juice Shop.**
- **Attempt CTF-style challenges from PortSwigger Labs.**
- **Simulate a full attack chain.**
- **Solidify knowledge gained over the past 13 days.**

---

## 🛠 Tools & Resources Used
- **Burp Suite (Community)**
- **OWASP Juice Shop**
- **PortSwigger CTF Labs (Apprentice + Practitioner)**
- **Browser Dev Tools (Firefox/Chrome)**

---

## 🧪 Practical Tasks Completed

### ✅ **Juice Shop Practice (Realistic Bug Hunting Sim)**
I leveraged my existing knowledge from the past 13 days and applied it practically to the Juice Shop environment. I attempted to chain multiple vulnerabilities together to simulate realistic exploitation.

### 🔍 **Things Practiced:**
- XSS (Reflected, Stored, DOM)
- SQL Injection
- Broken Authentication / Login Logic
- HTML Injection
- CORS Misconfiguration
- IDOR (Insecure Direct Object Reference)
- File Upload Vulnerabilities
- SSRF
- Open Redirect
- CSRF
- Clickjacking


---

## 🏁 **CTF Labs (PortSwigger)**  
Revisited **Practitioner-Level Labs** in areas I struggled with before:

### 📌 Categories Focused:
- Broken Access Control
- File Upload
- Authentication Bypass
- SSRF / Open Redirect
- CSRF
- DOM XSS / Filter Bypass XSS

### 🧑‍💻 **Labs Attempted:**
- Reflected XSS with Tag Filtering
- SSRF with Whitelist Bypass
- File Upload + Web Shell (theoretical)
- Bypassing CSRF Token Validation
- Access Control Based on Referer Header

---

## 🔗 **Attack Chain Simulation (Juice Shop)**
Simulated a **full chain attack scenario**:
1. Recon endpoints using dev tools.
2. Bypassed login using weak logic / SQLi.
3. Leveraged IDOR to access another user's profile.
4. Uploaded a file with malicious intent (theoretically, in scope).
5. Used CSRF to manipulate user state.
6. Captured cookies using XSS.
7. Accessed admin functionality.

---

## 💡 Key Lessons Learned
- Practicing realistic attack chains helped **connect the dots** between isolated vulnerabilities.
- **Recon is everything**. Repeatedly analyzing endpoints via Burp/Dev tools gave deeper insights.
- Chaining vulnerabilities requires patience and careful observation.
- Some CTF labs truly mimic real-world applications; they’re invaluable.
- Juice Shop is still one of the best platforms for **end-to-end exploitation practice**.

---



## 📄 Writeups / Documentation
Created **CTF-style write-ups** for:
- 🐛 XSS Cookie Theft (Juice Shop)
- 🔐 SQL Injection Login Bypass (Juice Shop)
- 🔄 CSRF Exploitation (PortSwigger)

---

## 🔥 What's Next?
- ✅ Finalized my **14-Day Learning Journey.**
- ✅ Ready to transition towards **real-world recon** on platforms like HackerOne/Bugcrowd.
- ✅ Planning to continue learning **Advanced Recon, Automation, and Advanced Bugs**.

---

## 🚀 Progress So Far:
| Day   | Topic                                | Status   |
|-------|--------------------------------------|----------|
| Day 1 | Recon + Juice Shop Setup              | ✅ Done   |
| Day 2 | BurpSuite + XSS Basics                | ✅ Done   |
| Day 3 | XSS Lab Practice                      | ✅ Done   |
| Day 4 | Authentication Bypass + Logic Flaws   | ✅ Done   |
| Day 5 | SQL Injection                         | ✅ Done   |
| Day 6 | DOM XSS + PortSwigger Labs            | ✅ Done   |
| Day 7 | HTML Injection + CORS Misconfig       | ✅ Done   |
| Day 8 | Broken Access Control                 | ✅ Done   |
| Day 9 | File Upload Vulnerabilities           | ✅ Done   |
| Day 10| SSRF                                  | ✅ Done   |
| Day 11| Open Redirect + Clickjacking          | ✅ Done   |
| Day 12| CSRF                                  | ✅ Done   |
| Day 13| Deep Recon (Waybackurls, Arjun, etc.) | ✅ Done   |
| Day 14| Juice Shop + CTF Practice             | ✅ Done   |

---

## 📝 Struggles / Overcame
- Some attack chains required creativity in chaining bugs together — not always straightforward.
- Repetition in Burp Suite (Repeater, Intruder) helped me grasp **request manipulation better**.

---


