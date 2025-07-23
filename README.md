# Team Roles

# This section outlines the key roles within the project team and their responsibilities, as adapted from the project overview and ITRexGroup's software development role structure.

# 

# Project Manager (PM)

# Responsible for planning, overseeing the project timeline, managing resources, ensuring effective communication among team members, and delivering the project on time and within budget.

# 

# Backend Developer

# Builds and maintains the server-side application logic. In this project, they are responsible for implementing APIs, business logic, authentication, and server-side integrations with the database.

# 

# Frontend Developer

# Creates the user interface and ensures a seamless user experience. They work closely with designers to implement UI components using HTML, CSS, JavaScript, and potentially frameworks like React or Vue.js.

# 

# Database Administrator (DBA)

# Designs, implements, and maintains the project’s database structure. Ensures data integrity, optimizes queries, and manages backups and recovery plans.

# 

# DevOps Engineer

# Manages infrastructure, deployment, CI/CD pipelines, and monitors the application. Ensures smooth development and deployment processes across environments.

# 

# UX/UI Designer

# Designs intuitive and engaging interfaces. Conducts user research, creates wireframes, prototypes, and collaborates with frontend developers to ensure the design is properly implemented.

# 

# QA Engineer / Tester

# Tests the application to find bugs and issues before release. Writes automated and manual test cases, ensuring functionality, performance, and security requirements are met.

# 

# Security Specialist

# Oversees the security of the application. Conducts vulnerability assessments, ensures secure authentication and data protection practices are followed.





\## Technology Stack



\### 1. Django

A high-level Python web framework used to build the backend logic of the application, including handling user requests, authentication, and serving data via RESTful APIs.



\### 2. PostgreSQL

An open-source relational database system used to store user data, property listings, bookings, and other structured data securely.



\### 3. HTML, CSS, JavaScript

Used to build the frontend of the web application. HTML structures the content, CSS styles it, and JavaScript adds interactivity.



\### 4. Bootstrap

A frontend CSS framework that helps create responsive, mobile-friendly layouts quickly.



\### 5. Git \& GitHub

Version control system (Git) and hosting platform (GitHub) used for tracking changes in code and collaborating with the development team.



\### 6. Docker (if used)

Used to containerize the application, making it easier to deploy across different environments consistently.



\### 7. GraphQL (if used)

An API query language that allows the client to request only the data it needs, improving performance and flexibility compared to traditional REST APIs.





\## Database Design



This project uses a relational database to store and manage core data entities. Below are the key entities, their attributes, and relationships:



\### 1. Users

\- `id`: Unique identifier

\- `name`: Full name

\- `email`: Email address

\- `password\_hash`: Encrypted password

\- `role`: (e.g., guest, host)



🔁 \*\*Relationships\*\*:  

\- A user can own multiple properties  

\- A user can make multiple bookings  

\- A user can leave multiple reviews  



---



\### 2. Properties

\- `id`: Unique identifier

\- `title`: Property name or listing title

\- `description`: Detailed description

\- `location`: Address or geographic coordinates

\- `price\_per\_night`: Rate per night



🔁 \*\*Relationships\*\*:  

\- A property belongs to one user (host)  

\- A property can have multiple bookings  

\- A property can have multiple reviews  



---



\### 3. Bookings

\- `id`: Unique identifier

\- `user\_id`: Guest making the booking

\- `property\_id`: The property being booked

\- `check\_in\_date`: Start date

\- `check\_out\_date`: End date



🔁 \*\*Relationships\*\*:  

\- A booking is linked to one user (guest)  

\- A booking is linked to one property  



---



\### 4. Reviews

\- `id`: Unique identifier

\- `user\_id`: Reviewer (guest)

\- `property\_id`: Property being reviewed

\- `rating`: Numeric score

\- `comment`: Review message



🔁 \*\*Relationships\*\*:  

\- A review is written by a user for a property  

\- A property can have multiple reviews  



---



\### 5. Payments

\- `id`: Unique identifier

\- `user\_id`: Who made the payment

\- `booking\_id`: Related booking

\- `amount`: Total paid

\- `status`: (e.g., completed, pending)



🔁 \*\*Relationships\*\*:  

\- A payment is tied to a specific booking  

\- A payment is made by a user  



Feature Breakdown

🧑‍💼 User Management

Allows users to sign up, log in, and manage their profiles securely. This feature enables authentication and authorization, ensuring that users can access their own data and perform actions based on their role (guest or host).



🏠 Property Management

Hosts can list properties by uploading details such as photos, descriptions, pricing, and availability. This feature is essential for adding accommodations and managing listings on the platform.



📅 Booking System

Users can search for available properties and make reservations based on date and availability. This system handles booking logic, availability checks, and confirmation workflows.



💳 Payment Integration

Enables secure payment processing for bookings. This feature ensures that users can pay for stays using payment gateways, and hosts can receive payouts.



⭐ Review and Rating System

After completing a stay, guests can leave reviews and ratings. This helps maintain trust in the community and gives other users insight into the quality of listings and hosts.



🔍 Search and Filter

Allows users to search for properties using filters like location, price range, date, number of guests, and amenities. This makes it easier to find relevant listings based on preferences.



📊 Admin Dashboard

Provides administrative users with tools to monitor platform activity, manage users, and remove inappropriate listings or reviews. This ensures the overall health and safety of the application

