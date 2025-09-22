# 📚 Library Management System – Database Schema

## 📌 Project Overview
This project is part of the **SQL Developer Internship Task 1**.
The goal is to design a **well-structured database schema** for a **Library Management System**, ensuring normalization, relationships, and data integrity.

---

## 🗂️ Database Schema

### **Entities & Attributes**

1. **Members**
- `member_id` (PK)
- `name`
- `email` (unique)
- `phone`
- `membership_date`

2. **Staff**
- `staff_id` (PK)
- `name`
- `role`
- `hire_date`

3. **Books**
- `book_id` (PK)
- `title`
- `author`
- `isbn` (unique)
- `published_year`
- `available_copies`

4. **Loans**
- `loan_id` (PK)
- `book_id` (FK → Books.book_id)
- `member_id` (FK → Members.member_id)
- `staff_id` (FK → Staff.staff_id)
- `loan_date`
- `return_date`

---

## 🔑 Keys & Relationships
- **Primary Keys (PK):** `member_id`, `staff_id`, `book_id`, `loan_id`
- **Foreign Keys (FK):**
  - `Loans.book_id → Books.book_id`
  - `Loans.member_id → Members.member_id`
  - `Loans.staff_id → Staff.staff_id`
- **Relationships:**
  - A **Member** can borrow many **Books**
  - A **Book** can be borrowed many times (through Loans)
  - A **Staff member** manages many **Loans**

---

## 📊 ER Diagram

![Library ER Diagram](<img width="283" height="203" alt="library_er_diagram" src="https://github.com/user-attachments/assets/12a75f08-c65c-4c4e-b0b9-4921fdb02e5e" />
)

---

## 🛠️ SQL Script

SQL DDL file: [`library_schema.sql`](library_schema.sql)

---

