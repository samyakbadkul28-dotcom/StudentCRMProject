# Phase-9: Integration  

## 📖 Overview  
In this phase, we integrated Salesforce with external systems to make the CRM more powerful and connected.  
We focused on:  
1. **Web-to-Lead Form** – allow students to submit inquiries via a web form that automatically creates Student Inquiry records in Salesforce.  
2. **(Optional) Email-to-Salesforce** – automatically log email communication inside Salesforce.  

---

## 🌐 Web-to-Lead Form Integration  

**Purpose:**  
Enable students to fill out an online form → auto-create a Student Inquiry record in Salesforce.  

**Steps Taken:**  
1. Setup → Quick Find → **Web-to-Lead**.  
2. Enabled Web-to-Lead.  
3. Created a Web-to-Lead Form and included fields: Student Name, Email, Phone, Interest Area, Source.  
4. Generated HTML form code.  
5. Saved HTML file locally and tested by submitting inquiry.  
<img width="1365" height="644" alt="Phase9_WebToLead_FormSetup" src="https://github.com/user-attachments/assets/9308e878-b484-459d-9593-5183c3300c00" />

 <img width="1363" height="675" alt="Phase9_WebToLead_TestSubmission" src="https://github.com/user-attachments/assets/6df1f4fa-6eac-466d-892d-333b481bd3ed" />

 

**Result:**  
When a student submits the form, a new Student Inquiry record is automatically created in Salesforce.  

---

## 📧 Email-to-Salesforce (Optional)  

**Purpose:**  
Automatically track emails exchanged with students inside Salesforce.  

**Steps Taken:**  
1. Setup → Quick Find → **Email-to-Salesforce**.  
2. Copied the unique Salesforce email address.  
3. BCC’d this address in Gmail/Outlook when sending student-related emails.  


**Result:**  
Emails sent externally now also appear inside Salesforce under the student’s record.  

---

## ✅ Outcome  

- Students can now self-submit inquiries through a web form → instantly visible in Salesforce.  
- Admissions staff have email communication automatically logged.  
- Integration reduces manual data entry and improves visibility.  

---


