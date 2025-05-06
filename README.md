# AirBnB Clone Project

This project is a simplified clone of the AirBnB web application.

## 📌 Project Goals

- Recreate key features of the AirBnB platform
- Practice backend and frontend integration
- Learn and apply OOP, database management, and web development principles

## 🛠 Tech Stack

- Python
- Flask
- HTML/CSS
- JavaScript
- SQLAlchemy / MySQL

## 👥 Team Roles

Here is a breakdown of the different roles within our AirBnB Clone project team and their responsibilities:

### 🔧 Backend Developer
Responsible for building the server-side logic of the application, APIs, and integrating the frontend with the database. Ensures the application runs smoothly behind the scenes.

### 🗄️ Database Administrator (DBA)
Manages the database structure and ensures data is properly stored, backed up, and optimized. Responsible for writing efficient SQL queries and maintaining data security.

### 🎨 Frontend Developer
Handles the user interface and user experience of the application. Implements designs using HTML, CSS, and JavaScript, ensuring that the application is responsive and accessible.

### 🧪 QA Tester
Tests the application to identify bugs, usability issues, and performance problems. Ensures the final product is stable and functions as intended.

### 📂 Project Manager
Coordinates the project timeline, resources, and team members. Ensures communication between all roles and keeps the project on track to meet deadlines.

### 📦 DevOps Engineer
Responsible for deployment, continuous integration/delivery, and managing infrastructure. Ensures that the application can be efficiently deployed and scaled.

## 🛠 Technology Stack

This project uses the following technologies:

### 🌐 Django
A high-level Python web framework that allows rapid development of secure and maintainable websites. It handles URL routing, user authentication, and provides tools for building RESTful APIs.

### 🗄️ PostgreSQL
A powerful, open-source relational database system used to store and manage application data. It works seamlessly with Django through the ORM (Object-Relational Mapping).

### 🔍 GraphQL
A query language for your API, and a runtime for executing those queries with your existing data. It provides a more efficient and flexible alternative to REST.

### 🖥️ HTML/CSS/JavaScript
Used for building the frontend interface of the application. HTML structures the content, CSS styles it, and JavaScript adds interactivity.

### 🐳 Docker *(optional)*
Used to containerize the application, making it easier to deploy and run in any environment.

### 🌍 Git & GitHub
Git is used for version control, while GitHub hosts the repository and facilitates collaboration.

## 🗃️ Database Design

The database for the AirBnB Clone project is structured around several key entities:

### 👤 Users
Represents the users of the platform.
- `id` (primary key)
- `name`
- `email`
- `password_hash`
- `role` (e.g., guest, host)

➡️ **Relationships**:
- A user can own multiple properties.
- A user can make multiple bookings.
- A user can write multiple reviews.

---

### 🏡 Properties
Represents listings available for booking.
- `id` (primary key)
- `title`
- `description`
- `location`
- `price_per_night`
- `owner_id` (foreign key to Users)

➡️ **Relationships**:
- A property belongs to a user (host).
- A property can have multiple bookings and reviews.

---

### 📅 Bookings
Represents reservations made by users.
- `id` (primary key)
- `user_id` (foreign key)
- `property_id` (foreign key)
- `start_date`
- `end_date`
- `total_price`

➡️ **Relationships**:
- A booking belongs to a user and a property.

---

### ✍️ Reviews
Represents feedback left by users for properties.
- `id` (primary key)
- `user_id` (foreign key)
- `property_id` (foreign key)
- `rating` (e.g., 1–5)
- `comment`

➡️ **Relationships**:
- A review belongs to a user and a property.

---

### 💳 Payments
Represents payments for bookings.
- `id` (primary key)
- `booking_id` (foreign key)
- `amount`
- `payment_date`
- `status` (e.g., pending, completed)

➡️ **Relationships**:
- A payment is linked to a specific booking.

## 🚀 Feature Breakdown

Below are the main features included in the Airbnb Clone project, designed to replicate core functionality of the original Airbnb platform.

### 👤 User Management
Users can register, log in, and manage their profiles. This feature includes authentication and authorization, ensuring data security and personalized access.

### 🏘️ Property Management
Hosts can list new properties, update property details, and manage availability. This allows users to showcase accommodations and control their listings.

### 📅 Booking System
Guests can book available properties for specific dates. The system handles availability checks, booking confirmation, and total cost calculations.

### 💳 Payment Integration
The platform supports secure payment processing for bookings. Users can pay using supported methods and view their transaction history.

### ✍️ Review System
Users can leave reviews and ratings after their stay. This builds trust within the community and helps future guests make informed decisions.

### 🔍 Property Search & Filtering
Guests can search for properties based on location, price range, and other criteria. This improves user experience and helps them find the right stay quickly.

### 📈 Admin Dashboard *(optional)*
An interface for admins to manage users, properties, and transactions. It provides insights and allows moderation when needed.

## 🔐 API Security

Securing the backend APIs is a critical component of the Airbnb Clone project. The following measures are implemented to ensure the safety of user data and the integrity of the platform:

### ✅ Authentication
Only registered users can access certain endpoints. Token-based authentication (e.g., JWT) ensures that each request is from a verified user.

**Why it matters**: Prevents unauthorized access to personal and sensitive data.

---

### ✅ Authorization
Role-based access control ensures that users only perform actions permitted to their role (e.g., hosts can create listings, guests can book).

**Why it matters**: Prevents users from accessing or modifying data they shouldn't.

---

### ✅ Rate Limiting
Limits the number of requests a user or IP can make within a time frame to prevent abuse and denial-of-service attacks.

**Why it matters**: Protects the server from overload and malicious activity.

---

### ✅ Input Validation & Sanitization
All inputs from users are validated and sanitized to prevent SQL injection and other attacks.

**Why it matters**: Ensures database integrity and prevents security breaches.

---

### ✅ HTTPS/SSL
All communications between clients and the server are encrypted using HTTPS.

**Why it matters**: Protects data in transit, especially sensitive information like login credentials and payment details.

## 🔄 CI/CD Pipeline

CI/CD (Continuous Integration and Continuous Deployment) pipelines automate the process of building, testing, and deploying code. They help ensure that changes pushed to the repository are automatically validated and deployed with minimal human intervention.

### 📌 Why CI/CD is Important:
- Ensures code quality by running automated tests before deployment.
- Speeds up the development process with automatic builds and deployments.
- Reduces human error and increases reliability of deployments.
- Enables faster feedback and more agile development workflows.

### 🛠️ Tools Used:
- **GitHub Actions**: Automates workflows directly from the GitHub repository (e.g., run tests, lint code, deploy on push).
- **Docker**: Ensures consistency across development, testing, and production environments by containerizing the application.
- **Heroku / AWS / Netlify** *(optional)*: For hosting and deployment depending on the tech stack.
