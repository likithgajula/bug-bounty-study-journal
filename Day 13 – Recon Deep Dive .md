# 📘 Day 13 – Recon Deep Dive: WaybackURLs + Parameter Mining

Today I explored some of the most *underrated but powerful recon techniques* that bug bounty hunters rely on : 
 <p> <b>🔄archived URL extraction</b>. -Wayback URLs </p>
 <p> <b> 🔍parameter mining</b>  - using tools like Arjun, ParamSpider, and Burp Suite’s Param Mine </p>

---

## 🔨 Tools Explored and Setup

### 1️⃣ `waybackurls` – Archived Endpoint Extraction
- **What I learned**: How Wayback Machine archives can be leveraged to find long-forgotten but still accessible endpoints.
- **Tool Setup**: Installed and tested `waybackurls`
- 🎥 **Demo video followed**: [Tool Tutorial – `waybackurls`](https://youtu.be/-zsYi0_xWbo?si=_OZYnrrva8iqz12Q)  
- 📚 **Concept video**: [Wayback Machine for Recon](https://youtu.be/ts1tu1BiSuY?si=bheFU-TP_Y7xUuO9)
- 📸 *Screenshot added in the repo!*

---

### 2️⃣ `ParamSpider`, `Arjun`, `Burp Param Miner` – Parameter Discovery Suite

These tools help in identifying hidden parameters that may lead to sensitive access or edge-case vulnerabilities.

---

## 🕵️‍♂️ ParamSpider

- **What it does**: Scrapes parameter names from JS files, URLs, and archives.
- **Installation Struggle**: Faced the common `externally-managed-environment` error. Resolved it by using:
 ```bash
  pip install -r requirements.txt --break-system-packages
```
- **Exact commands I used:** (directly copy and paste it into the terminal)
```bash
git clone https://github.com/devanshbatham/ParamSpider.git
cd ParamSpider
pip3 install -r requirements.txt
pip install -r requirements.txt --break-system-packages
```
**Run Check:**

```bash
python3 paramspider.py -d example.com
```
✅ Successfully ran it and included a screenshot in my journal!
[🎥 Video Guide – ParamSpider](https://youtu.be/ouEUEitRUfg?si=FKRJ_h_0IMeLbMnE)
### ⚙️ Arjun
**What it does:** Actively probes endpoints with a smart wordlist to discover hidden parameters.
<p><b>Workflow followed:</b></p>
<p>1.Created a local Flask server:</p>

```python 
from flask import Flask
app = Flask(__name__)

@app.route('/')
def home():
    return "A local server is running using Flask."
    
if __name__ == '__main__':
    app.run(host='127.0.0.1', port=5000)
```
 2.Then ran Arjun against it:
```bash
arjun -u http://127.0.0.1:5000/
```
**Struggle:** Burp Suite wasn't able to intercept the GET requests Arjun sent to my local server.
  ✅ But when I switched to testing it on external targets —   *everything worked fine!*
[🎥 Arjun Tool Demo](https://youtu.be/wRPxbz_Ht3k?si=iP7bVm2LZXcyxtWg)
### Burp Suite – Param Miner Extension 🧪
- Installed Param Miner from Burp BApp Store
- Used it to discover hidden parameters via:
- Header guessing (e.g., X-Original-URL)
- URL path & param brute forcing
- Simple and intuitive to use directly from Burp’s context menu → Guess Parameters
 [Param Miner Tool Demo](https://youtu.be/IYk7-xvOMOo?si=5BJcx6MP2qZbp_w2)
💡 Learned that Burp’s Param Miner is great for edge cases that ParamSpider/Arjun might miss

---
**✅Summary**


| Tool        | Purpose                              | Outcome                       |
| ----------- | ------------------------------------ | ----------------------------- |
| Waybackurls | Archived endpoints discovery         | ✅ Practiced + documented      |
| ParamSpider | Fast parameter scraping from URLs    | ✅ Installed + tested          |
| Arjun       | GET param fuzzing (dynamic analysis) | ✅ Practiced on local & remote |
| Param Miner | Hidden param discovery via Burp      | ✅ Explored inside Burp Suite  |
### ⚠️ Struggles Overcome
✅ Bypassed environment restrictions during ParamSpider installation.
✅ Learned how some tools behave differently on local vs. public targets.
✅ Solidified understanding of the parameter fuzzing logic used by Arjun and similar tools.
### 📸 Screenshots
✅ waybackurls demo result
✅ paramspider, arjun, and other tools installed successfully
(Uploaded in the repo's /images/ folder)










