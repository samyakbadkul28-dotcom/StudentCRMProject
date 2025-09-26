# Phase-7: Data Management  

## 📖 Overview  
In this phase, we managed data in Salesforce by:  
- Preparing objects with External ID fields  
- Importing Programs, Student Inquiries, Applications, and Enrollments  
- Handling import errors  
- Setting up duplicate management (Matching Rule + Duplicate Rule)  
- Backing up data with Data Export  
- Creating Data Quality reports  

This ensures data integrity, proper parent-child relationships, and error-free imports.  

---

## 🔹 Step 0 — Prepare Objects  
- Checked **Record Name** type (Text vs Auto Number).  
- Created External ID fields:  
  - Program Code (`Program_Code__c`)  
  - Inquiry External Id (`Inquiry_External_Id__c`)  
  - Application External Id (`Application_External_Id__c`)  
  - Enrollment External Id (`Enrollment_External_Id__c`)  

---

## 🔹 Step 1 — Import Programs  
- Imported `Programs.csv` using **Data Import Wizard**.  
- Mapped fields: Program Code, Department, Duration, Fees.  
<img width="1361" height="671" alt="Phase7_Programs_ImportResults" src="https://github.com/user-attachments/assets/902a50c9-af8b-4712-b36e-99c31a2bdc33" />

---

## 🔹 Step 2 — Import Student Inquiries  
- Imported `Student_Inquiries.csv`.  
- Mapped fields: Inquiry External Id, Student Name, Email, Phone, Source, Interest Area, Status, Lead Score.  
<img width="1352" height="667" alt="Phase7_Inquiries_FieldMapping" src="https://github.com/user-attachments/assets/0d2383f3-451f-42bd-8473-01d26a78c7cd" />

<img width="1346" height="671" alt="Phase7_Inquiries_ImportResults" src="https://github.com/user-attachments/assets/539171cf-5a68-49e8-aa48-cc7eaac8fb2b" />


## 🔹 Step 3 — Import Applications  
- Imported `Applications.csv`.  
- Linked Applications to Student Inquiries and Programs using External IDs.  

<img width="1365" height="686" alt="Phase7_Applications_FieldMapping" src="https://github.com/user-attachments/assets/600b2bd6-c8b5-4d10-84ca-7b677f2a1a71" />

<img width="1365" height="656" alt="Phase7_Applications_ImportResults" src="https://github.com/user-attachments/assets/34108dfa-9258-4e0c-8cd1-c50acf3a1931" />

---

## 🔹 Step 4 — Import Enrollments  
- Imported `Enrollments.csv`.  
- Linked Enrollments to Applications via Application External Id.  
<img width="1354" height="671" alt="Phase7_Enrollments_FieldMapping" src="https://github.com/user-attachments/assets/7077e892-5e3f-4b4b-b9d2-11d4fa56e05b" />


<img width="1353" height="680" alt="Phase7_Enrollments_ImportResults" src="https://github.com/user-attachments/assets/a3825ade-697c-4669-bc28-a1441aba649b" />

---

## 🔹 Step 5 — Handle Import Errors  
- Downloaded Error File when imports failed.  
- Fixed issues like missing External IDs or wrong date formats.  
- Re-ran import with corrected CSV.  

---

## 🔹 Step 6 — Duplicate Management  
### Matching Rule (by Email)  
- Created Matching Rule: Email must be unique.  
<img width="1125" height="489" alt="Phase7_MatchingRule_Email" src="https://github.com/user-attachments/assets/6113b37e-cf47-4c0f-8791-11a25ff58fae" />



### Duplicate Rule  
- Created Duplicate Rule to block/alert duplicates during Inquiry creation.  
<img width="1365" height="671" alt="Phase7_DuplicateRule_Email" src="https://github.com/user-attachments/assets/fde41264-e1a3-44c5-8dfb-fbf1a60d84e3" />



## 🔹 Step 7 — Data Export (Backup)  
- Used Data Export Service to download backup of Programs, Inquiries, Applications, Enrollments.  

📸 Insert screenshots:  
<img width="1352" height="669" alt="Phase7_DataExport_Request" src="https://github.com/user-attachments/assets/d5eb036a-45a3-4d90-b0c0-7fe5ff40060b" />
e7_DataExport_Request.png`  

---

## 🔹 Step 8 — Data Quality Reports  
### Report 1: Missing Emails  
- Report to find Student Inquiries with blank Email.  
<img width="1365" height="574" alt="Phase7_Report_MissingEmail" src="https://github.com/user-attachments/assets/947cd7f1-c781-4b76-805b-970278a6ee04" />



### Report 2: Duplicate Emails  
- Grouped report by Email → found duplicates.  
 <img width="1303" height="500" alt="Phase7_Report_DupesByEmail" src="https://github.com/user-attachments/assets/3f438463-a9bf-4729-b8a8-8f9ebf61c95d" />

---

## ✅ Conclusion  
Phase-7 ensured that our data is clean, validated, and backed up. Using External IDs and duplicate management improves data accuracy, while quality reports help monitor issues like missing or duplicate emails.  

---


