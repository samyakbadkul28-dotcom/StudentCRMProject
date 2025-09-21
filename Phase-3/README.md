# Phase 3 – Data Modeling & Relationships

This folder contains the custom objects and relationships designed for the Student Enrollment CRM project.

## Objects Created
1. **Student Inquiry**
   - Fields: Email, Phone, Source, Interest Area, Status, Assigned Counselor, Lead Score
2. **Program**
   - Fields: Department, Duration, Fees
3. **Application**
   - Fields: Student Inquiry (Lookup), Program (Lookup), Application Date, Status
4. **Enrollment**
   - Fields: Application (Lookup), Enrollment Date, Status

## Relationships
- Student Inquiry → Applications (1:N)
- Program → Applications (1:N)
- Application → Enrollment (1:1)

## Deliverables
- DataModelSteps.txt – step-by-step setup guide
- Screenshots – proof of all objects, fields, and schema builder
