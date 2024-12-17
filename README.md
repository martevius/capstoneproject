# capstoneproject
class project

Software Requirements Specification (SRS)

---

Table of Contents
1. Introduction  
   - 1.1 Purpose  
   - 1.2 Scope  
   - 1.3 Definitions, Acronyms, and Abbreviations  
   - 1.4 References  
   - 1.5 Overview  
2. Overall Description  
   - 2.1 Product Perspective  
   - 2.2 Product Features  
   - 2.3 User Classes and Characteristics  
   - 2.4 Operating Environment  
   - 2.5 Design and Implementation Constraints  
   - 2.6 Assumptions and Dependencies  
3. System Features  
   - 3.1 Registration and User Profile Management  
   - 3.2 Course Enrollment Management  
   - 3.3 Waitlist Management  
   - 3.4 Course Availability and Scheduling  
4. External Interface Requirements  
   - 4.1 User Interfaces  
   - 4.2 Hardware Interfaces  
   - 4.3 Software Interfaces  
5. Other Nonfunctional Requirements  
   - 5.1 Security  
   - 5.2 Performance  
   - 5.3 Scalability  
6. Appendices
  - 6.1 Github Screenshots

1. Introduction

1.1 Purpose
The purpose of this Software Requirements Specification (SRS) document is to define the functional and nonfunctional requirements for an online course management system. This system will allow users to register, create unique profiles, enroll in courses, manage enrollments, and interact with course waitlists for fully enrolled courses. The system aims to streamline course registration and management processes while ensuring data integrity and operational efficiency.

1.2 Scope
The online course management system will enable:  
User Registration: Users will create unique accounts to access the platform.  
Profile Management: Users can input and update their details, such as name, phone, and email.  
Course Enrollment: Users will select and enroll in available courses for specific semesters: Spring, Summer, or Fall.  
Waitlist Feature: If a course is full, users can add themselves to a waitlist. When a seat becomes available, the first person in the queue will be automatically notified and enrolled.  
Enrollment Cancellation: Users can cancel their course enrollment, which automatically updates the waiting list.  

The system will also allow administrators to configure course schedules and enrollment capacities for different semesters.

1.3 Definitions, Acronyms, and Abbreviations  
ID: A unique identifier generated for every user during account registration.  
SRS: Software Requirements Specification.  
Semester: Defined as one of three academic terms: Spring, Summer, or Fall.  
Enrollment Limit: The maximum number of allowed registrations for a course.  

1.4 References  
1. IEEE Standards Association, "Recommended Practice for Software Requirements Specifications."  
2. UML Documentation Guidelines for software design documentation.  

1.5 Overview  
This SRS document includes details about the system features, user interface requirements, functional and nonfunctional requirements, and operational assumptions. It serves as a guide for developers and stakeholders to ensure alignment about the system's expected behavior and constraints.

---

2. Overall Description

2.1 Product Perspective  
The course management system will replace traditional, manually operated registration processes with an automated digital platform. It will provide seamless access to course offerings, automated waitlist management, and administrative control over course schedules and enrollment capacities.

2.2 Product Features  
User Registration: New users can create unique accounts with an ID and password.  
User Profile Management: Users can enter and edit personal information such as name, phone, and email.  
Course Directory: Users can view the list of courses offered per semester (Spring, Summer, and Fall).  
Enrollment Management: Users can select and enroll in courses, with seat capacities enforced.  
Waitlist System: Handles full courses by creating queue-based reservations.  
Enrollment Cancellation: Allows cancellations and allocates seats to waitlisted users.  

2.3 User Classes and Characteristics  
Student Users: Individuals who will register for courses and manage their enrollments. Typically, they are expected to have basic digital literacy.  
Administrators: Responsible for maintaining the course catalog, managing enrollment capacities, and auditing course registers.  

2.4 Operating Environment  
The system will be developed as a web application accessible via modern web browsers (e.g., Chrome, Firefox, Safari).  
Supported on desktop and mobile devices with internet access.  

2.5 Design and Implementation Constraints  
Every user must be associated with a unique ID to ensure account uniqueness. The system must validate new IDs during registration.  
Each course will have a configurable enrollment cap (different limits for different courses).  
The waitlist and enrollment processes must execute automatically when a seat opens.  

2.6 Assumptions and Dependencies  
Users will provide valid contact details (email and phone) during registration to enable functionality like account recovery and notifications.  
The course catalog and semester schedules will be pre-approved and managed by administrators.  

---

3. System Features

3.1 Registration and User Profile Management  
3.1.1 Description and Priority  
Users can register and create an ID with a password to access the system. This feature is a high priority since it allows access to all other system features.  

3.1.2 Functional Requirements  
The system must allow users to create unique IDs and prevent duplicate registrations.  
The system must allow users to update their profiles, including name, email, and phone number.  
Login functionality must securely validate the ID and password of users.

3.2 Course Enrollment Management  
3.2.1 Description and Priority  
Enables users to view available courses and enroll in them. Courses have a maximum capacity, and this feature is a medium-to-high priority.  

3.2.2 Functional Requirements  
The system must display all courses available for each semester.  
The system must enforce maximum enrollment limits for courses.  
Users can view their active course enrollments at any time.  

3.3 Waitlist Management  
3.3.1 Description and Priority  
Manages a queue for full courses and ensures available seats are allocated fairly. This functionality is medium priority.  

3.3.2 Functional Requirements  
The system must allow users to add themselves to a waiting list for full courses.  
The system must automatically notify the next in line when a seat becomes available.  
The system must auto-enroll a user from the waitlist if they confirm availability or allow decline if they are unavailable.  

3.4 Course Availability and Scheduling  
3.4.1 Description and Priority  
Lists available courses for semesters and facilitates enrollment. This is high priority as it is core functionality.  

3.4.2 Functional Requirements  
The system must categorize courses by semester.  
Administrators must be able to update course offerings and their availability by term.  

---

4. External Interface Requirements

4.1 User Interfaces  
Web-based UI accessible via browsers with intuitive design for course search, registration, and profile management.  

4.2 Hardware Interfaces  
Supports desktops, laptops, tablets, and smartphones with internet access.  

4.3 Software Interfaces  
Integrates with email APIs for notifications and alerts for enrollment updates.  

---

5. Other Nonfunctional Requirements

5.1 Security  
Password encryption to protect sensitive data.  

5.2 Performance  
The system should process enrollment and waitlist changes within 5 seconds.  

5.3 Scalability  
Supports up to 10,000 concurrent users during peak registration times. 

