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
