
Abstract
The project is the design and implementation of an interactive World Wide Web-based Leave Management System. The Leave Management System automates the process of managing and tracking multiple types of student leaves. Students are able to submit the leave form and students can view their leave existing records. Faculty can also view the student existing records. The Leave Management System maintains a database to keep a running balance of each Students records.

1. Introduction

1.1 Purpose
The purpose of this document is to provide a detailed description of the Leave Management System. It outlines the system's functionalities, constraints, and requirements to be implemented by  our team.

1.2 Scope
The Leave Management System is designed to automate and streamline the process of managing leave requests and approvals within a college. The system will allow students to submit leave requests and view their leave records.

1.3 Definitions, Acronyms, and Abbreviations
SRS: Software Requirements Specification






2. Overall Description

2.1 Product Perspective
The Leave Management System will be a standalone web-based application that integrates with the faculties of the College. It will be accessible to students and faculties through their web browsers.

2.2 User Classes and Characteristics
Student:
It has the following columns:
•	prnnumber (integer, primary key): The PRN (Permanent Registration Number) of the student, serving as a unique identifier for each student.
•	username (varchar): The username or name of the student.
•	email (varchar): The email address of the student.
•	mobile (integer): The mobile or phone number of the student.
•	password (varchar): The password for the student's account.
•	leave_id (integer, foreign key references LeaveForm.leave_id): This column 


•	The LeaveForm table represents the leave forms submitted by students.
•	It has the following columns:
•	leave_id (integer, primary key, auto-increment): The unique identifier for each leave form.
•	description (varchar): A description or reason for the leave request.
•	task (varchar): Details of the tasks or activities to be performed during the leave period.
•	startDate (date): The start date of the requested leave.
•	student_id (integer, foreign key references Student.prnnumber): The PRN of the student who submitted the leave form.
•	endDate (date): The end date of the requested leave.

•	The Faculty table represents faculty or staff information.
•	It has the following columns:
•	empid (integer, primary key, auto-increment): The employee ID or unique identifier for each faculty member.
•	username (varchar): The username or name of the faculty.
•	email (varchar): The email address of the faculty.
•	password (varchar): The password for the faculty's account.
•	mobile (integer): The mobile or phone number of the faculty.
•	student_prn (integer, foreign key references Student.prnnumber): This column establishes a one-to-many relationship with the Student table, indicating that a faculty member can be associated with multiple students based on their PRN.


2.3 Operating Environment
The Leave Management System will be developed as a web application and will require a compatible web browser. The system will be hosted on a web server and will connect to a database server to store and retrieve data.

2.4 Design and Implementation Constraints
The system should be developed using a technology stack that is compatible with the existing IT infrastructure of the organization. 




2.5  Clear Registration Steps: 
Clearly outline the steps involved in the registration process, breaking them down into simple and sequential instructions. For example:
● Step 1: Access the registration page.
● Step 2: Fill out the registration form with your basic information.
● Step 3: Choose a username and password.
● Step 4: Click the "Register"  button to complete the registration.

3. System Features and Requirements
3.1 Functional Requirements
3.1.1 Student Functionality
The system should allow students to register and log in securely. Students should be able to submit leave requests specifying the type of leave, start and end dates, and any additional comments. Students should be able to view their leave records.

3.1.2 Faculty Functionality
Faculty should be able to log in securely to access the system.
Faculty should be able to view and review leave requests, including the students details, requested dates, and leave type.

3.2 Non-functional Requirements
3.2.1 Security
The system should implement secure user authentication and access controls. Students and Faculty data should be securely stored. The system should adhere to relevant data protection regulations and privacy requirements.

3.2.2 Performance
The system should be able to handle concurrent user requests efficiently. Response times for common operations should be within acceptable limits.
3.2.3 Usability
The system should have a user-friendly interface. Clear instructions and error messages should be provided to users. The system should be accessible across different devices and screen sizes.
3.2.4 Reliability
The system should be highly available and maintain data integrity. 




4. System Interfaces

4.1 User Interfaces
The system will have a web-based user interface for Students to submit leave requests and view their leave records. Faculty will have a separate interface to review leave requests. 

4.2 Software Interfaces
The system will integrate with the college faculty to manage existing students data. 

5. Appendices

Include any additional information that may be relevant to the Leave Management System.
This Software Requirements Specification (SRS) document provides a comprehensive outline of the Leave Management System's functionalities, constraints, and requirements. It serves as a reference for the development team to design, develop, and implement the system successfully.

