</head>
<body>

<h1>Experiment 9: Using Process Explorer to Identify Suspicious Processes</h1>

<h2>Aim</h2>
<p>To use Process Explorer to identify and analyze suspicious processes running on a Windows system.</p>

<h2>Objective</h2>
<ul>
  <li>Monitor running processes and their resource usage.</li>
  <li>Verify digital signatures of executables.</li>
  <li>Detect hidden or unauthorized processes.</li>
</ul>
<h2>Procedure </h2>

<h3>Step1: Launch Process Explorer</h3>
<p>Open <code>procexp.exe</code>. The Process Explorer window displays a hierarchical view of all running processes, showing their CPU usage, memory usage, and parent–child relationships.</p>
<img src="https://github.com/user-attachments/assets/c1bdb2e5-9c0c-4251-b320-480d70d626e8" alt="Screenshot 1">


<h3>Step 2: Viewing Process Details</h3>
<p>Right-click on any process and choose <strong>Properties</strong>. The “Image” tab shows the process file path, command line, and creation time. This helps verify if the process is legitimate or suspicious.</p>
<img src="https://github.com/user-attachments/assets/cf557a96-f286-4342-abbc-a4f94acb3856" alt="Screenshot 2">

<h3>Step 3: Analyzing Process Properties</h3>
<p>Explore the other tabs such as <strong>Performance</strong> and <strong>Threads</strong> to view real-time CPU usage, thread activity, and memory statistics for the selected process.</p>
<img src="https://github.com/user-attachments/assets/367cba93-c138-41e4-b2e1-8a0ff78825d2" alt="Screenshot 3">


<h3>Step 4: Viewing Thread and Performance Tabs</h3>
<p>In the Threads tab, you can inspect all threads started by the process and their CPU consumption. The Performance tab shows graphs of resource usage.</p>
<img src="https://github.com/user-attachments/assets/fb7954e7-5741-40de-ad17-74eb2aa3b586" alt="Screenshot 4">

<h3>Step 5: Checking Loaded DLLs</h3>
<p>Go to <strong>View → Lower Pane View → DLLs</strong> to see the list of DLLs loaded by the process. This helps in identifying injected or malicious modules.</p>
<img src="https://github.com/user-attachments/assets/dd89a0e1-da90-4071-90ec-286712bd62ea" alt="Screenshot 5">

<h3>Step 6: Verifying Process Signatures</h3>
<p>Hover over or check the <strong>Verified Signer</strong> column to confirm the authenticity of each process. A missing or invalid signature might indicate a potentially malicious file.</p>
<img src="https://github.com/user-attachments/assets/9d0847d4-bee6-4b1d-8489-9893e87cdddd" alt="Screenshot 6">

<h3>Step 7: Handling Suspicious Processes</h3>
<p>If a suspicious process is detected, right-click on it and choose <strong>Kill Process</strong> or <strong>Suspend</strong> to stop its execution. Always confirm its path and digital signature before taking action.</p>
<img src="https://github.com/user-attachments/assets/b3367c45-758b-4ac7-9c93-ba65dad5f3c9" alt="Screenshot 7">

<h2>Observation</h2>
<p>All system and user processes were successfully displayed with their respective CPU and memory usage. Unsigned or abnormal processes were identified by verifying signatures and observing their file paths.</p>

<h2>Result</h2>
<p>Process Explorer successfully helped in identifying and analyzing suspicious processes in the system.</p>

<h2>Conclusion</h2>
<p>Process Explorer is an effective forensic tool that allows investigators to detect, verify, and terminate suspicious processes, thereby improving system security and malware detection.</p>

</body>
</html>



 

 
  
  






  
