<div align="center">
  <h1>Day - 6 of CEH</h1>
</div>

## Part -2 : Footprinting & Reconnaissance
---

## 1. Metadata

### Definition
Metadata is data about data. It contains hidden information embedded inside:
- Images  
- PDFs  
- Word documents  
- Websites  

<center>
  <img src="Images/What-is-Metadata.png" alt="1" width="600">
</center>


### Metadata Can Contain
- File creation date  
- Last modified date  
- Author name  
- Software used  
- GPS location (Images)  
- Camera or device details  

### Risk
Improperly removed metadata can leak sensitive organizational or personal information.

---

## 2. ExifTool (Metadata Extraction)

### Tool Description
ExifTool is a command-line utility used to:
- Read metadata  
- Write metadata  
- Edit metadata  

### Command (Parrot OS)
exiftool <filename>

### Practical Steps
1. Download an image from a browser (Firefox preferred)  
2. Upload the image to gofile.io  
3. Copy the download link  
4. Download the image again  
5. Run ExifTool on the image  

<center>
  <img src="Images/130.png" alt="1" width="600">
</center>

<center>
  <img src="Images/131.png" alt="1" width="600">
</center>


### Information Extracted
- Camera model  
- Date and time  
- GPS coordinates  
- Image resolution  

---

## 3. Online Metadata Removal Tool

### Tool
metadata2go

### Purpose
- Removes unnecessary metadata  
- Protects user privacy  
- Reduces sensitive information leakage  

<center>
  <img src="Images/metadata remover.png" alt="1" width="600">
</center>


### Observation
After using metadata2go, the metadata extracted using ExifTool is significantly reduced.

---

## 4. Metagoofil

### Tool Description
Metagoofil extracts metadata from publicly available documents such as:
- PDF  
- DOCX  
- PPT  
- XLS  

### Installation
sudo apt install metagoofil

<center>
  <img src="Images/132.png" alt="1" width="600">
</center>


### Fix Broken Packages (If Required)
sudo apt --fix-broken install

### Help Menu
sudo metagoofil --help

<center>
  <img src="Images/144.png" alt="1" width="600">
</center>


### Information Gathered
- Usernames  
- Email IDs  
- File paths  
- Software versions  

## Implementation
sudo metagoofil -d <website name > -l <no. of search> -n <no.od download> -t <types of a file> -w

<center>
  <img src="Images/145.png" alt="1" width="600">
</center>


---

## 5. TheHarvester

### Tool Description
TheHarvester collects publicly available information such as:
- Email addresses  
- Subdomains  
- Hosts  
- Employee names  

### Command
sudo theHarvester -d <domain name> -b <source name>

<center>
  <img src="Images/133.png" alt="1" width="600">
</center>


### Data Sources
- Google  
- LinkedIn  
- Bing  
- Yahoo  
 
---

## 6. Web Camera Search Engines

### Examples
- webcamxp.com  
- iplivecam.com 
- Insecam 

<center>
  <img src="Images/134.png" alt="1" width="600">
</center>


### Purpose
- Demonstrates how attackers discover unsecured cameras  
- Highlights real-world IoT security risks  

<center>
  <img src="Images/135.png" alt="1" width="600">
</center>

<center>
  <img src="Images/136.png" alt="1" width="600">
</center>

<center>
  <img src="Images/137.png" alt="1" width="600">
</center>


### Important Note
Unauthorized access is illegal.  
Use only for educational and awareness purposes.

---

## 7. Shodan

### Website
https://www.shodan.io

### What is Shodan?
Shodan is a search engine for Internet-connected devices.  
It indexes:
- Servers  
- Routers  
- Webcams  
- IoT devices  
- Industrial systems (ICS/SCADA)  

---

## 7.1 Accessing Shodan
1. Open any browser  
2. Search for Shodan  
3. Click shodan.io  
4. Create an account  
5. Verify email  by using temp mail
6. Login  

<center>
  <img src="Images/138.png" alt="1" width="600">
</center>

<center>
  <img src="Images/139.png" alt="1" width="600">
</center>

---

## 8.2 Advanced Shodan Filters 
country:IN  
port:22  
org:BSNL  
os:Windows  
product:Apache  

Example:  
webcam country:IN

<center>
  <img src="Images/146.png" alt="1" width="600">
</center>

<center>
  <img src="Images/140.png" alt="1" width="600">
</center>

---

## 8.3 Information Extracted
- IP address  
- Open ports  
- Running services  
- Service banners  
- Organization name  
- Approximate location 

<center>
  <img src="Images/141.png" alt="1" width="600">
</center>

<center>
  <img src="Images/142.png" alt="1" width="600">
</center>

<center>
  <img src="Images/143.png" alt="1" width="600">
</center>

---
## Conclusion

In this session, we studied **metadata**, using tools like **ExifTool**, **Metagoofil**, **TheHarvester**, and exploring **Shodan** and web camera search engines, we understood how sensitive information can be exposed through publicly available sources. This lab highlights the importance of proper data handling, strong security configurations, and awareness of information leakage to protect systems from potential attacks.

---

