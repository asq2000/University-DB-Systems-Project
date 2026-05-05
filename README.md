# 🗄️ University Database System — Final Project
### Database Systems | Final Project

---

## 📌 Overview

This project involves designing and implementing a **relational database system**
for a university. The system manages student and course information, and tracks
student enrollments using SQLite — all built and queried within a Jupyter Notebook.

---

## 📁 Project Files

| File | Description |
|------|-------------|
| [`student_db.sqlite.ipynb`](student_db.sqlite.ipynb) | Main Jupyter Notebook — database implementation & queries |
| [`Final Project.db-Report.pdf`](Final%20Project.db-Report.pdf) | Full project report including schema, E/R diagram & results |

---

## 🗂️ Database Design

### Relational Schemas

**STUDENT**
```sql
STUDENT(
    StudentID INT PRIMARY KEY,
    StudentName VARCHAR(100)
)
```

**COURSE**
```sql
COURSE(
    CourseID INT PRIMARY KEY,
    CourseName VARCHAR(100),
    Credits INT
)
```

**ENROLLMENT**
```sql
ENROLLMENT(
    StudentID INT,
    CourseID INT,
    PRIMARY KEY (StudentID, CourseID),
    FOREIGN KEY (StudentID) REFERENCES STUDENT(StudentID),
    FOREIGN KEY (CourseID) REFERENCES COURSE(CourseID)
)
```

---

## 🔗 E/R Diagram

| Entity | Attributes |
|--------|-----------|
| **STUDENT** | StudentID *(PK)*, StudentName |
| **COURSE** | CourseID *(PK)*, CourseName, Credits |
| **ENROLLMENT** | StudentID *(FK)*, CourseID *(FK)* |

> **Relationship:** Students and Courses share a **many-to-many** relationship,
> resolved through the ENROLLMENT junction table linking StudentID and CourseID.

---

## 🎯 Project Goals

- Design a normalized relational database schema for a university system
- Model entities (Students, Courses) and their relationships (Enrollment)
- Implement the database using SQLite
- Write and execute SQL queries to interact with the data

---

## 🛠️ Technologies Used

- Python
- Jupyter Notebook
- SQLite
- SQL (DDL & DML)

---

## 🚀 How to Run

1. Clone the repository:
```bash
   git clone https://github.com/asq2000/Database--Final-Project.git
```

2. Open the Jupyter Notebook:
```bash
   jupyter notebook student_db.sqlite.ipynb
```

3. Run the cells in order to create the database and execute queries.

---

## 👤 Author

**asq2000**
- GitHub: [@asq2000](https://github.com/asq2000)
- Email: angeleesq3@gmail.com

---

## 📚 Course

**Database Systems — Final Project**

---

*Built with 🗄️ SQL and Python*
