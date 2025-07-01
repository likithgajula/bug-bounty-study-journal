# 💉 Day 3 – XSS Lab Practice (Reflected, Stored, DOM) + Burp Repeater

## ✅ What I Did Today

Today was all about **diving deep into XSS** vulnerabilities and understanding how they actually work in both ideal lab environments and real-world simulations.

I explored and completed hands-on labs on:

### 📘 PortSwigger Web Security Academy:
- ✅ Reflected XSS
- ✅ Stored XSS
- ✅ DOM-Based XSS

After understanding the concepts and exploiting them in a clean lab setup, I moved to **OWASP Juice Shop** to practice the same techniques on a more realistic application with noisy inputs, UI elements, and real-world structures.

To support the testing process, I also practiced using **Burp Suite's Repeater** — a tool that allowed me to modify and replay HTTP requests to test different XSS payloads efficiently.

---

## 🧪 Tools & Resources Used

| Tool/Resource | Purpose |
|---------------|---------|
| [PortSwigger Labs](https://portswigger.net/web-security/cross-site-scripting) | Conceptual learning and hands-on labs for XSS |
| OWASP Juice Shop | Realistic XSS practice in a vulnerable web app |
| [Burp Repeater Video](https://youtu.be/-6uPHcLj4oU?si=5L6EHvmTkJlQTy1F) | Guided walkthrough of Repeater tool in Burp |
| Burp Suite Community Edition | Intercepting, modifying, and testing web requests |

---
## 💡 Key Takeaways

- **XSS is contextual** — it's not about `alert(1)` but **where** and **how** you inject.
- DOM XSS is tricky — you must understand JS execution flows and inspect the DOM.
- **Burp Repeater = essential** for iterating payloads quickly and analyzing behaviors.
- PortSwigger teaches **clean theory**; Juice Shop delivers **dirty realism**—both matter.

---

## 🧱 Struggles & How I Overcame Them

### 😵‍💫 1. DOM-Based XSS Confusion
- I wasn’t seeing any payloads reflected in the server response.
- I later learned that DOM XSS doesn’t show in the HTTP response — it’s purely handled by JavaScript on the client side.
- 🔍 Fix: Inspected the DOM and used browser DevTools to trace how input was handled.

---

### 🔄 2. Burp Repeater Workflow Was Intimidating
- At first, I wasn’t sure how to send requests to Repeater or what to modify.
- 💡 Watched [this excellent video tutorial](https://youtu.be/-6uPHcLj4oU?si=5L6EHvmTkJlQTy1F) which clarified how to use Burp Repeater to test multiple payloads quickly.
- ✅ Eventually became confident editing parameters and analyzing responses.

---

### 💢 3. XSS Payloads Not Triggering
- Several times my XSS scripts like `<script>alert(1)</script>` didn’t work.
- 🧩 Cause: Input was either being sanitized or not reflected in the HTML output.
- ✅ Fix: Started inspecting where input landed in the page (HTML, attribute, JS context) and adapted payloads accordingly:
  ```html
  <img src=x onerror=alert(1)>
  <svg/onload=alert(1)>
