
<div align="center">
  <h1>Day - 6 of CEH</h1>
</div>

The objective of **Day–6** is to understand **Metadata**, its importance in **Ethical Hacking**, and to gain hands-on exposure to **information gathering (reconnaissance) tools** such as **ExifTool, Metagoofil, theHarvester, and Shodan**.  
This session focuses on how **hidden data inside files, documents, and online services** can unintentionally expose sensitive information and how ethical hackers analyze this data responsibly to improve security.

---

## 1. Metadata

**Metadata** refers to *data about data*. It is automatically generated information stored within digital files such as images, PDFs, Word documents, videos, and spreadsheets.
<center>
  <img src="images/What-is-Metadata.png" alt="steps for hacking" width="600">
</center>


### Examples of Metadata

- Author or creator name  
- File creation and modification dates  
- Software and operating system used  
- GPS coordinates (in images taken by mobile phones or cameras)  
- Device, camera, or smartphone model  

## Metadata Remover

A **Metadata Remover** is a tool or technique used to **remove hidden metadata information** from digital files such as images, PDFs, Word documents, and videos.  
Removing metadata helps protect **privacy, confidentiality, and security** by preventing unintended information disclosure.

<center>
  <img src="images/metadata remover.png" alt="steps for hacking" width="600">
</center>

---

### What Metadata Removers Do

Metadata removers are used to:

- Delete author and creator information  
- Remove GPS location data from images  
- Erase device or camera details  
- Clear software and system information  
- Sanitize documents before public sharing  

### Importance in Ethical Hacking

Metadata plays a crucial role during the **reconnaissance phase** of ethical hacking because it can unintentionally disclose sensitive organizational details.

Metadata analysis helps to:

- Identify employee names and usernames  
- Discover software versions and platforms in use  
- Reveal internal directory paths and file structures  
- Expose geographic location information  
- Assist in ethical social engineering assessments  

---

## 2. ExifTool

**ExifTool** is a powerful command-line utility used to read, write, and analyze metadata from various file formats including images, videos, PDFs, and documents.

### Basic ExifTool Command

```
exiftool image.jpg
```

<center>
  <img src="images/130.png" alt="steps for hacking" width="600">
</center>


### Information Extracted

- Camera or mobile device model  
- Date and time of image capture  
- GPS latitude and longitude  
- File size, format, and encoding details  

### Use Case

ExifTool is commonly used to analyze images downloaded from websites, emails, or social media platforms to identify **metadata leakage** that may reveal sensitive personal or organizational information.
<center>
  <img src="images/131.png" alt="steps for hacking" width="600">
</center>


---

## 3. gofile.io – Image Download Process

**gofile.io** is a free file-sharing platform that allows users to upload and download files without mandatory registration.

### Steps to Download an Image

1. Open a web browser and visit **gofile.io**  
2. Access the shared download link  
3. Select the required image file  
4. Click on **Download**  
5. Save the image to the local system  
6. Analyze the downloaded image using **ExifTool**


### Purpose

The downloaded images are analyzed to check for **metadata exposure**, such as GPS location, device details, and timestamps, which could pose privacy or security risks.

---

## 4. Metagoofil

**Metagoofil** is a Kali Linux–based reconnaissance tool used to extract metadata from **publicly available documents** belonging to a specific domain.

### Installing Metagoofil

```
sudo apt install metagoofil
```
<center>
  <img src="images/132.png" alt="steps for hacking" width="600">
</center>


### Help Command

```
sudo metagoofil --help
```
<center>
  <img src="images/144.png" alt="steps for hacking" width="600">
</center>



### Targeted Command Used

```
sudo metagoofil -d vignaniit.edu.in -l 10 -n 10 -t pdf,xls,xlsx -w

```
<center>
  <img src="images/145.png" alt="steps for hacking" width="600">
</center>


### Explanation

- `-d` → Specifies the target domain  
- `-l 10` → Limits the number of search engine results  
- `-n 10` → Number of files to download  
- `-t` → File types to search (pdf, xls, xlsx)  
- `-w` → Generates an HTML report  

### Information Collected

- Author and employee names  
- Usernames and email IDs  
- Software and application details  
- Internal file paths and document structure  

---
## Insecam

**:contentReference[oaicite:0]{index=0}** is a publicly accessible website that indexes **open and unsecured IP cameras** available on the internet.  
It is commonly referenced in **cyber security awareness and OSINT studies** to demonstrate the risks of misconfigured devices.

---

### Purpose of Insecam

Insecam is used for **educational and awareness purposes** to show how improperly secured cameras can expose live video feeds to anyone on the internet.

Its main goals are to:

- Highlight the importance of securing IoT and IP camera devices  
- Demonstrate real-world impacts of weak or default credentials  
- Promote cyber security awareness among users and organizations  

---

### Type of Devices Shown

The platform may list publicly exposed:

- Home surveillance cameras  
- Office and shop security cameras  
- Baby monitors  
- Traffic and public area cameras  

These devices are visible **only because they are misconfigured or left unsecured**.

---

### Security Risks Demonstrated
<center>
  <img src="images/135.png" alt="steps for hacking" width="600">
</center>
Insecam clearly shows the dangers of poor security practices, such as:

- Using default usernames and passwords  
- Not enabling authentication on IP cameras  
- Exposing cameras directly to the internet  
- Lack of firmware updates and security patches  

Such issues can lead to **privacy violations and unauthorized monitoring**.
<center>
  <img src="images/136.png" alt="steps for hacking" width="600">
</center>

---

### Importance in Ethical Hacking & OSINT

From an ethical hacking perspective, Insecam helps learners understand:

- How exposed IoT devices can be discovered through OSINT  
- The consequences of misconfiguration in real-world systems  
- Why device hardening and access control are critical  

It is mainly used in **defensive security learning**, not for exploitation.

---
<center>
  <img src="images/137.png" alt="steps for hacking" width="600">
</center>



## 5. theHarvester

**theHarvester** is an **Open-Source Intelligence (OSINT)** tool used for gathering publicly available information related to a domain.
<center>
  <img src="images/133.png" alt="steps for hacking" width="600">
</center>


### Usage

- Performs passive reconnaissance  
- Collects data without directly interacting with the target  
- Uses public sources such as search engines and databases  

### Collected Data

- Email addresses  
- Subdomains  
- IP addresses  
- Hostnames  

This information helps in understanding the **digital footprint** of an organization.

---

## 6. Shodan

**Shodan** is a specialized search engine designed to discover **Internet-connected devices and services**.
<center>
  <img src="images/138.png" alt="steps for hacking" width="600">
</center>
### Login Process

1. Visit **shodan.io**  
2. Click **Sign Up / Login**  
3. Register using an email address  
4. Log in to access advanced search filters  
<center>
  <img src="images/139.png" alt="steps for hacking" width="600">
</center>

### Search Filters Used

- `port:20` → Identifies FTP services  
- `country:IN` → Filters results from India  
<center>
  <img src="images/146.png" alt="steps for hacking" width="600">
</center>

- `apache` → Finds servers running Apache  
- `city:chennai` → Devices located in Chennai  
<center>
  <img src="images/140.png" alt="steps for hacking" width="600">
</center>

- `camera` → Internet-connected cameras  
<center>
  <img src="images/141.png" alt="steps for hacking" width="600">
</center>
## CP PLUS ORANGE – Camera Login Interface

The above image shows the **CP PLUS ORANGE IP Camera login interface**, which is used to access and manage live camera feeds and settings.

### Description

- The login screen requires a **username** and **password**
- Default user shown is **admin**
- Supports connection over **TCP protocol**
- Provides options such as **Login**, **Cancel**, and **Forgot password**
- Used for configuring and viewing surveillance cameras
<center>
  <img src="images/142.png" alt="steps for hacking" width="600">
</center>


### Purpose

Shodan helps ethical hackers and security teams to:

- Identify exposed services  
- Detect misconfigured systems  
- Discover vulnerable or unsecured devices  
<center>
  <img src="images/143.png" alt="steps for hacking" width="600">
</center>

---

## 7. Key Learnings (Day–6)

- Gained a clear understanding of **Metadata** and its security implications  
- Learned how metadata can unintentionally expose sensitive information  
- Practiced metadata extraction using **ExifTool**  
- Downloaded and analyzed files from **gofile.io**  
- Installed and executed **Metagoofil** to extract document metadata  
- Performed passive reconnaissance using **theHarvester**  
- Used **Shodan search filters** to identify exposed services and devices  
- Understood the importance of **ethical and legal boundaries** in information gathering  
