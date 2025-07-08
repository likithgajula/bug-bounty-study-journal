# 🕳️ Day 11 – Open Redirects + Clickjacking

### ✅ What I Explored Today

Today was about diving into **two tricky web vulnerabilities**:  
**Open Redirects** and **Clickjacking** — both often overlooked but still very real in modern applications.

---

### 🔀 Open Redirects
I understood how attackers can trick users into being redirected to malicious websites using vulnerable redirect parameters (like `?next=`, `?url=`, etc.).

🔍 Helpful resource:  
[🎥 Open Redirect Vulnerability Explained](https://youtu.be/4Jk_I-cw4WE?si=nvQpAo5M8-MUaspm)

---

### 🖼️ Clickjacking
Learned how an attacker can "trick-click" users by hiding malicious elements inside transparent iframes. Explored how **CSRF** tokens and frame-busting scripts help defend against this.

#### 🔬 Covered concepts:
- What is Clickjacking?
- Constructing basic attacks (using **Clickbandit** tool)
- Clickjacking + DOM XSS attack chain
- Prefilled form injection via URL
- Frame busting scripts
- Preventive headers:
  - `X-Frame-Options`
  - `Content-Security-Policy (CSP)`

---

### 🧪 Labs Covered – PortSwigger (Apprentice Level)
- ✅ Basic Clickjacking with CSRF token protection  
- ✅ Clickjacking with form input data prefilled from a URL parameter  
- ✅ Clickjacking with a frame buster script  

---

### 🛠️ Tools/Methods Used:
- 🔗 Tested redirect parameters in demo URLs  
- 💻 Used browser dev tools to inspect frame and headers  
- 🧪 Followed attack structures using Clickbandit-like behavior  

---

### 📌 Takeaway

While these bugs don’t always give direct access like XSS or SQLi, they **open doors** to phishing, token stealing, and user manipulation. It was a great lesson in subtle yet powerful vulnerabilities.

---

### 😵‍💫 My Struggles Today

- I came in with **only HTML knowledge**, which made building the clickjacking PoCs harder than expected.
- Since **CSS** plays a crucial role in styling and layering the attack, I felt stuck and had to do extra Googling.
- Learned the importance of knowing at least **basic CSS** (opacity, positioning, z-index, etc.) — I’ll be revisiting CSS soon just to be able to exploit and test these better!

