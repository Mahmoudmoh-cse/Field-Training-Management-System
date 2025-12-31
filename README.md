# Field-Training-Management-System
The Field Training Management System (FTMS) is a centralized application designed to streamline student internship management at the university. It manages student enrollment, mentor assignment, organization approvals, report submissions, and evaluations. The system supports all stakeholders: students , internal and external mentors, evaluators, coordinators, and administrators.

# Objectives

Enable students to register for internships and submit reports.

Allow coordinators to approve/reject organizations and assign mentors.

Support mentors and evaluators in monitoring student progress.

Provide admins with full management control and reporting capabilities.

Ensure data integrity, efficient queries, and structured workflow.

# Technologies Used

SQL – Relational database design and queries

MySQL / MariaDB – Database engine

Stored Procedures, Views – For automation and reporting

ERD / EERD – Data modeling

Normalization – Third Normal Form (3NF) applied for all tables

# Key Features
1️⃣ Student Features

Register for internships (Field Training 2 – 2 credit hours, level 3+)

Submit internship reports

Receive evaluations from internal and external mentors

2️⃣ Mentor & Evaluator Features

Internal mentors guide assigned students

External mentors and evaluators evaluate students’ reports

Track weekly evaluations and provide feedback

3️⃣ Organization Features

Only coordinator-approved organizations are available

Track internships hosted by each organization

4️⃣ Admin Features

Manage users, mentors, students, and organizations

Ensure weekly and final reports are submitted

Maintain database integrity

Generate comprehensive reports

# Database Structure
Main Entities

User, Student, Admin, Mentor, Internal Mentor, External Mentor

Internship Coordinator, Internship Evaluator

Internship, Organization, Internship Report, Evaluation

Apply_For, Host, Submits, Phones, UserPhoneNumbers

Relationships

Admin → Users (1:M)

Student ↔ Internship (M:M via Apply_For)

Coordinator → Internship (1:M)

Organization ↔ Internship (M:M via Host)

Internal Mentor → Student (1:M)

Evaluator / External Mentor → Internship (1:M)

Student ↔ Internship_Report (M:M via Submits)

Evaluator / External Mentor → Evaluation (M:1)

Normalization

All tables normalized to 3NF:

1NF: No multivalued attributes

2NF: No partial dependencies

3NF: No transitive dependencies
