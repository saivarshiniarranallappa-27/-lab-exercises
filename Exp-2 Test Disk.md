# Experiment No. 2: Recover Deleted or Damaged Files using TestDisk

**Aim:**  
Use TestDisk to recover a missing partition and repair a corrupted one.

---

<p align="center">
  <img src="https://github.com/user-attachments/assets/bccd84c0-81ff-4f96-acfe-b06689c1194c" width="80%" />
</p>


- TestDisk lists all detected disks with their sizes.  
- Select the disk that has the lost partition (arrow keys).  
- If available on your system, prefer the raw device `/dev/rdisk*` over `/dev/disk*` for faster I/O.  
- Choose the **partition table type** (TestDisk usually auto-detects correctly) and press **Enter** to proceed.

---

<p align="center">
  <img src="https://github.com/user-attachments/assets/e899ef29-5adf-4e47-98f6-c525f42b13f8" width="80%" />
</p>


- From the main menu, select **Analyse** to inspect current partition structure and search for lost ones.  
- Review the shown structure for problems:  
  - Same partition listed twice → partition table corruption.  
  - “Invalid NTFS boot” → NTFS boot sector is damaged (filesystem corruption).  
- Choose **Quick Search** to continue.

---

<p align="center">
  <img src="https://github.com/user-attachments/assets/72821706-fc21-4d48-b0f2-21f5be7b5c98" width="80%" />
</p>


- Quick Search displays results in real time; your missing logical partition may appear (e.g., *Partition 3*).  
- Highlight a found partition and press **`p`** to list files (press **`q`** to go back).  
  - Files shown in **red** are deleted entries.  
- If directory listings look correct, press **Enter** to proceed.

---

<p align="center">
  <img src="https://github.com/user-attachments/assets/509d5c71-6443-40cd-a2e4-381a17522792" width="80%" />
</p>


- If something is still missing, run **Deeper Search**.  
- This scans each cylinder and checks FAT/NTFS/ext backup structures to find more partitions.  
- After the scan:  
  - Some entries may be duplicated or overlapping.  
  - Entries marked **D (Deleted)** won’t be recovered if left as D.  
  - Identify which overlapping entry is the *correct* one (use **`p`** to preview files).

---

<p align="center">
  <img src="https://github.com/user-attachments/assets/450922c6-fb7c-49cc-9ab6-0aafaf42596f" width="80%" />
</p>


- Use **`p`** on each candidate to verify which has a healthy file listing.  
- Leave the **bad**/damaged one as **D (Deleted)**.  
- Change the **correct** one to **L (Logical)** (or **P (Primary)** / **\* (bootable)** if appropriate) using left/right arrows.  
- Press **Enter** to proceed after statuses are set.

---

<p align="center">
  <img src="https://github.com/user-attachments/assets/73a1ad98-c5cf-4df9-b112-bd20f0762cff" width="80%" />
</p>


- When all partitions are correctly defined, choose **Write** → confirm with **Enter**, then **y**, then **OK**.  
- If the NTFS boot sector of a partition is bad but the **backup boot sector** is valid, choose **Backup BS** to copy the backup over the main boot sector.  
- After a successful copy, the boot sector and its backup become identical.

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/232ca666-7f34-4c74-b2fb-572b0bb022f9" width="80%" />
</p>


- TestDisk will indicate that you must **restart** to access the recovered data.  
- Press **Enter** to exit and **reboot** the system.  
- After reboot, verify the partition and files in your OS.

---

## Conclusion
Following TestDisk’s **Analyse → (Quick/Deeper) Search → Set Status → Write → (Backup BS)** flow allows recovery of lost partitions and repair of corrupted NTFS boot sectors with minimal risk. Always verify files with **`p`** before writing changes.



