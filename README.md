# Gym-Management-System-GMS-SDD
<Gym Management System >

Submitted by
<Altaf Hussain(F22BINFT1M01262)>

Submitted to
<Dr Musarat Karim >

Department of Information Technology
Faculty of Computing
The Islamia University of Bahawalpur

Summery
The Gym Management System is a web-based application developed using PHP, MySQL, HTML, CSS, and JavaScript.
It runs on a local server (XAMPP/WAMP) and works offline.
The system digitizes gym operations such as member and trainer management.
It allows attendance tracking and payment recording.
A secure admin login controls access to all system modules.
All data is stored centrally in a MySQL database.
The system reduces manual paperwork and human errors.
It improves efficiency and speeds up data retrieval.
The modular design ensures reliability and easy maintenance.
Future enhancements include online registration, mobile support, and analytics dashboards. 
Table of Contents
    1. Introduction
1.1 Purpose
1.2 Scope
1.3 Intended Audience
    2. System Architecture
2.1 Architectural Overview
2.2 Architectural Characteristics
    3. Module Design
3.1 Authentication (Login) Module
3.2 Member Management Module
3.3 Trainer Management Module
3.4 Attendance Management Module
3.5 Payment Management Module
3.6 Reports Module
    4. Data Design
4.1 Database Design Strategy
4.2 Main Database Tables
    5. Interface Design
5.1 User Interface Design
5.2 Navigation Design
    6. Security Design
    7. Error Handling and Validation
    8. Non-Functional Design Considerations
8.1 Performance
8.2 Reliability
8.3 Maintainability
8.4 Portability
    9. Design Constraints
    10. Future Design Enhancements
    11. Conclusion
                1. Introduction
1.1 Purpose
This Software Design Document (SDD) provides a detailed description of the architecture, design decisions, modules, data structures, and interfaces of the Gym Management System. It translates the requirements defined in the SRS into a technical blueprint for system implementation.
1.2 Scope
The Gym Management System is a web-based, locally hosted application designed to automate gym operations including member management, trainer management, attendance tracking, payment handling, and reporting. The system runs on a local server (XAMPP/WAMP) and is accessible only to an authenticated admin.
1.3 Intended Audience
    • Software Developers
    • Project Supervisor
    • Evaluators / Examiners
    • Maintenance & Support Team

                    2. System Architecture
2.1 Architectural Overview
The system follows a Three-Tier Web Architecture.
Architecture Type
    • Standalone
    • Web-based
    • Localhost (Offline)
System Layers
    • Presentation Layer (HTML, CSS, JavaScript)
    • Application Layer (PHP Business Logic)
    • Data Layer (MySQL Database)
2.2 Architectural Characteristics
    • No internet dependency
    • Centralized database
    • Secure admin-controlled access
    • Modular and scalable design

                     3. Module Design
3.1 Authentication (Login) Module
Responsibilities
    • Admin authentication
    • Session management
    • Unauthorized access prevention
Main Functions
    • validateLogin()
    • createSession()
    • logoutUser()
Inputs
    • Username
    • Password
Outputs
    • Admin dashboard access

3.2 Member Management Module
Responsibilities
    • Add, update, and delete members
    • Assign membership plans
    • View member details
Main Functions
    • addMember()
    • updateMember()
    • deleteMember()
    • viewMembers()
Data Stored
    • Member ID
    • Name
    • Contact details
    • Membership plan
    • Joining and expiry dates

3.3 Trainer Management Module
Responsibilities
    • Manage trainer records
    • Assign trainer schedules
Main Functions
    • addTrainer()
    • updateTrainer()
    • deleteTrainer()
    • manageSchedule()
Data Stored
    • Trainer ID
    • Name
    • Specialization
    • Contact details

3.4 Attendance Management Module
Responsibilities
    • Record daily attendance
    • View attendance history
Main Functions
    • markAttendance()
    • viewAttendanceReport()
Data Stored
    • Attendance ID
    • Member ID
    • Date
    • Status (Present/Absent)

3.5 Payment Management Module
Responsibilities
    • Record member payments
    • Track dues and membership validity
Main Functions
    • addPayment()
    • viewPaymentHistory()
    • checkPendingDues()
Data Stored
    • Payment ID
    • Member ID
    • Amount
    • Payment date
    • Membership validity

3.6 Reports Module
Responsibilities
    • Generate system reports
Main Functions
    • generateMemberReport()
    • generateAttendanceReport()
    • generatePaymentReport()
Report Types
    • Member list
    • Trainer list
    • Attendance summary
    • Payment summary

                4. Data Design
4.1 Database Design Strategy
    • Relational database (MySQL)
    • Normalized schema
    • Primary and foreign keys enforced
4.2 Main Database Tables
Member Table
    • member_id (PK)
    • name
    • phone
    • plan_id
    • join_date
    • expiry_date
Trainer Table
    • trainer_id (PK)
    • name
    • specialization
    • phone
Attendance Table
    • attendance_id (PK)
    • member_id (FK)
    • date
    • status
Payment Table
    • payment_id (PK)
    • member_id (FK)
    • amount
    • payment_date
Membership Plan Table
    • plan_id (PK)
    • plan_name
    • duration
    • fee

                      5. Interface Design
5.1 User Interface Design
    • Simple admin dashboard
    • Form-based input screens
    • Tabular data display
    • Consistent layout
5.2 Navigation Design
    • Login → Dashboard
    • Sidebar/menu for module access
    • Logout option

                   6. Security Design
    • Encrypted passwords stored in database
    • Session-based authentication
    • SQL injection prevention
    • Restricted admin-only access
    • Input validation on all forms

                7. Error Handling and Validation
    • Required field validation
    • Numeric validation for payment fields
    • Error messages for invalid login
    • Confirmation dialogs before delete operations

                8. Non-Functional Design Considerations
8.1 Performance
    • Optimized SQL queries
    • Fast response on local server
    • Supports 1,000+ records
8.2 Reliability
    • Stable CRUD operations
    • Manual database backup support
8.3 Maintainability
    • Modular PHP file structure
    • Well-commented code
    • Scalable database schema
8.4 Portability
    • Runs on any Windows system with XAMPP/WAMP
    • Browser-independent operation

               9. Design Constraints
    • Localhost-only deployment
    • Single admin user
    • No cloud access
    • Dependency on PHP and MySQL

          10. Future Design Enhancements
    • Online member registration
    • Payment gateway integration
    • Responsive mobile user interface
    • Automated backups
    • Analytics dashboards
    • Multi-user role support

                  11. Conclusion
This Software Design Document provides a complete technical blueprint for implementing the Gym Management System. The design ensures secure, efficient, and maintainable management of gym operations while supporting future scalability and feature expansion.
