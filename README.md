# 🔍 Footprinting & Reconnaissance with Google Hacking Database - GHDB (W2-PM2)

![Cybersecurity](https://img.shields.io/badge/Track-Offensive_Security-red.svg)
![Category](https://img.shields.io/badge/Method-Passive_OSINT-orange.svg)
![Batch](https://img.shields.io/badge/Batch-B082_Networkwalks-green.svg)
![Platform](https://img.shields.io/badge/Source-Exploit--DB-blue.svg)

---

## 📌 Executive Summary
Google Hacking Database (GHDB) ek curated framework hai jo advanced search operators (Google Dorks) ke zariye publicly indexed sensitive information talash karta hai. Is practical module mein baghair kisi active attack ya target par direct request bheje sirf Google Search aur Exploit-DB GHDB dorks ke zariye passive reconnaissance perform ki gayi hai.

Is assessment ka maqsad exposed IoT devices (live webcams) aur misconfigured open directory listings ko uncover karna tha taake misconfigurations aur data leaks ko effectively document aur mitigate kiya ja sake.

---

## ⚙️ Target & Environment Scope
* **Pentester / Author:** Faheem Ali Wattoo
* **Program:** Networkwalks Cybersecurity & Ethical Hacking Internship
* **Batch Code:** B082-Networkwalks
* **Resource Source:** Exploit-DB (Google Hacking Database)
* **Testing Type:** 100% Passive Reconnaissance (Read-Only OSINT via Google)

---

## 🧰 Reconnaissance Methodology
1. **GHDB Exploration:** `exploit-db.com/google-hacking-database` par ja kar relevant categories browse ki gayin.
2. **Dork Extraction:** Target specific search operators (jaise `intitle:`, `inurl:`, `site:`) extract kiye gaye.
3. **Live Search Verification:** Dorks ko Google Search engine mein execute karke returning assets ko verify kiya gaya.
4. **Data Logging:** Findings aur open assets ko structured tables mein record kiya gaya.

---

## 🔬 Hands-on Technical Activities & Verification

### 🔹 Task 1: 10x Live Exposed Security Camera Streams
Google Dorks ka istemal karke unsecured, default authenticated, ya publicly exposed live webcams aur security stream portals discover kiye gaye.

| No. | Target Link / Discovered Asset | Relevant Google Dork | Authentication / Exposure State |
| :---: | :--- | :--- | :---: |
| **01** | `https://www.skylinewebcams.com/en/webcam/italia/lazio/roma/piazza-di-spagna.html` | `inurl:webcam site:skylinewebcams.com inurl:roma` | Public Stream Portal |
| **02** | `http://109.233.191.130:8080/` | `intitle:"webcamXP" inurl:8080` | Open / No Authentication |
| **03** | `http://85.93.53.175:8080/home.html` | `intitle:"webcamXP 5" inurl:admin.html` | Open Web Interface |
| **04** | `http://109.206.96.249:8080/` | `inurl:/multi.html intitle:webcam` | Open Multi-Camera View |
| **05** | `https://www.lmc.edu/webcam.htm` | `intitle:"Webcam" inurl:WebCam.htm` | Educational Public WebCam |
| **06** | `http://myfishcam.homedns.org:444/` | `intitle:"webcamxp" "Flash JPEG Stream"` | Unauthenticated Stream |
| **07** | `http://75.149.26.30:1024/` | `intitle:"webcamxp" "Flash JPEG Stream"` | Direct IP Stream Port |
| **08** | `http://139.64.168.120:8080/` | `intitle:"webcamxp 5" intext:"live stream"` | Live Unrestricted Stream |
| **09** | `http://176.62.180.41:7777/192.168.1.21_554/snapshotfull.php` | `intitle:"ContaCam" "Snapshot Image"` | Unauthenticated Snapshot API |
| **10** | `https://tuwebcam.towson.edu/popup.html` | `intitle:"NetCamSC*"` | Campus Public Camera Interface |

#### Evidence - Discovered Live Camera Streams:
<img width="1360" height="1017" alt="Screenshot_cam_2" src="https://github.com/user-attachments/assets/d05851dc-6109-4efb-aea1-a961a1d9e079" />
<img width="1355" height="967" alt="Screenshot_cam_1" src="https://github.com/user-attachments/assets/60272ec9-e0f5-4211-a8f3-489cb6075d43" />


* **Security Insight:** Surveillance devices aur webcams ko public internet par without authentication expose chorna physical privacy breach aur unwanted surveillance ka rasta kholta hai.

---

### 🔹 Task 2: 10x Open Directory Listings (Downloadable Mathematics PDFs)
`intitle:index of` dork family ka use karke academic aur technical open directory servers map kiye gaye jahan downloadable PDFs exposed theen.

| No. | Target Link / Exposed Directory | Relevant Google Dork | Content Type |
| :---: | :--- | :--- | :---: |
| **01** | `https://education.giakonda.org.uk/Maths/Additional_Mathematics__Pure_and_Applied.pdf` | `intitle:index of "parent directory" mathematics pdf` | Complete Textbook PDF |
| **02** | `https://www.jsoftware.com/books/pdf/aioj.pdf` | `intitle:index of "parent directory" mathematics pdf` | Applied Math E-Book |
| **03** | `https://www.unm.edu/~megrad/Math/` | `intitle:index of "parent directory" mathematics pdf` | University Math Directory |
| **04** | `https://www.netlib.org/math/docpdf/` | `intitle:index of "parent directory" mathematics pdf` | Documentation Repository |
| **05** | `https://ochicken.net/library/Mathematics/math-hyperref.pdf` | `intitle:index of "parent directory" mathematics pdf` | Open Library Document |
| **06** | `https://math.dartmouth.edu/~carlp/PDF/` | `intitle:index of "parent directory" mathematics pdf` | University Faculty Directory |
| **07** | `https://maths.nuigalway.ie/~rquinlan/linearalgebra/` | `intitle:index of "parent directory" mathematics pdf` | Academic Course Material |
| **08** | `https://www.learn-fo.com/FYUG%20mathematics%20solutions/?SD` | `intitle:index of "parent directory" mathematics pdf` | Educational Repository |
| **09** | `https://pegaso.changeip.org/DOCS-TECH/Math/Engineering%20and%20Applied/` | `intitle:index of "parent directory" mathematics pdf` | Technical Documents Index |
| **10** | `https://www.maths.dur.ac.uk/papers/2025/` | `intitle:index of "parent directory" mathematics pdf` | Research Papers Index |

#### Evidence - Discovered Open Directories:
<img width="1796" height="1009" alt="Screenshot_ebook_2" src="https://github.com/user-attachments/assets/c0ca9c97-2993-4477-b7e0-92fcf7fae0fb" />
<img width="1008" height="1003" alt="Screenshot_ebook_1" src="https://github.com/user-attachments/assets/1e776c3b-b312-418a-8151-9375bbb74b8f" />


* **Security Insight:** Web servers par directory indexing enable hone ki waja se internal files, backup zips, aur sensitive source files Google crawlers ke zariye publicly index ho jati hain.

---

## 📊 Risk Analysis & Security Impact

| # | Finding | Observation / Proof | Potential Security Risk | Risk Level |
| :---: | :--- | :--- | :--- | :---: |
| **01** | Unauthenticated Live Camera Streams | webcamXP & ContaCam ports open publicly | Unauthorized live monitoring & physical reconnaissance | `High` |
| **02** | Open Directory Indexing | Web servers exposing `/parent directory/` trees | Internal file enumeration & intellectual property leakage | `Medium` |
| **03** | Google Bot Indexing of Private Assets | Misconfigured robots.txt allowing full crawling | Permanent caching of sensitive endpoints in Google index | `Medium` |

---

## 🛡️ Defensive Recommendations & Hardening

* **Disable Directory Browsing:** Apache web servers mein `httpd.conf` ya `.htaccess` ke andar `Options -Indexes` enforce karein taake folder tree expose na ho.
* **Enforce Strong Authentication on IoT:** Kisi bhi camera ya surveillance feed ko public facing bananay se pehle multi-factor ya strong password authentication implement karein.
* **Configure `robots.txt` & NoIndex Meta Tags:** Sensitive directories par `Disallow:` aur header level par `X-Robots-Tag: noindex` apply karein taake search engines unhein index na karein.
* **Regular GHDB Self-Audits:** Security teams ko apni company ke domains par regular basis par Google Dorks run karke accidental data leaks verify karne chahiyein.

---

## 👨‍💻 Author / Pentester Details
* **Pentester Name:** Faheem Ali Wattoo
* **Program:** Networkwalks Cybersecurity & Ethical Hacking Internship
* **Batch:** B082 Networkwalks
* **Lead Instructor:** [Waqas Karim CCIE](https://www.linkedin.com/in/waqaskarim/)
