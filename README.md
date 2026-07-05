# LECS Student Management System

## Overview
**LECS Student Management System** is a comprehensive, web-based platform tailored for Libon East Central School (LECS). It is designed to streamline administrative tasks, manage student and teacher records, track academic progress, and automate the generation of critical educational forms and certificates.

This system provides dedicated portals for School Administrators and Teachers, enabling efficient management of the school's operational and academic needs.

## 🚀 Key Features

*   **Role-Based Access Control:** Secure portals for Administrators and Teachers with tailored permissions.
*   **Student Information Management:** Complete profiling of pupils including personal details, parental information, and academic status.
*   **Teacher & Staff Management:** Management of teaching and non-teaching staff profiles, positions, and assignments.
*   **Academic Tracking & Grading:** Streamlined encoding, tracking, and viewing of student grades across different quarters and subjects.
*   **Automated Form Generation:** Built-in PDF generation for standard DepEd forms:
    *   School Form 1 (SF1)
    *   School Form 9 (SF9) - Report Card
    *   School Form 10 (SF10) - Permanent Record
    *   Certificate of Enrollment (COE)
    *   Quarterly and Year-End Certificates
*   **Curriculum Management:** Administration of Grade Levels, Sections, Subjects, and School Years.
*   **Event Calendar:** Integrated calendar for tracking school events and academic schedules.

## 🛠️ Technology Stack

*   **Frontend:** HTML5, CSS3, JavaScript, FontAwesome
*   **Backend:** PHP (Native)
*   **Database:** MySQL / MariaDB
*   **PDF Generation:** TCPDF, FPDF

## ⚙️ Installation & Setup

Follow these steps to set up the project locally for development or testing:

### Prerequisites
*   Web Server stack like XAMPP, WAMP, or LAMP.
*   PHP 7.4 or higher.
*   MySQL / MariaDB database.
*   [Composer](https://getcomposer.org/) (for managing PHP dependencies).

### 1. Clone the Repository
```bash
git clone https://github.com/renjiyomo/sms-lecs.git
cd lecs
```

### 2. Configure the Database
1. Open your database management tool (e.g., phpMyAdmin).
2. Create a new database named `lecs_gis`.
3. Import your database schema into `lecs_gis`. *(Note: Ensure you are only importing the database structure and not sensitive student PII records into a public repository).*

### 3. Setup Database Connection
Ensure the database credentials match your local database setup (default for XAMPP is `root` with no password). Check the following files:
*   `Landing/Login/lecs_db.php`
*   `Landing/Login/Page/lecs_db.php`

> **Warning:** Never commit production database passwords to public repositories.

### 4. Install Dependencies
Navigate to the `Page` directory and run composer to install the required PDF generation libraries (like TCPDF):
```bash
cd Landing/Login/Page
composer install
```

### 5. Run the Application
1. Start your local web server (Apache & MySQL in XAMPP).
2. Ensure the project folder is placed in your `htdocs` (for XAMPP) or `www` (for WAMP) directory.
3. Access the application via your web browser:
   ```
   http://localhost/lecs/Landing/landing.html
   ```

## 🔒 Security Guidelines

Before deploying to a live production environment, please ensure:
*   **Credentials:** Change default database users (`root`) and use strong, unique passwords.
*   **Environment Variables:** Consider moving connection strings out of `.php` files and into environment variables.
*   **File Permissions:** Ensure upload directories (`Landing/Login/Page/uploads`) do not have execute permissions to prevent malicious script uploads.
*   **SSL:** Enforce HTTPS to encrypt data in transit, especially since the system handles student grades and passwords.

## 📄 License
This system is developed for Libon East Central School. All rights reserved.
