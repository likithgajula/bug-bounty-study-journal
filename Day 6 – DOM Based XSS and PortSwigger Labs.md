# 🧠 Day 06 - DOM-Based XSS Deep Dive

## 🔍 Focus Area:
Today, I concentrated on **DOM-based Cross-Site Scripting (DOM XSS)** — a powerful client-side attack that doesn’t depend on server responses. I learned how attackers exploit insecure JavaScript functions to execute scripts in the browser.

---

## ✅ Labs Completed (PortSwigger)

| Lab Title                                                                                   | Status     |
|---------------------------------------------------------------------------------------------|------------|
| DOM XSS in `document.write` sink using `location.search`                                    | ✅ Solved  |
| DOM XSS in `innerHTML` sink using `location.search`                                         | ✅ Solved  |
| DOM XSS in jQuery anchor `href` attribute sink using `location.search` source               | ✅ Solved  |

---

## 📚 Learning Resources

To understand the **theory and hands-on exploitation**, I watched the following:

- 📘 [Conceptual: DOM XSS Explanation](https://youtu.be/biMtIOR8UAI?si=2XzRZeaTfIUtOwTf)
- 🧪 [Practical Lab Walkthrough #1](https://youtu.be/1Bt8mQyzFkI?si=C5t8tcxxuJqhTDy7)
- 🧪 [Practical Lab Walkthrough #2](https://youtu.be/5oeg4AqmFdo?si=m7rN5CTNBLu0GSw-)

These were  useful to bridge theory and practice.

---

## 🧠 Key Concepts Learned

- **DOM XSS** is caused when **user-controlled input (source)** is passed into insecure **DOM sinks** (like `document.write`, `innerHTML`, etc.) without sanitization.
- Understanding **how data flows from `location.search`** into various sinks is the key to exploitation.
- **jQuery** functions like `.attr()` can also be abused if developers aren't careful with dynamic values.

---


## 🛠️ Tools Used

- 🧩 **Browser Developer Tools** (Inspect, Console, and URL bar manipulation)
- 🌐 **PortSwigger Web Security Academy** for safe, guided labs

---

## ✍️ Reflection

Even though I didn’t solve many labs numerically today, I **gained deep conceptual clarity** around DOM-based XSS. These labs showed how XSS can occur entirely on the client side — and how powerful browser tools can be in debugging vulnerabilities.

DOM XSS is now less of a mystery — and more of a challenge I’m ready to tackle.

---
## ⚠️ Struggles Faced

- I was **initially confused between "sources" and "sinks"** — especially how `location.search` is interpreted and injected into HTML or JS contexts.
- Debugging payloads was challenging at first. I used **browser developer tools** extensively to observe the DOM behavior and trace the vulnerable code.
- The process was **frustrating but rewarding**, especially when the final payload worked!

---
