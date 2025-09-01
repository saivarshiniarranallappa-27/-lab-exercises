# Experiment No. 4: Analyze Email Headers and Detect Email Spoofing using MHA (Mail Header Analyzer)

---


This experiment demonstrates how to extract and analyze an email header to detect spoofing.  
Mail Header Analyzer (MHA) and similar tools help visualize email routing, authentication, and anomalies.

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/1b95d575-9cca-4ff8-96cd-7bb2a84a9c50" width="80%" />
</p>


Access the **email header** from your email client:  
- **Gmail:** More (three dots) → Show original  
- **Outlook:** File → Properties → Internet headers box  
- **Yahoo:** More (three dots) → View raw message  

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/8cd0d3b8-ac47-424b-a871-f51fb141842f" width="80%" />
</p>


 It contains metadata such as:  
- `From`, `To`, `Date`, `Subject`  
- `Return-Path`  
- `Received` chain (server hops)  
- `Message-ID`  
- SPF/DKIM/DMARC authentication results  

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/576d05cb-dbf4-4ff9-a834-6831141eabc1" width="80%" />
</p>


 
Each line shows:  
- Sending server hostname/IP  
- Receiving server hostname/IP  
- Date/time of handoff  
Check for suspicious IPs or mismatched hostnames.

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/24d0fc44-c6a4-43b1-a256-2a962812ad18" width="80%" />
</p>


Verify they match the expected sending servers.  
Flag unusual locations or unknown domains.

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/236f7349-f2f6-4625-b0ff-b7c05932d30c" width="80%" />
</p>

 
- SPF Pass → IP authorized for domain  
- DKIM Pass → Message content intact  
- DMARC Pass → SPF/DKIM alignment  
Failures may indicate spoofing or tampering.

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/5ae72266-bcff-43da-a18f-4f8061fb0a93" width="80%" />
</p>


- Domain mismatches (From vs Return-Path vs Message-ID)  
- Suspicious IPs or server names  
- Irregular timestamps in `Received` lines  
Use online tools like **MXToolbox** or **Google’s G Suite Toolbox** to automate parsing.  
Document and report findings if spoofing is detected.

---

## Conclusion
By carefully examining headers — especially `Received` lines, IP ownership, and SPF/DKIM/DMARC results — investigators can detect spoofed or malicious emails. MHA and other online analyzers make this process faster and easier.
