# 🧃 Day 1 – Recon Basics + Juice Shop Setup

## ✅ What I Did Today

### 🔹 Installed and Used Recon Tools
- Installed:
  - [`subfinder`](https://github.com/projectdiscovery/subfinder)
  - [`httpx`](https://github.com/projectdiscovery/httpx)
  - [`gau`](https://github.com/lc/gau)
- Practiced recon on a real program:
  ```bash
  subfinder -d github.com -o subs.txt
  httpx -l subs.txt -o live.txt
  gau github.com > urls.txt
### 🔹 Set Up Juice Shop Lab
Installed OWASP Juice Shop using Docker:

```bash
docker run -d -p 3000:3000 bkimminich/juice-shop
```
- Accessed it at `http://localhost:3000`
- Explored the UI and checked out the Score Board
## 🛠️ Tools Used Today
| Tool |	Purpose|
|------|------------|
|subfinder|	Subdomain enumeration|
|httpx	|Check which subdomains are alive|
|gau	|Discover archived endpoints|
|Docker|	To host Juice Shop lab locally|
## 💡 Key Takeaways
- Recon is the first and most important step in bug hunting
- Subdomain discovery and probing are passive and safe to try on public bounty programs
- `Juice Shop is a fully featured real-world vulnerable web app — perfect for daily practice

## 📷 Screenshots
`Installed Tools and Docker Versions`
[![Installed Tools and Docker Versions](images/day01-tools-version.png)](images/day01-tools-version.png)
`Juice Shop site`
[![Juice Shop Running in Docker](images/day01-juice-shop-running.png)](images/day01-juice-shop-running.png)


## 🧱 Struggles & Errors Faced Today

### 🐳 1. Docker Installation Failed — VM Disk Space Issue

- ❌ **Problem:** I got stuck trying to install Docker on my Kali Linux VM — the installation either failed silently or didn't complete.
- 🔍 **Root Cause:** My VM had **less than 25 GB** of allocated disk space, which is insufficient for Docker images like Juice Shop.
- 💡 **Fix:** Increased my virtual disk allocation to **50 GB**, then reinstalled Docker successfully.

> 🔁 **Lesson Learned:** If you're working with Docker and large labs, always make sure your Kali VM has **greater 25**. Docker needs enough room for images, containers, and system dependencies.

---
