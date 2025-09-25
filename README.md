# Campus Course & Records Manager (CCRM)

**CCRM** is a console-based Java SE application that allows institutes to manage students, courses, enrollments, grades, and transcripts with import/export functionality.

---

## Project Overview

Campus Course & Records Manager (CCRM) is designed to handle:

- **Students**: Add, update, deactivate, and enroll/unenroll in courses.
- **Courses**: Add, update, list, search, assign instructors.
- **Grades & Transcripts**: Record marks, compute GPA, and print transcripts.
- **File Utilities**: Import/export CSV files and perform timestamped backups of course/student data.

**How to Run:**

1. Ensure **Java SE 17** or higher is installed.
2. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Campus-Course-Records-Manager.git
Open the project in Eclipse IDE.

Compile and run the main class:

bash
Copy code
javac -d bin src/edu/ccrm/MainApp.java
java -cp bin edu.ccrm.MainApp
Evolution of Java
1995 – Java 1.0: Platform-independent programming language.

1998 – Java 1.2: Collections Framework introduced.

2004 – Java 5: Generics, enums, annotations, enhanced for-loop.

2011 – Java 7: NIO.2, try-with-resources, improved I/O.

2014 – Java 8: Lambda expressions, Stream API, functional programming.

2017 – Java 9–10: Modules, local-variable type inference.

2021 – Java 17: LTS, enhanced pattern matching, modern date/time API improvements.

Java ME vs SE vs EE
Feature	Java ME	Java SE	Java EE
Target	Mobile & embedded devices	Desktop & standard apps	Large-scale enterprise apps
Libraries	Lightweight APIs	Core Java APIs	Servlets, JSP, EJB, Web Services
Deployment	Small devices, IoT	PCs, laptops	Application servers
Use Case	Mobile apps, embedded systems	Console & GUI apps	Enterprise web apps, distributed systems

JDK, JRE, and JVM Explained
JVM (Java Virtual Machine): Executes Java bytecode and provides platform independence.

JRE (Java Runtime Environment): JVM + core libraries to run Java applications.

JDK (Java Development Kit): JRE + compiler (javac) + development tools for building Java applications.

Flow:

scss
Copy code
Java Source (.java) → javac compiler → Bytecode (.class) → JVM executes
Windows Install Steps
1. Install Java SE
Download JDK from Oracle/OpenJDK.

Run the installer and set JAVA_HOME:

ini
Copy code
JAVA_HOME = C:\Program Files\Java\jdk-17
Add to Path:

ini
Copy code
PATH = %JAVA_HOME%\bin;%PATH%
Verify installation:

bash
Copy code
java -version
javac -version
Screenshot:

2. Install Eclipse IDE
Download Eclipse IDE for Java Developers.

Extract and open eclipse.exe.

Create a new Java project: File → New → Java Project → Project Name → Finish.

Import source files (src/edu/ccrm/...).

Right-click MainApp.java → Run As → Java Application.

Screenshot:

Mapping Table: Syllabus Topic → File/Class/Method
Syllabus Topic	File/Class	Method/Implementation
Encapsulation	Student.java	private fields + getters/setters
Inheritance	(Optional) Instructor.java → Person.java	N/A
Polymorphism	TranscriptService.java	printTranscript()
Abstraction	Person.java (abstract)	Abstract methods for Student/Instructor
Exception Handling	StudentService.java	addStudent(), removeStudent()
File I/O (NIO.2)	ImportExportService.java	exportStudents(), importStudents()
Streams & Lambdas	ReportService.java (optional)	filter/search courses using Stream API
Enums	Semester.java, Grade.java	Course.semester, Transcript.grade
Recursion	BackupService.java	computeBackupSize(Path path)

Enabling Assertions
Assertions are used to check program correctness during development.

Code Example:

java
Copy code
assert student.getId() != null : "Student ID cannot be null";
Enable Assertions at Runtime:

bash
Copy code
java -ea edu.ccrm.MainApp
Usage Example
java
Copy code
StudentService studentService = new StudentService();
EnrollmentService enrollmentService = new EnrollmentService();
TranscriptService transcriptService = new TranscriptService();
ImportExportService ioService = new ImportExportService("data");

// Add students, enroll, record grades, export/import CSV
Screenshots
Program Running Example:

Backup Folder Structure:

References
Oracle Java SE Documentation: https://docs.oracle.com/javase/

Java Tutorials: https://docs.oracle.com/javase/tutorial/

Java NIO.2 Guide: https://docs.oracle.com/javase/7/docs/api/java/nio/file/package-summary.html