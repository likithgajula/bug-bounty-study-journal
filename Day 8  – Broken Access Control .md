# 🔓 Day 08: Broken Access Control (IDOR & Privilege Escalation)

## 🔍 Focus Area:
Today’s journey focused on one of the **most critical OWASP Top 10 issues** —  
**Broken Access Control**, with a deep dive into:
- 🧩 **IDOR (Insecure Direct Object Reference)**
- 🚀 **Privilege Escalation**

The more I explored, the more I realized how simple misconfigurations can lead to **serious access flaws** — just by changing IDs or roles in the request.

---

## ✅ What I Learned

### 🔐 Broken Access Control
- Access control is more than login — it's **about enforcing what each user is allowed to do**.
- Practiced how apps fail to verify user permissions properly at the backend.

### 🧩 IDOR (Insecure Direct Object Reference)
- Manipulated object IDs like `user_id=123` → `user_id=124` in request parameters and saw how access was granted.
- Explored multiple request types (GET/POST) to exploit the IDOR vector.
- Saw real examples where simply **guessing another user’s ID** gave me access to their data.

### 🚀 Privilege Escalation
- Experimented with role-based parameters (`role=admin`, `isAdmin=true`) in Burp Suite Repeater.
- Identified unprotected admin endpoints and functions that responded without proper checks.

---

## 🔁 Hands-On Practice (Burp Suite)

This is where the real learning happened:
- Explored requests in **HTTP History** and replayed/modded them in **Repeater**.
- Modified HTTP **methods** (e.g., changing GET to POST and vice versa) to observe changes in server behavior.
- Tampered with **`Origin` and `Referer` headers** to see how backend validation reacted — both in labs and safe real-world targets.
- Observed how subtle tweaks could sometimes **bypass weak logic** in access checks.

---


## 🧪 Labs Completed

- ✅ **Insecure Direct Object Reference** (PortSwigger – Apprentice)
- ✅ **User ID controlled by request parameter with data leakage**
- ✅ Manually modified ID parameters and roles using Burp
- ✅ Practiced header tampering and endpoint testing in real web apps (responsibly)

---



## 🛠️ Tools Used

- 🧰 **Burp Suite**
  - Repeater: for modifying request methods, IDs, headers
  - Proxy & HTTP History: for analyzing intercepted traffic
- 🌐 **PortSwigger Labs** – for structured and safe practice

---

## 🧠 Key Takeaway

> “Real-world bugs often hide in plain sight — all it takes is a curious mind and the right request tampering.”

Today taught me how a simple tweak — whether an ID, a method, or a header — could open doors the developer *never intended to unlock*.

## ⚠️ Struggles Faced

- At first, it was hard to tell **if access was actually unauthorized** — not all responses made it obvious.
- Confused between **authentication and authorization logic**.

---
