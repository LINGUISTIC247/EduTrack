# EduTrack – Automated Student Result Processing and Transcript Generation System

![ASP.NET](https://img.shields.io/badge/ASP.NET-Web%20Forms-blue)
![C#](https://img.shields.io/badge/C%23-.NET%20Framework%204.7.2-green)
![SQL Server](https://img.shields.io/badge/SQL%20Server-2022-red)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3.2-purple)
![License](https://img.shields.io/badge/License-Educational-orange)

## Overview

EduTrack is a comprehensive Academic Management System designed to automate student result processing, GPA/CGPA computation, transcript generation, and academic record management for universities, colleges, and tertiary institutions.

The system is developed using ASP.NET Web Forms, C#, ADO.NET, and SQL Server, following a layered architecture that separates business logic from data access operations for maintainability and scalability.

---

## Key Features

### Authentication & Security

* User Registration
* Secure Login System
* PBKDF2 Password Hashing
* Password Reset & Recovery
* Session-Based Authentication
* Role-Based Authorization
* Account Approval Workflow
* Failed Login Tracking
* Account Lockout Protection

### User Management

* User Account Creation
* User Approval System
* User Activation/Deactivation
* Profile Management
* Change Password
* Audit Tracking

### Student Management

* Add Students
* Edit Students
* Delete Students
* Search Students
* Automatic Matric Number Generation
* Student Profile Management

### Lecturer Module

* Result Entry
* Result Editing
* Result Submission
* Course Assignment Management

### Examination Officer Module

* Review Submitted Results
* Approve Results
* Reject Results
* Lock Approved Results
* Generate Official Transcripts

### Academic Processing

* Automatic Grade Assignment
* GPA Calculation
* CGPA Calculation
* Semester Performance Tracking
* Academic History Management

### Transcript Management

* Official Transcript Generation
* Transcript Preview
* Transcript Download
* PDF Export Using Built-in .NET Libraries

### Audit Logging

* Login Activity Tracking
* Profile Update Logs
* Password Change Logs
* Result Submission Logs
* Approval Workflow Logs
* Transcript Generation Logs

---

## Technology Stack

### Backend

* ASP.NET Web Forms
* C# 7.3
* .NET Framework 4.7.2
* ADO.NET

### Database

* SQL Server 2022+

### Frontend

* HTML5
* CSS3
* Bootstrap 5.3.2 (CDN)
* Bootstrap Icons 1.11.3
* Vanilla JavaScript

### Architecture

* Two-Layer Architecture
* Business Logic Layer (BLL)
* Data Access Layer (DAL)

---
##Every .aspx page must contain an embedded CSS block using the /* Modern EduTrack Design System */ comment.
The design language must be consistent across all pages and include:

* Glassmorphism cards
* Gradients
* Bootstrap Icons
* Hover effects, shadows, smooth animations, transitions
* Responsive layouts, dashboard widgets, professional tables & forms
* Animated buttons, modern alerts, empty‑state components, statistics cards
* Mobile responsiveness

## Project Structure

```text
EduTrack
│
├── Auth
│   ├── Login.aspx
│   ├── Register.aspx
│   ├── ForgotPassword.aspx
│   ├── ResetPassword.aspx
│   └── Logout.aspx
│
├── Admin
│   ├── AdminDashboard.aspx
│   ├── ManageUsers.aspx
│   ├── ManageStudents.aspx
│   └── ManageCourses.aspx
│
├── Lecturer
│   ├── LecturerDashboard.aspx
│   └── EnterResults.aspx
│
├── ExamOfficer
│   ├── ExamOfficerDashboard.aspx
│   └── ApproveResults.aspx
│
├── Student
│   ├── StudentDashboard.aspx
│   ├── ViewResults.aspx
│   └── ViewTranscript.aspx
│
├── Profile
│   ├── Profile.aspx
│   ├── EditProfile.aspx
│   └── ChangePassword.aspx
│
├── DAL
├── BLL
├── Models
├── Utilities
├── Reports
├── Documentation
│
├── Site.Master
├── Web.config
└── README.md
```

---

## Database

### Database Name

```sql
EduTrack
```

### Core Tables

```text
Users
Students
Lecturers
Departments
Programmes
Courses
Semesters
Results
Grades
GPARecords
CGPARecords
PasswordResets
AuditLogs
TranscriptRequests
SystemSettings
LoginAttempts
```

---

## User Roles

### Administrator

Responsibilities:

* Manage Users
* Approve Accounts
* Manage Courses
* Manage Departments
* Manage Programmes
* Configure System Settings
* View Audit Logs
* Generate Reports

---

### Lecturer

Responsibilities:

* Enter Results
* Edit Results Before Approval
* Submit Results
* View Assigned Courses

---

### Examination Officer

Responsibilities:

* Review Results
* Approve Results
* Reject Results
* Lock Results
* Generate Transcripts

---

### Student

Responsibilities:

* View Results
* View GPA
* View CGPA
* Download Transcript
* Manage Profile

---

## Grading System

| Score Range | Grade | Grade Point |
| ----------- | ----- | ----------- |
| 80 – 100    | A     | 4.0         |
| 70 – 79     | B+    | 3.5         |
| 60 – 69     | B     | 3.0         |
| 50 – 59     | C     | 2.5         |
| 40 – 49     | D     | 2.0         |
| 0 – 39      | F     | 0.0         |

---

## GPA Formula

[
GPA = \frac{\sum (GradePoint \times CreditHours)}{\sum CreditHours}
]

---

## System Requirements

### Software Requirements

* Visual Studio 2022
* .NET Framework 4.7.2 Developer Pack
* SQL Server 2022 or later
* SQL Server Management Studio (SSMS)
* IIS Express or IIS
* Modern Web Browser

---

## Installation Guide

### Step 1: Clone Repository

```bash
git clone https://github.com/linguistic247/EduTrack.git
```

---

### Step 2: Open Project

1. Open Visual Studio 2022
2. Select Open Project/Solution
3. Open the EduTrack solution

---

### Step 3: Create Database

Open SQL Server Management Studio and run:

```sql
CREATE DATABASE EduTrack;
GO
```

---

### Step 4: Execute Database Scripts

Run all generated SQL scripts in the following order:

```text
1. Database Creation Script
2. Table Creation Script
3. Constraints Script
4. Seed Data Script
```

---

### Step 5: Configure Connection String

Open:

```xml
Web.config
```

Update:

```xml
<connectionStrings>
  <add name="EduTrackConnection"
       connectionString="Data Source=YOUR_SERVER_NAME;
                         Initial Catalog=EduTrack;
                         Integrated Security=True"
       providerName="System.Data.SqlClient"/>
</connectionStrings>
```

---

### Step 6: Build Solution

```text
Build
 └── Rebuild Solution
```

---

### Step 7: Run Application

```text
Press F5
```

or

```text
Ctrl + F5
```

---

## Default Administrator Account

### Administrator Login

```text
Email:
edutrackadmin37@gmail.com

Password:
Nt5437132#37
```

### Important

Change the administrator password immediately after first login in a production environment.

---

## Security Features

* PBKDF2 Password Hashing
* Session Authentication
* Role-Based Authorization
* Parameterized SQL Queries
* SQL Injection Prevention
* Account Lockout Mechanism
* Password Reset Tokens
* Audit Logging
* Input Validation
* Server-Side Validation
* Client-Side Validation

---

## Development Architecture

### Presentation Layer

Handles:

* ASPX Pages
* User Interface
* User Interaction

### Business Logic Layer (BLL)

Handles:

* Business Rules
* GPA Calculation
* Validation Logic
* Workflow Processing

### Data Access Layer (DAL)

Handles:

* Database Connectivity
* CRUD Operations
* SQL Execution

---

## Future Enhancements

* Multi-Campus Support
* Email Notifications
* SMS Notifications
* REST API Integration
* Mobile Application
* Analytics Dashboard
* Course Registration Module
* Attendance Tracking Module

---

## Author

### Developer

**LINGUISTIC**

GitHub:

[linguistic247](https://github.com/linguistic247?utm_source=chatgpt.com)

LinkedIn:

[Timothy Akwasi Nyarko](https://www.linkedin.com/in/timothy-akwasi-nyarko-22a364357?utm_source=chatgpt.com)

Email:

**[edutrackadmin37@gmail.com](mailto:edutrackadmin37@gmail.com)**

---

## License

This project is developed for educational, research, and academic purposes.

You may modify, extend, and adapt the project for learning, coursework, institutional deployment, and software engineering practice.

---

## Project Vision

> To provide a secure, efficient, and automated platform for managing academic records, processing student results, calculating GPA/CGPA, and generating official transcripts while reducing manual workload and improving data accuracy across educational institutions.
