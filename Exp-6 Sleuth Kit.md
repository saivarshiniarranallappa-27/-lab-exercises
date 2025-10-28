</head>
<body>

  <div class="container">
    <h1>Experiment 06 — Sleuth Kit Analysis</h1>

    <h3>Aim:</h3>
    <p>
      To analyze digital evidence using the Sleuth Kit (TSK) tools and extract file system, partition, and metadata information from a disk image for forensic purposes.
    </p>

    <h3>Objective:</h3>
    <p>
      The objective of this experiment is to learn and perform forensic analysis using Sleuth Kit tools. 
      Commands such as <b>fsstat</b>, <b>mmls</b>, <b>fls</b>, <b>icat</b>, and <b>istat</b> help examine disk partitions, list files, extract data, and analyze metadata.
    </p>

    <h3>Procedure with Screenshots:</h3>

    <div class="step">
      <h4>Step 1: Install Sleuth Kit</h4>
      <p>
        Download Sleuth Kit from the official website or trusted source and install it on your Windows system.
        Open the Command Prompt and navigate to the installation directory to ensure it’s working properly.
      </p>
      <img src="https://github.com/user-attachments/assets/7abe267b-e607-451f-b58a-16e97bd06858" alt="Sleuth Kit Installation Screenshot">
    </div>

    <div class="step">
      <h4>Step 2: Acquire Disk Image</h4>
      <p>
        Use tools like <b>FTK Imager</b> or <b>dd</b> to create a forensic disk image. The image file format can be <code>.dd</code>, <code>.img</code>, or <code>.E01</code>.
      </p>
      <img src="https://github.com/user-attachments/assets/73a36faa-ed5e-4c0d-9ad4-45f67c23a931" alt="Acquire Disk Image Screenshot">
    </div>

    <div class="step">
      <h4>Step 3: Identify File System Type</h4>
      <p>
        Use the <b>fsstat</b> command to get information about the file system of the image.
      </p>
      <p><code>fsstat [image file] &gt; filesystem_info.txt</code></p>
      <img src="https://github.com/user-attachments/assets/8cffaaf5-7f49-45d4-a7ad-42ea2ce5e9ad" alt="fsstat Command Screenshot">
    </div>

    <div class="step">
      <h4>Step 4: List Partitions</h4>
      <p>
        Use the <b>mmls</b> command to view all partitions present in the image.
      </p>
      <p><code>mmls [image file] &gt; partitions.txt</code></p>
      <img src="https://github.com/user-attachments/assets/8b29af79-16ee-4a75-b095-7ccf9ccd13db" alt="mmls Command Screenshot">
    </div>

    <div class="step">
      <h4>Step 5: List Files and Directories</h4>
      <p>
        Use the <b>fls</b> command to list all files and directories recursively.
      </p>
      <p><code>fls -r [image file] &gt; file_list.txt</code></p>
      <img src="https://github.com/user-attachments/assets/9f0aa5a3-4292-4e59-a545-59b76e22223f" alt="fls Command Screenshot">
    </div>

    <div class="step">
      <h4>Step 6: Extract Files</h4>
      <p>
        Use <b>icat</b> to extract a file using its inode number. Replace the inode number with one from the <b>fls</b> output.
      </p>
      <p><code>icat [image file] [inode number] &gt; extracted_file</code></p>
      <img src="https://github.com/user-attachments/assets/22970889-abe2-46ef-a7b4-e91c5f0307ab" alt="icat Extraction Screenshot">
    </div>

    <div class="step">
      <h4>Step 7: View Metadata Information</h4>
      <p>
        Use the <b>istat</b> command to view detailed metadata information for a specific inode.
      </p>
      <p><code>istat [image file] [inode number] &gt; metadata_info.txt</code></p>
      <img src="https://github.com/user-attachments/assets/67a5a2dd-41fe-474c-9486-bec7b02d9d6f" alt="istat Command Screenshot">
    </div>

    <div class="step">
      <h4>Step 8: Create a Timeline (Optional)</h4>
      <p>
        Generate a file activity timeline using <b>mactime</b>. This helps track file modifications, accesses, and creation times.
      </p>
      <p>
        <code>fls -m / -r [image file] &gt; body.txt</code><br>
        <code>mactime -b body.txt &gt; timeline.txt</code>
      </p>
    </div>

    <h3>Result:</h3>
    <p>
      The Sleuth Kit was successfully used to analyze the disk image. Details such as partition layout, file listings, metadata, and timelines were extracted and analyzed. 
      This experiment demonstrates how digital evidence can be recovered and interpreted for forensic investigation.
    </p>

    <footer>
      Prepared by: [Your Name] • Course: Digital Forensics Lab • Experiment No. 06
    </footer>
  </div>

</body>
</html>
