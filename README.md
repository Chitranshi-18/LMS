# 🗂️ Leave Management System (LMS)

[GitHub Repository](https://github.com/Chitranshi-18/LMS)  

A **group project** for managing student leave requests, approvals, and tracking, with a focus on **database design and SQL implementation**.

---

## 💼 My Contribution

- Designed an **ER diagram** and implemented a **normalized MySQL schema** capturing core entities:  
  `Student`, `Warden`, `HOD`, `Admin`, `Leave Request`
- Built **SQL queries** to:  
  - Retrieve leave records  
  - Calculate approved leaves  
  - Support eligibility validation  
  - Generate leave slips
- Assisted in mapping the **leave approval workflow** via database relationships  

> ⚠️ **Note:** Frontend and backend components (PHP, HTML, CSS, JS) were implemented by other team members. My focus was **database design and SQL logic**.

---

## ⚙️ Project Overview

- **Role-based access:** Different permissions for Student, Warden, HOD, and Admin  
- **Leave request tracking:** Submission, approval/rejection, and leave history  
- **Database-driven workflow:** Approval status maintained via MySQL tables  

---
## 📦 Database Schema & Files

- **Tables:** `Students`, `Users`, `Leave_Requests`, `HOD`, `Warden`, `Admin`  
- **Relationships:** One-to-many between Users and Leave Requests, implementing the leave approval workflow  
- **Normalization:** Ensured minimal redundancy and data integrity  

All database-related work is available in the [`database/`](./database) folder:

- `ER_diagram.png` – visual representation of the database schema  
- `schema.sql` – MySQL schema creation file  
- `sample_queries.sql` – example SQL queries implemented  


---
### Example SQL Query

Retrieve approved leaves for each student:

```sql
SELECT s.name, lr.leave_date, lr.status
FROM Students s
JOIN Leave_Requests lr ON s.id = lr.student_id
WHERE lr.status = 'Approved';

Count total approved leaves per student:


```sql
SELECT student_id, COUNT(*) AS approved_leaves
FROM Leave_Requests
WHERE status = 'Approved'
GROUP BY student_id;


---

## 🔗 Contact

For questions or collaboration, reach out at:  
📧 chitranshi181200@gmail.com
