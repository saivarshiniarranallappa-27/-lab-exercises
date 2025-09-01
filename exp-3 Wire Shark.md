# Experiment No. 3: Password Capturing using Wireshark

**Aim:**  
Capture and inspect network traffic with Wireshark to locate login credentials transmitted in cleartext (HTTP).

---


Wireshark is a network protocol analyzer that captures packets transmitted over the network. When login forms are submitted over unencrypted HTTP, usernames and passwords can be seen in packet payloads. This experiment shows how to capture such traffic and filter it to find credentials.

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/2ff01719-7ac3-4268-9eb0-bf75f72a9a02" width="80%" />
</p>


Open **Wireshark** on your machine (Windows or Linux VM). Start capturing packets on the appropriate network interface (e.g., Wi-Fi or Ethernet). Make sure you have permissions to capture on that interface.

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/af22375f-7610-444e-9084-bdedb166c647" width="80%" />
</p>


While Wireshark is capturing, open the target website in your browser and perform a login using the test credentials. This generates the packets that contain the login request and form data.

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/b870b9ce-a48a-43d8-9afb-de5e243c8280" width="80%" />
</p>


To narrow down the captured packets, use display filters. First look for plain HTTP traffic by applying the filter:

This shows only HTTP protocol packets in the capture.

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/9cd13912-f658-4f32-9a6f-0ee401a12e96" width="80%" />
</p>


Login form submissions commonly use either GET or POST. Filter for GET requests if you want to see URL query-based submissions:

Often GET does not include form body data (credentials are rarely in GET body), so if GET yields nothing, check POST.

---

<p align="center">
  
  <img src="https://github.com/user-attachments/assets/906a9333-e8f8-4a32-9fc1-0c3ee0ae7fbe" width="80%" />
</p>


Filter for POST requests to find form data sent in the request body:

Click a POST packet of interest and inspect the **"HTML form URL Encoded"** (or the packet's payload) in the packet details pane to view submitted form fields.

---


When you expand the POST packet's details under **Hypertext Transfer Protocol → Form item**, you may see lines like:

This confirms the captured username and password exactly as submitted by the browser.

---


- This experiment demonstrates how unencrypted HTTP can expose sensitive credentials. Never capture or use credentials you do not have permission to access.  
- Always obtain explicit authorization before performing packet captures on networks or systems that are not your own.  
- Prefer HTTPS in real deployments — it encrypts form data and prevents simple sniffing.

---

## Conclusion
Using Wireshark with simple filters (`http`, `http.request.method == "GET"`, `http.request.method == "POST"`) makes it straightforward to find submitted form data during a login action when the site uses unencrypted HTTP. This experiment highlights the importance of TLS/HTTPS for protecting user credentials.






