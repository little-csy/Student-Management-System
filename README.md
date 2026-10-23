# Student Management System

A C# desktop application for managing student records, course enrollment, and grades. Built with a client–server architecture, the system provides separate interfaces for students, teachers, and administrators.

Developed as a team project for the **Database System Principles** course at **Xiamen University**, completed in June 2022.

## Features

### Students

- View personal information, course schedules, grades, and GPA.
- Search courses by ID or name and look up department information.
- Enroll in courses with confirmation and duplicate enrollment checks.
- Change passwords after verifying the current password.

### Teachers

- View and update personal information.
- Search students by ID, name, or class.
- View teaching schedules, assigned courses, and enrolled students.
- Enter student grades and change passwords.

### Administrators

- Search, add, and update student, teacher, class, and course records.
- Manage course credits, capacity, schedules, instructors, and classrooms.
- Create and delete student and teacher login accounts.
- Change administrator passwords.

## Architecture

The application uses **C#** and a **relational database** named `StudManager`. Its client–server design separates the presentation layer, data access layer, and database.

```text
Users → Presentation Layer → Data Access Layer → Database
```

Login validates the username, password, and selected role, then displays the corresponding menus.

## Database Structure

| Table | Purpose |
| --- | --- |
| `Student` | Student records |
| `Teacher` | Teacher records |
| `Course` | Course details and scheduling |
| `ClassInfo` | Class records |
| `ClassRoom` | Classroom information |
| `Department` | Department information |
| `SC` | Student course enrollments and grades |
| `User_Admin`, `User_Stu`, `User_Tea` | Login accounts for each role |

## Grade Reporting

Students can review course scores, grade classifications, grade points, and average GPA. The documented calculation applies a weight of **1.2** to required courses and **1.0** to elective courses.


Preview:

<img width="812" height="484" alt="image" src="https://github.com/user-attachments/assets/32fc7a45-1494-4481-a0f4-cf968500c446" />
<img width="822" height="479" alt="image" src="https://github.com/user-attachments/assets/045b6656-b832-4a17-abd7-32b11c98952d" />
<img width="808" height="487" alt="image" src="https://github.com/user-attachments/assets/575fee2a-775a-4c28-909e-2112e29d9b5f" />
<img width="763" height="515" alt="image" src="https://github.com/user-attachments/assets/13983578-e137-4e24-b6fc-264738f45769" />




