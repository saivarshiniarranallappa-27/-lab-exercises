# Experiment 9: Using Process Explorer to Identify Suspicious Processes

## Aim
To use **Process Explorer** to identify and analyze suspicious processes running on a Windows system.

## Objective
- Monitor running processes and their resource usage.  
- Verify digital signatures of executables.  
- Detect hidden or unauthorized processes.

## Procedure

### Step 1: Launch Process Explorer
Open `procexp.exe`. The Process Explorer window displays a hierarchical view of all running processes, showing their CPU usage, memory usage, and parent–child relationships.  
![Screenshot 1](https://github.com/user-attachments/assets/c1bdb2e5-9c0c-4251-b320-480d70d626e8)

### Step 2: Viewing Process Details
Right-click on any process and choose **Properties**. The “Image” tab shows the process file path, command line, and creation time. This helps verify if the process is legitimate or suspicious.  
![Screenshot 2](https://github.com/user-attachments/assets/cf557a96-f286-4342-abbc-a4f94acb3856)

### Step 3: Analyzing Process Properties
Explore the other tabs such as **Performance** and **Threads** to view real-time CPU usage, thread activity, and memory statistics for the selected process.  
![Screenshot 3](https://github.com/user-attachments/assets/367cba93-c138-41e4-b2e1-8a0ff78825d2)

### Step 4: Viewing Thread and Performance Tabs
In the **Threads** tab, you can inspect all threads started by the process and their CPU consumption. The **Performance** tab shows graphs of resource usage.  
![Screenshot 4](https://github.com/user-attachments/assets/fb7954e7-5741-40de-ad17-74eb2aa3b586)

### Step 5: Checking Loaded DLLs
Go to **View → Lower Pane View → DLLs** to see the list of DLLs loaded by the process. This helps in identifying injected or malicious modules.  
![Screenshot 5](https://github.com/user-attachments/assets/dd89a0e1-da90-4071-90ec-286712bd62ea)

### Step 6: Verifying Process Signatures
Hover over or check the **Verified Signer** column to confirm the authenticity of each process. A missing or invalid signature might indicate a potentially malicious file.  
![Screenshot 6](https://github.com/user-attachments/assets/9d0847d4-bee6-4b1d-8489-9893e87cdddd)

### Step 7: Handling Suspicious Processes
If a suspicious process is detected, right-click on it and choose **Kill Process** or **Suspend** to stop its execution. Always confirm its path and digital signature before taking action.  
![Screenshot 7](https://github.com/user-attachments/assets/b3367c45-758b-4ac7-9c93-ba65dad5f3c9)

## Observation
All system and user processes were successfully displayed with their respective CPU and memory usage. Unsigned or abnormal processes were identified by verifying signatures and observing their file paths.

---

## Rubrics

| Criteria | Mark Allotted | Mark Awarded |
|-----------|---------------:|--------------:|
| 1. GitHub Activity & Submission Regularity | 3 | |
| 2. Application of Forensic Tools & Practical Execution | 3 | |
| 3. Documentation & Reporting | 2 | |
| 4. Engagement, Problem-Solving & Team Collaboration | 2 | |
| **Total** | **10** | |

---

## Result
**Process Explorer** successfully helped in identifying and analyzing suspicious processes in the system.



 

 
  
  






  
