# 🔍 Footprinting & Reconnaissance with Google Hacking Database - GHDB (W2-PM2)

![Cybersecurity](https://img.shields.io/badge/Track-Offensive_Security-red.svg)
![Category](https://img.shields.io/badge/Method-Passive_OSINT-orange.svg)
![Batch](https://img.shields.io/badge/Batch-B082_Networkwalks-green.svg)
![Platform](https://img.shields.io/badge/Source-Exploit--DB-blue.svg)

---

## 📌 Executive Summary
The Google Hacking Database (GHDB) is a curated framework of advanced search queries (Google Dorks) used to uncover sensitive information and misconfigured systems publicly indexed by search engines[cite: 3]. In this practical module, passive reconnaissance was conducted solely using Google Search and Exploit-DB GHDB dorks without launching active attacks or transmitting direct requests to target systems[cite: 3].

The objective of this assessment was to discover exposed IoT devices (live webcams) and publicly accessible open directory listings to document, analyze, and mitigate potential data leakage risks[cite: 3].

---

## ⚙️ Target & Environment Scope
* **Pentester / Author:** Faheem Ali Wattoo
* **Program:** Networkwalks Cybersecurity & Ethical Hacking Internship[cite: 6]
* **Batch Code:** B082-Networkwalks[cite: 6]
* **Resource Source:** Exploit-DB (Google Hacking Database)[cite: 3]
* **Testing Type:** 100% Passive Reconnaissance (Read-Only OSINT via Google Search)[cite: 3]

---

## 🧰 Reconnaissance Methodology
1. **GHDB Exploration:** Navigated through relevant vulnerability categories on `exploit-db.com/google-hacking-database`[cite: 3].
2. **Dork Extraction:** Extracted target-specific search operators (such as `intitle:`, `inurl:`, `site:`)[cite: 3].
3. **Live Search Verification:** Executed the selected dorks in Google Search and verified the returning exposed assets[cite: 3].
4. **Data Logging:** Systematically recorded all findings and open directory assets in structured tables[cite: 3].

---

## 🔬 Hands-on Technical Activities & Verification

### 🔹 Task 1: 10x Live Exposed Security Camera Streams
Utilized Google Dorks to discover unsecured, unauthenticated, or publicly exposed live webcams and security surveillance interfaces[cite: 3].

| No. | Target Link / Discovered Asset | Relevant Google Dork | Authentication / Exposure State |
| :---: | :--- | :--- | :---: |
| **01** | `https://www.skylinewebcams.com/en/webcam/italia/lazio/roma/piazza-di-spagna.html` | `inurl:webcam site:skylinewebcams.com inurl:roma` | Public Stream Portal[cite: 13] |
| **02** | `http://109.233.191.130:8080/` | `intitle:"webcamXP" inurl:8080` | Open / No Authentication[cite: 13] |
| **03** | `http://85.93.53.175:8080/home.html` | `intitle:"webcamXP 5" inurl:admin.html` | Open Web Interface[cite: 13] |
| **04** | `http://109.206.96.249:8080/` | `inurl:/multi.html intitle:webcam` | Open Multi-Camera View[cite: 13] |
| **05** | `https://www.lmc.edu/webcam.htm` | `intitle:"Webcam" inurl:WebCam.htm` | Educational Public WebCam[cite: 13] |
| **06** | `http://myfishcam.homedns.org:444/` | `intitle:"webcamxp" "Flash JPEG Stream"` | Unauthenticated Stream[cite: 13] |
| **07** | `http://75.149.26.30:1024/` | `intitle:"webcamxp" "Flash JPEG Stream"` | Direct IP Stream Port[cite: 13] |
| **08** | `http://139.64.168.120:8080/` | `intitle:"webcamxp 5" intext:"live stream"` | Live Unrestricted Stream[cite: 13] |
| **09** | `http://176.62.180.41:7777/192.168.1.21_554/snapshotfull.php` | `intitle:"ContaCam" "Snapshot Image"` | Unauthenticated Snapshot API[cite: 13] |
| **10** | `https://tuwebcam.towson.edu/popup.html` | `intitle:"NetCamSC*"` | Campus Public Camera Interface[cite: 13] |

#### Evidence - Discovered Live Camera Streams:
<img width="1360" height="1017" alt="Screenshot_cam_2" src="https://github.com/user-attachments/assets/d05851dc-6109-4efb-aea1-a961a1d9e079" />
<img width="1355" height="967" alt="Screenshot_cam_1" src="https://github.com/user-attachments/assets/60272ec9-e0f5-4211-a8f3-489cb6075d43" />

* **Security Insight:** Leaving surveillance cameras and webcams internet-facing without authentication leads to unauthorized live monitoring, privacy violations, and physical reconnaissance risks[cite: 3].

---

### 🔹 Task 2: 10x Open Directory Listings (Downloadable Mathematics PDFs)
Leveraged the `intitle:index of` operator family to identify open web server directories exposing downloadable academic and technical documents[cite: 3].

| No. | Target Link / Exposed Directory | Relevant Google Dork | Content Type |
| :---: | :--- | :--- | :---: |
| **01** | `https://education.giakonda.org.uk/Maths/Additional_Mathematics__Pure_and_Applied.pdf` | `intitle:index of "parent directory" mathematics pdf` | Complete Textbook PDF[cite: 13] |
| **02** | `https://www.jsoftware.com/books/pdf/aioj.pdf` | `intitle:index of "parent directory" mathematics pdf` | Applied Math E-Book[cite: 13] |
| **03** | `https://www.unm.edu/~megrad/Math/` | `intitle:index of "parent directory" mathematics pdf` | University Math Directory[cite: 13] |
| **04** | `https://www.netlib.org/math/docpdf/` | `intitle:index of "parent directory" mathematics pdf` | Documentation Repository[cite: 13] |
| **05** | `https://ochicken.net/library/Mathematics/math-hyperref.pdf` | `intitle:index of "parent directory" mathematics pdf` | Open Library Document[cite: 13] |
| **06** | `https://math.dartmouth.edu/~carlp/PDF/` | `intitle:index of "parent directory" mathematics pdf` | University Faculty Directory[cite: 13] |
| **07** | `https://maths.nuigalway.ie/~rquinlan/linearalgebra/` | `intitle:index of "parent directory" mathematics pdf` | Academic Course Material[cite: 13] |
| **08** | `https://www.learn-fo.com/FYUG%20mathematics%20solutions/?SD` | `intitle:index of "parent directory" mathematics pdf` | Educational Repository[cite: 13] |
| **09** | `https://pegaso.changeip.org/DOCS-TECH/Math/Engineering%20and%20Applied/` | `intitle:index of "parent directory" mathematics pdf` | Technical Documents Index[cite: 13] |
| **10** | `https://www.maths.dur.ac.uk/papers/2025/` | `intitle:index of "parent directory" mathematics pdf` | Research Papers Index[cite: 13] |

#### Evidence - Discovered Open Directories:
<img width="1796" height="1009" alt="Screenshot_ebook_2" src="https://github.com/user-attachments/assets/c0ca9c97-2993-4477-b7e0-92fcf7fae0fb" />
<img width="1008" height="1003" alt="Screenshot_ebook_1" src="https://github.com/user-attachments/assets/1e776c3b-b312-418a-8151-9375bbb74b8f" />

* **Security Insight:** Enabled directory indexing allows search engine crawlers to automatically index internal directories, exposing source files, backups, and intellectual property to the public[cite: 3].

---

## 📊 Risk Analysis & Security Impact

| # | Finding | Observation / Proof | Potential Security Risk | Risk Level |
| :---: | :--- | :--- | :--- | :---: |
| **01** | Unauthenticated Live Camera Streams | Publicly accessible webcamXP and ContaCam ports[cite: 13] | Unauthorized surveillance and physical reconnaissance[cite: 3] | `High` |
| **02** | Open Directory Indexing | Web servers exposing `/parent directory/` paths[cite: 13] | Unrestricted file enumeration and sensitive document leakage[cite: 3] | `Medium` |
| **03** | Search Bot Indexing of Private Assets | Misconfigured robots.txt allowing widespread crawling | Permanent caching of sensitive administrative and data endpoints[cite: 3] | `Medium` |

---

## 🛡️ Defensive Recommendations & Hardening

* **Disable Directory Browsing:** Enforce `Options -Indexes` in Apache configuration files (`httpd.conf` or `.htaccess`) to prevent exposure of directory structures[cite: 3].
* **Enforce Authentication on IoT Endpoints:** Implement strong authentication mechanisms and restrict internet accessibility on surveillance and IoT management interfaces[cite: 3].
* **Configure `robots.txt` & NoIndex Directives:** Restrict sensitive paths using `Disallow:` directives and apply `X-Robots-Tag: noindex` headers to prevent public search indexing[cite: 3].
* **Perform Regular GHDB Audits:** Conduct periodic Google Dork assessments against corporate assets to detect and resolve accidental public exposures proactively[cite: 3].

---

## 👨‍💻 Author / Pentester Details
* **Pentester Name:** Faheem Ali Wattoo
* **Program:** Networkwalks Cybersecurity & Ethical Hacking Internship[cite: 6]
* **Batch:** B082-Networkwalks[cite: 6]
* **Lead Instructor:** [Waqas Karim CCIE](https://www.linkedin.com/in/waqaskarim/)[cite: 6]
