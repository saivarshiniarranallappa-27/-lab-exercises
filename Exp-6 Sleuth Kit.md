#  *Experiment No. 06 — Digital Forensic Analysis using Sleuth Kit (TSK)*

##  Aim
To perform *digital forensic analysis* on a disk image using the *Sleuth Kit (TSK)* by examining file systems, recovering deleted files, analyzing metadata, and preserving evidence for investigation.

---

##  *Step 1: Installing Sleuth Kit*

1. *Download the Tool:*  
   - Head over to the official Sleuth Kit page or use this link:  
      [Download Sleuth Kit](https://drive.google.com/drive/u/1/folders/1ilSFY7Tqn2L7AjQGhq8yJ8kixc_xTU-v)  
   - Choose the latest stable *Windows-compatible* version.

2. *Installation Process:*  
   - Run the installer and follow the setup wizard .  
   - Once done, TSK will be ready to use on your system!

---



##  *Step 2: Acquire the Disk Image*

Before analysis, a *forensic disk image* (a perfect bit-by-bit copy) of the device is needed.

1. *Create Disk Image:*  
   - Use tools like *FTK Imager*  or **dd** to create an exact copy.  
   - Save it in a TSK-supported format: .dd, .raw, .img, or .E01.

2. *Sample Evidence Files:*  
   - For this lab, download the following from the provided link:  
      4Dell Latitude CPi.E01  
      4Dell Latitude CPi.E02

---




##  *Step 3: Mounting the Disk Image (Optional)*

Mounting lets you access the disk image as if it were a normal drive.

- Use *OSFMount*  to mount the image in *read-only mode*.  
-  Note: This is optional but helps when browsing the file system.

---

## *Step 4: File System Analysis with TSK*

Now let’s dive into Sleuth Kit tools to inspect the file system.

### Navigate to the TSK Directory

bash
cd "C:\Program Files (x86)\sleuthkit-4.14.0-win32\bin"

  
<img width="1552" height="338" alt="1 1" src="https://github.com/user-attachments/assets/17e6fb2e-c02f-4bc1-9b52-83f90fba27d2" />



---

###  Identify File System Type



 
<img width="1464" height="908" alt="2 1" src="https://github.com/user-attachments/assets/0e665adb-d1ff-4fc8-a989-15e51713bb7e" />


 Displays key details about the file system type and structure.

---

### View Partition Layout

<img width="1641" height="286" alt="3 1" src="https://github.com/user-attachments/assets/40ede90f-d59b-4326-b953-1279c697bd17" />

  



 Lists all partitions and their respective start/end addresses.

---








###  List Files and Directories


  
<img width="869" height="830" alt="4 1" src="https://github.com/user-attachments/assets/8a468658-87c0-456f-8f65-8aa1cb77b4c9" />


 Recursively lists files and folders with their inode details.

---

###  Recover Deleted Files

<img width="735" height="338" alt="6 1" src="https://github.com/user-attachments/assets/018f9323-a01a-4bf8-ace2-26611759d289" />

 


 Recovers a deleted or existing file by its inode number.

---

## *Step 5: Metadata Analysis*

To uncover file history and access details, view the file’s metadata.

<img width="635" height="321" alt="7 1" src="https://github.com/user-attachments/assets/827f6122-1166-4946-8343-641419a70e3c" />



 Displays file attributes such as MAC times (Modified, Accessed, Changed), size, and allocation info.

---


## *Step 6: Report Generation*

After completing your analysis:

1. *Compile All Outputs:*  
   Collect files like filesystem_info.txt, partitions.txt, file_list.txt, and timeline.txt.

2. *Interpret and Document:*  
   Write a clear summary explaining your findings, methods used, and any key recovered evidence.

---

## *Step 7: Evidence Preservation*

Ensuring the integrity of evidence is the final and most important step .

1. *Archive Evidence Securely:*  
   Use encryption  and hashing  to store your disk image and findings.

2. *Maintain Chain of Custody:*  
   Keep the evidence in a secure location following proper forensic protocols .

---
 # Rubrics
 ---
  
  | Criteria | Mark Allotted | Mark Awarded |
  |---|---:|---:|
  | 1. GitHub Activity & Submission Regularity | 3 | |
  | 2. Application of Forensic Tools & Practical Execution | 3 | |
  | 3. Documentation & Reporting | 2 | |
  | 4. Engagement, Problem-Solving & Team Collaboration | 2 | |
  | *Total* | *10* | |

---

## *Result*

Using the *Sleuth Kit (TSK)*, investigators can efficiently extract, analyze, and preserve digital evidence .  
It remains one of the most reliable and open-source forensic toolkits for digital investigation .
    
---
