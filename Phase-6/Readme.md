# Phase-6: Security & Access Control  

## 📖 Overview  
In this phase, we implemented **Salesforce security and access controls** to protect student data and define who can do what in the Admissions CRM.  

We configured:  
1. **Profiles** – define baseline permissions  
2. **Permission Sets** – grant extra permissions without changing profiles  
3. **Roles & Role Hierarchy** – manage record visibility  
4. **Organization-Wide Defaults (OWD)** – set baseline record access  
5. **Sharing Rules** – allow controlled data sharing  

---

## 👥 Users  
We created different users to test profiles and roles (e.g., Counselor, Admissions Manager).  

---

## 🔐 Profiles  
Profiles control what objects a user can access.  

- **Admissions Staff Profile** – can create/edit Student Inquiries, create Applications, read Enrollments & Programs  
- **Counselor Profile** – can edit Applications in addition to inquiries  
- **Admissions Manager Profile** – full access  

<img width="1361" height="661" alt="Profile_AdmissionsStaff" src="https://github.com/user-attachments/assets/493cdba3-438f-4da7-be10-9a3e1566a304" />


---

## 🎟️ Permission Sets  
We created a **Report Builder Access** permission set:  
- System Permission → *Create and Customize Reports*  
- Assigned to a Counselor user  

<img width="1364" height="672" alt="PermissionSet_ReportBuilder" src="https://github.com/user-attachments/assets/78f2d209-dbc2-494a-b4f8-3ac5a9fe27b8" />

<img width="1363" height="657" alt="PermissionSet_Assignment" src="https://github.com/user-attachments/assets/05b1d0f6-7883-4459-9db1-080080a91c5f" />


---

## 🏢 Roles & Role Hierarchy  
Roles define record visibility in a tree structure:  
- Admissions Manager (top)  
  - Counselors  
    - Admissions Staff  

Managers can see records owned by their subordinates.  

<img width="1324" height="617" alt="Roles_Hierarchy" src="https://github.com/user-attachments/assets/3a963969-bf6a-4bf5-87f2-d945f34e7496" />


---

## 🛡️ Organization-Wide Defaults (OWD)  
We set baseline access levels:  
- Student Inquiry → **Private**  
- Application → **Private**  
- Enrollment → **Public Read Only**  
- Program → **Public Read Only**  
<img width="1350" height="607" alt="OWD_Settings" src="https://github.com/user-attachments/assets/d1be51aa-a01c-456a-8f09-292876769e18" />

---

## 🔗 Sharing Rules  
To let Counselors see each other’s Student Inquiries, we created a sharing rule:  
- Rule Name: `Counselors_Share_Inquiries`  
- From Role: Counselor  
- To Role: Counselor  
- Access: Read/Write  
<img width="1077" height="112" alt="SharingRule_Counselors" src="https://github.com/user-attachments/assets/d7df6a1f-830a-46c8-b7d9-4cb66c6160e7" />


---



## 🎯 Outcome  
- Data is secure and only visible to the right users  
- Managers get visibility into their teams’ records  
- Counselors can collaborate via sharing rules  
- Permission sets provide flexible access without modifying profiles  

---

