# Campus Course & Records Manager (CCRM)

CCRM is a console-based Java SE application for managing students, courses, enrollments, grades, and transcripts. It also supports CSV import/export and automated backups.

---

## 📌 Project Overview

This project demonstrates core Java SE concepts (OOP, file handling, enums, exception handling) through a real-world academic records management system.

### Features
- Add, update, and deactivate students  
- Manage courses and assign instructors  
- Enroll/unenroll students in courses  
- Record grades, calculate GPA, print transcripts  
- Import/export CSV files, create timestamped backups  

---

## ▶️ How to Run

**Requirements:** Java SE 17 or higher  

### Steps:
```bash
# Clone repository
git clone https://github.com/your-username/Campus-Course-Records-Manager.git

# Compile main class
javac -d bin src/edu/ccrm/MainApp.java

# Run application
java -cp bin edu.ccrm.MainApp
