# 🧭 Week 4: Recon in the Real World — From Scope to Subdomains

### 📌 Overview
This week, I began applying recon techniques in a real-world context by selecting live bug bounty programs on **HackerOne**. My focus was on practical reconnaissance — exploring the subdomain and URL discovery pipeline using standard tools. The process helped me understand how theory translates into practice, especially when balancing this journey alongside college academics.

---

### 🛠️ Tools & Techniques Used

- **Subdomain Enumeration**
  - [`subfinder`](https://github.com/projectdiscovery/subfinder): Passive subdomain collection.
  - [`amass`](https://github.com/owasp-amass/amass): Active enumeration — initially felt slow, but proved valuable after understanding its behavior better.
  - `sort` + `uniq`: For organizing and filtering subdomain lists.
  
- **URL Collection & Filtering**
  - [`gau`](https://github.com/lc/gau): Initially faced issues with response time, likely due to rate-limits or target configuration.
  - `curl`: Switched to manual URL scraping and HTTP probing.
  - `grep`: Used for extracting “spicy” URLs (e.g., parameters, admin paths).

---

### 🧠 Key Learnings

- **Tool Behavior Matters**: Initially thought Amass wasn't working — later realized it was running slow due to active scanning on a large-scope target.
- **Target Scope is Crucial**: Starting with a huge target was overwhelming. Switching to a small-scope program gave me focus and faster results.
- **Time-Intensive Process**: Recon is relatively simple in terms of commands, but the execution time and filtering process require patience and attention.
- **Real-World Application**: Understood the importance of organizing output files, chaining tools, and optimizing pipelines for efficient recon.

---

### 🔄 Reflection

This week was more about *depth than breadth*. Despite time constraints from academics, I gained **hands-on experience in end-to-end reconnaissance** — from identifying subdomains to extracting actionable URLs. I now understand what it *feels like* to deal with noisy data, slow tools, and the challenge of staying focused on a real target. This practical knowledge is a huge leap from just watching tutorials.

---

### 🧾 Files Created

- `subdomains.txt` — Final filtered list of all subdomains.
- `urls.txt` — Collected URLs from various sources (gau, curl).
- `filtered_spicy_urls.txt` — URLs containing potential attack surfaces (`?`, `admin`, `login`, etc.).

---

### 📅 Time Management

Although I couldn't dedicate as many hours due to college workload, I ensured that every recon step was **deliberate and documented**. This taught me how to make consistent progress even with limited time.

---

### 🔚 Closing Note

Recon is the first gatekeeper in bug bounty — and this week helped me step through it with confidence. Next, I look forward to mapping these recon results into actual vulnerabilities.
