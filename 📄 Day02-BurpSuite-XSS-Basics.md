# 🧠 Day 2 – Burp Suite Setup + Intro to XSS

## ✅ What I Did Today

Today I explored the **basics of Burp Suite** and gained foundational knowledge about **Cross-Site Scripting (XSS)** vulnerabilities. While I haven't mastered XSS yet, I now understand how these attacks are crafted and how Burp Suite plays a major role in intercepting and manipulating web traffic.

---

## 🔧 Activities Performed

- Installed and configured **Burp Suite Community Edition**
- Set up **interception** for traffic between my browser and **OWASP Juice Shop**
- Observed request/response behavior in Burp’s **HTTP history**
- Navigated through Juice Shop while inspecting GET and POST requests
- Began experimenting with simple **XSS payloads** like:
  ```html
  <script>alert(1)</script>
  ```
  in various search and input fields
##  🧱 Struggles & Errors Faced
### 🛑 1. Interception not working at first
**Problem:** Burp wasn’t intercepting any requests.<br><br>
**Causes & Fixes:**<br>
❌ Forgot to set browser proxy to 127.0.0.1:8080.<br>
✅ Set it in browser > Network Settings > Manual Proxy.<br>
❌ Firefox blocked localhost proxying.<br>
✅ In search bar, search for `aboutconfig` → set `network.proxy.allow_hijacking_localhost` to true.<br>

> 💡 Lesson: Always check browser proxy settings and trust Burp’s certificate for HTTPS interception to work.

### 🔍 2. Confused by XSS filters<br>
I tried injecting `<script>alert(1)</script>` into input fields, but didn’t see any pop-ups.<br>
Later realized some fields had basic input sanitization or my payload wasn’t being reflected.<br>
Still experimenting with different payloads and reflection points.<br>

> 💡 Lesson: XSS exploitation is not just about injecting scripts — context, reflection, and encoding all matter.

## 🛠️ Tools Used
|Tool|	Purpose|
|------|-------|
|Burp Suite	|Intercept and inspect HTTP traffic
|Juice Shop|	Vulnerable web app for XSS testing
|Firefox|	Configured to route traffic through Burp

### 📚 Key Takeaways
Burp Suite is an essential tool for intercepting, modifying, and replaying HTTP requests.<br>
Understanding how web applications reflect and sanitize input is key to exploiting XSS.<br>
Even when a payload doesn’t trigger an alert, it doesn’t mean the input is safe — deeper testing is needed.<br>
Getting comfortable with Burp is a **critical step in progressing** toward real-world bug hunting.<br>

### 📷 Screenshots
`Burp Suite Intercepting Juice Shop Traffic`
[![Burp Interception](images/day02-burp-interception.png)](images/day02-burp-interception.png)


