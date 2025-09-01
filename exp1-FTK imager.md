
# Experiment No. 1: Evidence Acquisition Using AccessData FTK Imager



---

## Description
Forensic Toolkit (FTK) is a Windows-based computer forensics software product by AccessData.  
The free FTK Imager tool can both acquire and analyze forensic evidence.  

It can acquire:
- **Volatile memory** (RAM)
- **Non-volatile memory** (Hard disk)

Two ways to use FTK Imager:
1. **Portable version** from USB/HDD — useful for live data acquisition when the evidence machine is ON.
2. **Installed on investigator’s laptop** — source disk mounted via **write blocker** to prevent modification.

---

## Acquiring Volatile Memory

<p align="center">
 
  <img src="https://github.com/user-attachments/assets/68577e22-8a1e-4534-bf62-9f2bae8b31d0" width="80%" />
</p>


Open **FTK Imager** and navigate to the **volatile memory (capture memory)** icon.

---

<p align="center">
 
  <img src="https://github.com/user-attachments/assets/f093c6f6-1c0f-40a5-a4ab-5a17c563a7cc" width="80%" />
</p>

  
Select the option to capture memory. You can include:
- **Pagefile.sys** — used when RAM is full, may contain valuable data.
- **AD1 file** — FTK image file format for later use.

---

<p align="center">

  <img src="https://github.com/user-attachments/assets/7c707552-ee1a-4c54-89d6-d88ea8965d4c" width="80%" />
</p>


Click **Capture Memory** to start the acquisition process.

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/d15ce4f0-bd77-45bb-832b-9d16fd9e372f" width="80%" />
</p>

 
After acquisition completes, the destination folder will contain the `.mem` file (volatile memory image).

---

## Acquiring Non-Volatile Memory (Disk Image)

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/8c12a7bc-50da-4db5-b179-429010bf9073" width="80%" />
</p>

 
Open FTK Imager and select **Create Disk Image**.

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/7d39281a-80b2-4cfa-ad3f-c65f150a6520" width="80%" />
</p>


Select the source to acquire:
- Physical drive
- Logical drive
- Image file
- Folder contents
- CD/DVD

---

<p align="center">
 
  <img src="https://github.com/user-attachments/assets/af170331-a96f-4de2-a549-dfa339245768" width="80%" />
</p>


Choose **Physical Drive** for full disk acquisition.

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/1e5ac5fe-c85e-4959-8548-ca9124f981d0" width="80%" />
</p>

  
Select the drive and click **Finish**.

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/e3953571-2436-404d-883d-0d4192f613f2" width="80%" />
</p>

  
Choose the image format:
- **Raw (dd)** — No headers, widely used.
- **SMART** — Linux bitstream format.
- **E01** — EnCase proprietary format with compression.
- **AFF** — Open format, not vendor-locked.

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/ab5dd338-cdbe-4dad-b4c9-6794594e504d" width="80%" />
</p>

 
Enter case details such as examiner name, notes, and date.

---

<p align="center">
 
  <img src="https://github.com/user-attachments/assets/644a6ddb-b78d-49d5-a3c3-f65a92360287" width="80%" />
</p>

  
Set:
- Destination path
- File name
- Image fragment size (`0` for single file)

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/9743e524-a795-40e5-9063-58af4c93f7bc" width="80%" />
</p>


Enable **Verify images after they are created** to ensure hash value integrity.

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/36e6fc93-833b-4f85-a5c9-ae258bb64340" width="80%" />
</p>

 
Click **Start** to begin acquisition.  
After completion, FTK Imager generates a report file with acquisition details and matched hash values.

---

## Conclusion
FTK Imager is a reliable tool for acquiring both volatile and non-volatile memory while ensuring evidence integrity through hashing and write blockers.



  

