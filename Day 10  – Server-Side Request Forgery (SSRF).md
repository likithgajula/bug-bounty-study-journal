# 🕵️‍♂️ Day 10: Server-Side Request Forgery (SSRF)

## 🧠 Focus:
Today, I deep-dived into one of the most **underrated but high-severity vulnerabilities** in web security —  
**Server-Side Request Forgery (SSRF)**.

I explored how attackers can abuse server-side functionality to send unauthorized requests — sometimes to internal services, cloud metadata, or even loop back to the server itself 🔄.

---

## 📘 What I Learned:

### 🚨 What is SSRF?
- **SSRF** happens when the server fetches a URL or resource provided by the user, and the attacker manipulates it to access unintended internal services.

### 💣 Impact:
- **Internal network scanning**
- Access to **AWS metadata endpoints** (169.254.169.254)
- Bypass IP-based access controls
- May lead to **RCE**, data leakage, or further pivoting

---

### 🔍 Key Topics Explored:

#### 🧩 Common SSRF Attacks
- Against the **server itself** (`http://127.0.0.1`)
- Against **back-end systems** (e.g., `http://internal-api`)

#### 🔓 Circumventing SSRF Defenses
- 🟥 Blacklist-based input filters: Bypassed using encoded input, redirect chains
- 🟩 Whitelist-based filters: Used open redirection to bounce through allowed URLs
- 🪞 SSRF via redirect logic

#### 🕵️‍♂️ Blind SSRF
- SSRF that **doesn’t return any visible response**
- Learned how to detect these using **out-of-band tools** like Burp Collaborator and DNS logging

#### 🔧 Finding Hidden Attack Surface
- URLs hidden in:
  - Request bodies
  - Headers like `Referer`
  - JSON/XML/yaml payloads

---

## 🧪 Labs Solved (PortSwigger – Apprentice)

- ✅ **Basic SSRF against the local server**
- ✅ **Basic SSRF against another back-end system**

These beginner-friendly labs were incredibly helpful in demonstrating the **core SSRF flow**.  
The moment I changed the URL parameter to `http://127.0.0.1` and got access to internal data — that was 💥.

---

## 🛠️ Tools & Techniques Used

- 🔁 **Burp Repeater** to manipulate URL-based parameters
- 🌐 Explored targeting:
  - `http://localhost`
  - `http://169.254.169.254` (cloud metadata endpoint)
- 🧠 Thought process: Looked for parameters like `?url=`, `?next=`, `?image=` — all SSRF-prone

---



## 💡 Key Takeaways

> “Just because the browser can’t reach it, doesn’t mean the **server** can’t.”  
> SSRF is all about **thinking like the server** — and that shift in mindset is critical for deeper exploitation.

---

## ⚠️ Struggles

- At first, it was hard to **mentally visualize** that the request is **sent by the server**, not the browser.
- Took a few tries to understand why some SSRF payloads don’t return any output (blind SSRF).
- Played around with different internal IP ranges and localhost shortcuts to see which are blocked or filtered.


