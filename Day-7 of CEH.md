<div align="center">
  <h1>Day - 7 of CEH</h1>
</div>

# OSINT & Reconnaissance

---

## 1. Censys
- **Purpose**: Alternative to Shodan for discovering internet-connected devices.
- **Censys GPT**:
  - Helps build and extract search filters.
  - Identifies devices/services in a specific region.
  <center>
  <img src="images/148.png" alt="steps for hacking" width="600">
</center>
- **Workflow**:
  - Select a filter (e.g., cameras in a country).
  - Copy the generated filter/query.
  - Paste it into the Censys search bar.
  <center>
  <img src="images/147.png" alt="steps for hacking" width="600">
</center>



###  //Censys Login Process//
---
### Step 1: Open Browser
- Open Firefox (or any browser)

### Step 2: Go to Censys Website
- Type the following URL in the address bar:
  https://search.censys.io

### Step 3: Click on Login
- On the top-right corner, click **Log In**

### Step 4: Choose Login Method
- You can log in using:
  - Email and password
  - Google account
  - GitHub account

### Step 5: Enter Credentials
- Enter your registered email and password
- Click **Log In**

### Step 6: Verify Email (If New User)
- Check your email inbox
- Click the verification link sent by Censys

### Step 7: Access Censys Dashboard
- After successful login, you will be redirected to the Censys dashboard
- You can now search for:
  - Hosts
  - IP addresses
  - Domains
  - Certificates

### Step 8: Start Searching
- Use the search bar to apply filters
- Example:
  services.http.response.status_code:200


---

## 2. Infoga (Email OSINT)
- **Purpose**: Collects publicly available email information related to a domain.
- **Source**: GitHub repository.
<center>
  <img src="images/153.png" alt="steps for hacking" width="600">
</center>
- **Basic Steps**:
  - Clone the repository.
  - Navigate to the Infoga directory.
  - View help options.
  - Run against a target domain.
- **Use Case**:
  - Finding emails indexed by search engines.

## Infoga Setup on Parrot OS (Complete Steps)

### Step 1: Open Firefox, search for Infoga GitHub, and copy the repository link
<center>
  <img src="images/154.png" alt="steps for hacking" width="600">
</center>
### Step 2: Clone Infoga from GitHub
- command: git clone https://github.com/m4ll0k/Infoga.git

<center>
  <img src="images/155.png" alt="steps for hacking" width="600">
</center>
### Step 3: Enter Infoga directory
- command: cd Infoga
<center>
  <img src="images/156.png" alt="steps for hacking" width="600">
</center>

### Step 4: Verify installation and view help menu
- command: python3 infoga.py --help
<center>
  <img src="images/157.png" alt="steps for hacking" width="600">
</center>

### Step 5: Run Infoga on a target domain
- command: python3 infoga.py -d example.com -s all
<center>
  <img src="images/158.png" alt="steps for hacking" width="600">
</center>

---

## 3. Search Engine Dorking
### General Rules
- Use quotes (`" "`) for exact phrase matching.
- Combine operators to narrow search results.

### Common Operators
- `site:` – Restricts results to a specific website  
  - Example: `site:example.com`
  <center>
  <img src="images/161.png" alt="steps for hacking" width="600">
</center>
- `inurl:` – Searches keywords in URLs  
  - Example: `inurl:login`
- `filetype:` – Searches for specific file types  
  - Example: `filetype:pdf`
  <center>
  <img src="images/162.png" alt="steps for hacking" width="600">
</center>

### Examples
- Academic sites: `site:.ac.in`, `site:.edu`
- Government sites: `site:.gov`, `site:.gov.in`
- Job listings: `site:company.com jobs`

> ⚠️ Use only for educational or authorized purposes.

---

## 4. Wayback Machine (archive.org)
- **Purpose**: View historical versions of websites.
<center>
  <img src="images/159.png" alt="steps for hacking" width="600">
</center>
- **Steps**:
  - Copy the website URL.
  - Paste it into archive.org.
  - Browse snapshots using the timeline.
  <center>
  <img src="images/160.png" alt="steps for hacking" width="600">
</center>

---

## 5. Subdomains
- **Definition**: A subdomain is part of a larger domain name.
- **Purpose**:
  - Organizes different sections of a website.

### Example
- https://photos.example.org
- `photos` → Subdomain (third-level domain)
- `example` → Domain name
- `.org` → Top-level domain (TLD)

---

## 6. Subdomain Enumeration Tools
### Sublist3r
- Discovers subdomains of a target domain.
- Installed via package manager.
- Displays discovered subdomains.
<center>
  <img src="images/166.png" alt="steps for hacking" width="600">
</center>
<center>
  <img src="images/167.png" alt="steps for hacking" width="600">
</center>
# Sublist3r Setup on Parrot OS 

 ### Step 1: Open Firefox, search for Sublist3r GitHub, and copy the repository link

 ### Step 2: Clone Sublist3r from GitHub
- Command: git clone https://github.com/aboul3la/Sublist3r.git

 ### Step 3: Enter Sublist3r directory
- Command: cd Sublist3r

### Step 5: Verify installation and view help menu
- Command: python3 sublist3r.py -h

### Step 6: Run Sublist3r on a target domain
- Command:python3 sublist3r.py -d example.com


### Netcraft
- Online tool for subdomain and hosting discovery.
<center>
  <img src="images/169.png" alt="steps for hacking" width="600">
</center>
<center>
  <img src="images/179.png" alt="steps for hacking" width="600">
</center>
---

## 7. OSINT Tools & Databases
- **Exploit Database**:
  - Public vulnerability reference database.
- **GHDB (Google Hacking Database)**:
  - Collection of advanced Google dorks.
  <center>
  <img src="images/164.png" alt="steps for hacking" width="600">
</center>

- **DorkGPT**:
  - AI-assisted dork/query generator.
  <center>
  <img src="images/163.png" alt="steps for hacking" width="600">
</center>


---

## 8. People Search Tools
### Spokeo
<center>
  <img src="images/171.png" alt="steps for hacking" width="600">
</center>
- Gathers public information about individuals.
- Mostly paid.
- Primarily works for U.S. citizens.
<center>
  <img src="images/172.png" alt="steps for hacking" width="600">
</center>
<center>
  <img src="images/173.png" alt="steps for hacking" width="600">
</center>

---

## 9. Command-Line Basics
- `pip` – Installs Python libraries.
- `apt` – Installs system packages on Debian-based systems.

---

## 10. GPT-based CLI Tools
### ShellGPT / TGPT
- Command-line tools using GPT models.
<center>
  <img src="images/174.png" alt="steps for hacking" width="600">
</center>
- Example use cases:
  - Mathematical calculations.
  - Finding public IP address.
  - Generating WHOIS or port-scan explanations (theoretical).
 <center>
  <img src="images/175.png" alt="steps for hacking" width="600">
</center>
pt is a command-line tool that lets you use ChatGPT directly from the Linux terminal (Parrot OS, Kali Linux, Ubuntu, etc.).

When you run:

**tgpt --help**
(or sometimes tgpt help)

it shows:

How to use the tgpt command

Available options and flags

Examples of common usage

In short, tgpt help explains how to use tgpt.
<center>
  <img src="images/176.png" alt="steps for hacking" width="600">
</center>


> ⚠️ Always follow ethical and legal guidelines. Perform scans or reconnaissance only on systems you own or have permission to test.

---