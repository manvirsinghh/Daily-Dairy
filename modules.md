# REPORT

**DATE:** 29/01/2025

### **Start time:** 9:00 AM  
**Task:** Frappe modules

---

### **Issue 1:**  
I have created these fields in the Address doctype. 

![image](https://github.com/user-attachments/assets/b72a17f5-c5a0-4818-879a-d0f7dfdf4a83)



In the Geo module, I have the City and Country doctypes and linked the country field of the Address doctype to the Geo module's country doctype. The OpenStreetMap was added, but it does not show the latitude and longitude when I enter the address.

**Paused At:** 10:30 AM  
**Resumed At:** 12:00 PM

---

### **Issue 2:**  
I read about the email module. I tried to send a welcome email notification to a user. First, I created an email account and filled in the information. Then, I created an email template that I wanted to send. After that, I set up the notification to send the email when a new user is created. I created a user with their email ID and name and saved it. The problem is that when I create a user, I don't see any email notification.

**End at:** 4:09 PM

---

### **Task:** Read Frappe installation script automation on VirtualBox  
**Start time:** 4:15 PM  
**End time:** 6:00 PM

---

### **Task:** View Q&A and read their answers  
**Start time:** 6:30 PM  

1) **Can I transfer data from Server A to B from my laptop C, using curl?**  
   **Ans:**  
   - **Scenario 1**: Download the file from Server A to your laptop, then upload it to Server B using curl.  
   - **Scenario 2**: Stream data directly from Server A to Server B by piping the output of curl from Server A to Server B, bypassing your laptop’s storage.

2) **Is it good practice to store large data in a database? Like photos, documents, etc?**  
   **Ans:**  
   Storing large files like photos and documents directly in a database is not recommended because it can degrade performance, increase database size, and make maintenance harder.  
   A better approach is to store files in a dedicated file storage system (e.g., AWS S3).

3) **Tools similar to wget**  
   **Ans:**  
   curl, aria2, lftp, HTTPie, uget

4) **How to download any website for offline viewing using wget?**  
   **Ans:**  
   To download a website for offline viewing using wget, use this command:  
   ```bash
   wget -r -np -k https://example.com
       -r: Recursively download the site.
    -np: No parent (avoid downloading from parent directories).
    -k: Convert links for offline viewing.
    Just replace https://example.com with the website you want to download.

  5) **Difference between curl and cron?**
    Ans:
        curl is for transferring data (downloading/uploading).
        cron is for scheduling tasks to run at specified intervals.

  6)  **Why link without www is not opening?**
    Ans:
    A link without www might not open because:
        The website may be set up to only work with the www version (e.g., www.example.com), and not the non-www version (e.g., example.com).
        The DNS records may only be configured for the www version, and not the root domain.
        The server may be configured to respond only to requests with www.

Dinner break:-8:30pm
Resumed At:-9:00pm
End time:-11:00pm

