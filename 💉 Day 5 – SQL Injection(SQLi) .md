# 💉 Day 5 – SQL Injection (SQLi) Theory + Beginner Labs (PortSwigger)

## ✅ What I Did Today

Today, I focused on mastering the fundamentals of **SQL Injection (SQLi)** — one of the most powerful vulnerabilities in web security. I studied the **complete theory** of SQLi using PortSwigger’s learning materials and reinforced the concepts through **beginner labs**.

---

### 📚 Theory Covered (PortSwigger Academy)

- ✅ What is SQL Injection?  
- ✅ Impact of SQLi on application logic and data confidentiality  
- ✅ How to detect SQLi vulnerabilities:
  - In different parts of the query (WHERE, ORDER BY, etc.)
  - In different contexts (strings, numbers, logic)
- ✅ Real-world examples of SQLi exploitation:
  - Retrieving hidden data  
  - Subverting application logic  
  - Accessing data from other tables  
  - Blind SQLi  
  - Second-order SQLi  
- ✅ Database fingerprinting techniques:
  - Determining DB type and version  
  - Listing tables and columns  
- ✅ UNION attacks:
  - Finding number of columns  
  - Identifying data types  
  - Retrieving interesting data  
- ✅ Blind SQL Injection:
  - Triggering conditional responses  
  - Using errors to infer data  
  - Time-based techniques  
  - Out-of-band (OAST) attacks  
- ✅ Prevention strategies:
  - Parameterized queries  
  - Input validation  
  - Least privilege access to databases

---

### 🧪 Practical Labs Completed

| Lab Title | Status |
|-----------|--------|
| SQL injection in WHERE clause (retrieving hidden data) | ✅ Solved |
| SQL injection login bypass | ✅ Solved |

Both labs were from the **Apprentice track** on PortSwigger, and they helped reinforce the theory I learned today.

---

## 🎥 Videos I Watched

| Title | Link |
|-------|------|
| SQL Tutorial for Beginners | [Watch on YouTube](https://youtu.be/xiUTqnI6xk8?si=GTm-RAaafsQP5o4T) |
| hacking tutorial for beginners | [Watch on YouTube](https://youtu.be/2OPVViV-GQk?si=5W5EUHipih6BGm4Q0) |

---

## 🧪 Tools & Resources Used

| Tool / Resource                                  | Purpose                                                      |
|--------------------------------------------------|--------------------------------------------------------------|
| [PortSwigger SQLi Labs](https://portswigger.net/web-security/sql-injection) | Theory and hands-on SQLi training                             |
| Burp Suite Community Edition                     | Intercepting and modifying HTTP requests with SQL payloads    |
| SQLi Cheat Sheets                                | Quick reference for syntax and payloads                      |

---

## 💡 Key Takeaways

- SQLi can be simple yet devastating — even a basic injection can leak sensitive data or bypass login.
- Understanding query structure and context (e.g. string vs numeric) is critical for crafting payloads that work.
- Hints and solutions are valuable tools — they accelerate learning when you're just starting.
- I now feel confident in **identifying basic SQLi flaws**, and ready to move into more advanced attacks like UNION and blind SQL injection in the coming days.

---



## 🧱 Struggles & Errors Faced

- As it was my first exposure to SQLi exploitation, crafting payloads like `' OR 1=1--` and understanding how they alter query logic took a few tries.
- **I used the hints and solutions** provided by PortSwigger to solve both labs, which helped me grasp the attacker mindset and decode how SQL queries are built.
- UNION attacks, blind SQLi, and database enumeration still feel a bit abstract — I plan to revisit those when I practice the intermediate/advanced labs.

---

