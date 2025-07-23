# EED-e-Learning-Platform
The EED E-Learning Platform is a comprehensive, role-based web application designed to streamline the management and delivery of technical and vocational training at the Entrepreneurship Development (EED) Center of the Federal Polytechnic Mubi.

# Key Features (Bulleted List)
# Three-Tier Role-Based Access Control (RBAC):
Admin: Global oversight with a dashboard showing platform-wide statistics. Manages units, questions, materials, and coordinator assignments.
Coordinator: Scoped management of a single, assigned unit. Manages materials and questions, and monitors student performance for their specific unit.
Student: A personalized learning portal focused on their single registered unit, with access to materials and a one-time quiz.
# Dynamic Dashboards:
Each user role gets a unique dashboard tailored to their specific tasks and needs.
Admin dashboard features summary cards for students, units, questions, and assigned/unassigned coordinators, plus unit-level performance metrics.
Coordinator dashboard provides statistics and detailed student/score tables for their specific unit.
# Comprehensive Content Management:
Admins and Coordinators can upload course materials (PDFs, videos, etc.) for different units.
A streamlined interface allows for the direct creation and deletion of quiz questions for each unit.
# Secure Authentication & Registration:
Secure login system with password hashing (password_hash).
A robust registration system that captures different details based on the selected role.
First-Admin Security: The system automatically disables new admin registrations after the first admin account is created.
# Quiz and Assessment System:
Students can take a quiz for their assigned unit once.
Scores are automatically calculated and saved to the database.
Students can view their quiz history and performance on their dashboard.
Admins and Coordinators can view detailed score reports for their respective scopes.
# Coordinator Assignment Module:
Admins have a dedicated interface to assign coordinators to specific units.
The system prevents a single unit from being assigned to multiple coordinators and includes an "Unassign" feature.

# Core Functionality & User Roles
The platform revolves around a three-tier user hierarchy, ensuring that each user only has access to the tools and information relevant to their role.
# 1. Administrator
The Administrator has a "bird's-eye view" of the entire platform.
Central Dashboard: View high-level statistics, including total students, units, and questions, as well as a breakdown of assigned vs. unassigned coordinators. It also displays quiz performance summaries for every unit.
Unit Management: Create and delete the technical skill units offered by the center (e.g., Tailoring, Solar Installation).
Coordinator Management: Create coordinator accounts and assign them to a specific unit using an intuitive interface that prevents duplicate assignments.
Content Oversight: Can upload materials and add/remove quiz questions for any unit on the platform.
Reporting: View and print detailed score reports for any student in any unit.
# 2. Coordinator
The Coordinator has a focused management portal for their single, assigned unit.
Scoped Dashboard: View statistics and performance metrics relevant only to their assigned unit, including student count and average quiz score.
Student Monitoring: Access a detailed list of all students registered under their unit and view their quiz scores.
Content Creation: Directly manage the learning content for their unit by uploading course materials and creating/deleting quiz questions.
# 3. Student
The Student has a streamlined and personalized learning path.
Personal Dashboard: Upon login, the student is greeted with a personalized dashboard focused on their single registered unit.
Access to Materials: View and download all course materials (PDFs, videos) uploaded by their coordinator.
Quiz System: Take a randomized quiz for their unit to test their knowledge. The system is designed for a single attempt to ensure fair assessment.
Track Performance: View their quiz score and history directly on their dashboard.
Technology Stack
# Backend: PHP
Database: MySQL / MariaDB
Frontend: HTML5, CSS3, Bootstrap 5, JavaScript
Server: Apache (designed for a XAMPP/LAMP environment)
Setup & Installation
Clone the repository: git clone https://github.com/your-username/eed-elearning.git
Import the database.sql file into your MySQL/phpMyAdmin database.
Configure your database connection in includes/db.php.
Place the project files in your web server's root directory (e.g., htdocs for XAMPP).
Navigate to login.php in your browser and register the first Admin account. Subsequent admin registrations will be disabled automatically.
