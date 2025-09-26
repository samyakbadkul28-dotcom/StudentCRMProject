# Phase-8: Automation  

## 📖 Overview  
In this phase, we implemented **automation in Salesforce** to enforce data quality, auto-update records, and notify users automatically.  

We covered three main automation tools:  
1. **Validation Rules** – to prevent bad data.  
2. **Workflow Rules** – to auto-update fields based on conditions.  
3. **Flows (Record-Triggered)** – to send email alerts when criteria are met.  

---

## 🛑 Validation Rule – Require Email in Student Inquiry  

**Purpose:**  
Ensure every Student Inquiry has an Email before saving.  

**Steps Taken:**  
- Created Validation Rule on **Student Inquiry** object.  
- Rule Formula:  
- Error Message: “Email is required for every Inquiry.”  
- Location: Email field.  
<img width="1303" height="646" alt="Phase8_ValidationRule_RequireEmail" src="https://github.com/user-attachments/assets/e764afac-ebfc-4a99-a5c2-c6315825a7fa" />

---

## ⚙️ Workflow Rule – Auto-Qualify High-Score Inquiries  

**Purpose:**  
Automatically qualify inquiries with a high lead score.  

**Steps Taken:**  
- Created Workflow Rule on **Student Inquiry** object.  
- Criteria: `Lead_Score__c > 8`  
- Action: Field Update → set **Status = Qualified**  
- Activated the rule.  
<img width="1114" height="576" alt="Phase8_WorkflowRule_LeadScore" src="https://github.com/user-attachments/assets/bd42608b-7dbd-48d2-9011-1d8dbe524b16" />



---

## 🔄 Flow – Notify Manager on Submitted Applications  

**Purpose:**  
Send an email to Admissions Manager whenever an Application is submitted.  

**Steps Taken:**  
- Created a **Record-Triggered Flow** on **Application** object.  
- Trigger: When record is created/edited.  
- Condition: `Status = "Submitted"`  
- Action: Send **Email Alert** using an email template.  
- Activated the Flow.  
<img width="1342" height="673" alt="Phase8_Flow_ApplicationSubmitted" src="https://github.com/user-attachments/assets/93e2f14f-58f5-4594-ad98-777b49188f7a" />


---

## ✅ Outcomes  

- Validation Rules prevented incomplete or wrong data.  
- Workflow automatically qualified high-scoring inquiries.  
- Flow triggered email notifications to managers for submitted applications.  

This phase reduced manual effort, improved data quality, and made the admissions process more efficient.  

---



