# 🧩 Day 07: HTML Injection & CORS Misconfigurations


## 🔍 Focus Area:
Today's learning focused on two important but often overlooked vulnerabilities:  
- **HTML Injection**: Inserting raw HTML into a web page to manipulate its structure or appearance.  
- **CORS Misconfiguration**: How improperly configured CORS headers can expose sensitive data to untrusted origins.

---

## ✅ What I Learned

### 🧩 HTML Injection
- Learned how **HTML Injection** allows attackers to inject raw HTML tags like `<h1>`, `<a>`, and `<img>`.
- Practiced injecting these elements into vulnerable forms and observing how they altered the page content.
- Understood how it differs from XSS — **HTML Injection doesn't execute JavaScript**, but it can trick users, modify layouts, or deliver phishing payloads.

### 🌐 CORS Misconfiguration
- Understood the role of **CORS (Cross-Origin Resource Sharing)** and how it controls access between different origins.
- Learned why headers like:
  - `Access-Control-Allow-Origin: *`
  - `Access-Control-Allow-Credentials: true`  
  can be **dangerous if misused**.

---

## 📚 Learning Resources

- 🎥 **CORS Deep Explanation:**  
  [Complete CORS Guide – Rana Khalil](https://youtu.be/t5FBwq-kudw?si=_t-vNImHkm9--vWA)

- 🧪 **Lab Walkthrough:**  
  [CORS Misconfiguration Practical Video](https://youtu.be/ZK-h5xei07k?si=stuo1hdHAjnSGKmR)

---

## 🧪 Labs & Practice

- ✅ Solved the **CORS Misconfiguration Lab** on PortSwigger using Burp Suite and guidance from the video walkthrough.
- 🧠 Applied theoretical CORS knowledge in a practical exploitation scenario.

---

## 🛠️ Tools Used

- 🔍 **Burp Suite** – for modifying `Origin` headers and testing misconfigurations
- 🌐 **PortSwigger Labs** – for safe, realistic exploitation

---

## 🧠 Key Takeaways

> "Even the most secure-looking applications can fail if a single response header is misconfigured."

Learning CORS and HTML Injection helped me appreciate how **client-side behaviors and server-side controls** must align perfectly to ensure security.

---
## ⚠️ Struggles Faced

- Initially confused CORS with CSRF due to the similar “cross-origin” concept.
- Took time to fully understand the risk of combining wildcard origins (`*`) with `Access-Control-Allow-Credentials: true`.
- Needed multiple replays of the walkthrough video to understand the exploitation flow step-by-step.

---
