# EduTrack

## Project Overview
The EduTrack Registration System is a Java-based application that is designed to manage course registration, student records, professor assignments, and administrative tasks for a university setting. The system allows students to register for courses, professors to manage their courses, and administrators to oversee and manage the entire system. It is a command line interface and it utilises popular OOPs concepts.

It introduces new features such as generic feedback handling, extended user role management via inheritance, and robust exception handling. These enhancements are implemented while maintaining the core functionality of the original system.

## Files Overview

### Main.java
The main entry point of the application. This file initializes the system, including sample data for students, professors, and courses. It provides the user interface for signing up, logging in, and navigating through the application’s features based on user roles (Student, Professor, Administrator).

### Administrator.java
Defines the `Administrator` class, which extends the `User` class. Administrators can manage the course catalog, student records, and professor assignments. They can also handle complaints and oversee various administrative tasks.

### Student.java
Defines the `Student` class, which extends the `User` class. Students can sign up for courses, view their schedules, track academic progress, drop courses, and manage complaints. The class includes methods for interacting with the course list and performing various student-related actions.

### Professor.java
Defines the `Professor` class, which extends the `User` class. Professors can be assigned to courses, manage course details (e.g., schedule, syllabus, enrollment limits), and view enrolled students. The class includes methods for updating course information and interacting with the courses they are assigned to.

### User.java
Defines the `User` class, which serves as a base class for `Student` and `Professor`. It includes basic user properties such as email and password, along with methods for login and logout.

### Course.java
Defines the `Course` class, representing a university course. It includes properties such as course code, title, credits, schedule, enrollment limit, semester, and location. The class also manages course prerequisites and enrolled students.

### Complaint.java
Defines the `Complaint` class, which represents a student complaint. It includes properties for the complaint description and status, and methods for managing complaints.

### UserInterface.java
Defines an interface that includes login and logout methods, which are implemented by the User class and its subclasses (Student, Professor, and Administrator).

## Installation
1. Ensure you have Java JDK installed on your system.
2. Clone or download the project repository.
3. Compile the Java files:
    ```sh
    javac Main.java Administrator.java Student.java Professor.java User.java Course.java Complaint.java
    ```
4. Run the application:
    ```sh
    java Main
    ```

## Usage

### Sign Up:
Choose to sign up as a Student or Professor. Provide the required details (email, password, ID, semester/office hours).
### Login:
Log in as a Student, Professor, or Administrator using your credentials.
### Student Menu:
Students can view available courses, register for courses, view their schedule, track academic progress, drop courses, submit and view complaints, and proceed to the next semester.
### Professor Menu:
Professors can manage their assigned courses (update schedule, syllabus, enrollment limit) and view enrolled students.
### Administrator Menu:
Administrators can manage the course catalog (add/remove courses), manage student records, assign professors to courses, handle complaints, and log out.

## Object-Oriented Programming Concepts Utilized

### Abstraction:
The UserInterface provides a clear contract for classes to implement login and logout methods. This abstracts away the implementation details and allows different user types to have their own login behaviors.

### Inheritance:
The User class is a base class that provides common properties (like email, password) and methods (login, logout) for Student, Professor, and Administrator. These subclasses inherit these properties and can extend or override them as needed.

### Polymorphism:
The system uses polymorphism to treat instances of Student, Professor, and Administrator as instances of the User class, allowing the program to use a unified interface for different user types. For example, the handleLogin method uses polymorphism to handle login functionality for different user types.

### Encapsulation:
The classes use private fields with public getter and setter methods to protect and manage access to sensitive information, such as user credentials (email, password) in the User class and course details in the Course class.

### Interfaces:
The UserInterface is used to define a contract for classes that need login and logout functionalities. This allows for a flexible and consistent way to implement user interactions across various user types.

## File Descriptions

- **Main.java**: Contains the main logic and user interface for interacting with the system.
- **Administrator.java**: Contains functionalities for administrators.
- **Student.java**: Contains functionalities for students.
- **Professor.java**: Contains functionalities for professors.
- **User.java**: Base class for all user-related classes.
- **Course.java**: Represents a course in the system.
- **Complaint.java**: Represents a complaint submitted by a student.


