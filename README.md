# Task Management System

## Overview

The **Task Management System** is my graduation project from ALX program. It is a web-based application developed using Oracle APEX. It allows users to manage their tasks effectively while providing administrators the ability to view and oversee all tasks created by users. This project demonstrates the use of database-driven applications with user authentication, password hashing, and role-based access control.

## Features

- **User Registration**: Users can create an account to manage their tasks.
- **User Authentication**: Secure login system with hashed passwords.
- **Task Management**: Users can create, update, and delete their tasks.
- **Admin Dashboard**: Admins can view all tasks created by users.
- **Role-Based Access Control**: Different permissions for regular users and administrators.
- **User-Specific Task Display**: Each user can see only their own tasks, while admins can view all tasks.

## Technologies Used

- **Oracle APEX**: Application development framework for building web applications.
- **Oracle Database**: Backend database for storing user and task information.
- **PL/SQL**: Procedural language used for server-side processing and business logic.
- **HTML/CSS**: Frontend technologies for creating a user-friendly interface.

## Database Schema

### Users Table

| Column Name | Data Type    | Constraints                  |
|-------------|--------------|------------------------------|
| USER_ID     | NUMBER       | Primary Key, Auto-Increment  |
| USERNAME    | VARCHAR2     | UNIQUE                       |
| PASSWORD    | VARCHAR2     | NOT NULL                     |
| EMAIL       | VARCHAR2     |                              |
| ROLE        | VARCHAR2     | Default 'User'               |

### Tasks Table

| Column Name | Data Type    | Constraints                  |
|-------------|--------------|------------------------------|
| TASK_ID     | NUMBER       | Primary Key, Auto-Increment  |
| TITLE       | VARCHAR2     | NOT NULL                     |
| DESCRIPTION | VARCHAR2     |                              |
| START_DATE    | DATE         |                              |
| DUE_DATE    | DATE         |                              |
| USER_ID     | NUMBER       | Foreign Key (Users)         |

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/Task_Management_System.git
   ```

2. **Set Up the Database**:
Import the SQL scripts for creating the Users and Tasks tables into your Oracle database.
Ensure that the hash_password function is created for password hashing.

3. **Deploy the APEX Application**:
Import the APEX application into your Oracle APEX environment.
Configure the authentication scheme and database connection as needed.

## Usage
1. **Navigate to the application URL in your web browser.**
2. **Register a new user or log in with existing credentials.**
3. **Manage tasks through the user interface.**
4. **Admin users can access the admin dashboard to view all tasks.**

## Contributing
Contributions are welcome! If you have suggestions for improvements or bug fixes, please fork the repository and submit a pull request.

## Acknowledgments
**Thanks to Oracle APEX for providing a powerful platform for rapid application development.**
**Special thanks to ALX program.**
**Thanks to the community resources and documentation that made this project possible.**