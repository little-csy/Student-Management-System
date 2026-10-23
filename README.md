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

![image](https://user-images.githubusercontent.com/73229305/220565752-72087d35-fa0c-45e1-b7ff-78502397d2b8.png)

![image](https://user-images.githubusercontent.com/73229305/220565823-4112975e-04ae-46af-a784-5a0b9f94446a.png)
