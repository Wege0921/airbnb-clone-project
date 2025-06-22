# 📌 Team Roles
Understanding the responsibilities of each team member ensures clear communication and effective collaboration. Below are the key roles within our project team
# 👨‍💻 Backend Developer
Responsibility:
Designs and implements the server-side logic, APIs, and core business logic. Ensures secure, scalable, and efficient backend functionality that powers the application.


# 🧰 Technology Stack
Below is an overview of the key technologies used in this project, along with their roles:

# ⚙️ Django
Purpose: A high-level Python web framework used for building scalable, secure, and maintainable web applications. In this project, Django serves as the backend framework for developing RESTful APIs and handling business logic.

# 🐘 PostgreSQL
Purpose: A powerful open-source relational database management system. Used in this project to store and manage structured data with strong support for advanced queries and data integrity.

# 🔍 GraphQL
Purpose: A query language for APIs that allows clients to request exactly the data they need. Used in this project for flexible and efficient client-server data interactions.

# 🎨 HTML/CSS/JavaScript
Purpose: Core web technologies for building the structure, style, and interactivity of the frontend user interface.

# 🌐 React (or another frontend framework, if applicable)
Purpose: A JavaScript library for building dynamic and interactive user interfaces. Used in this project to create a responsive frontend that communicates with the backend APIs.

# 🐳 Docker
Purpose: A containerization platform that packages the application and its dependencies into containers. Used for creating consistent development and deployment environments.

# ☁️ GitHub / Git
Purpose: Version control tools used to manage and track code changes, collaborate with team members, and maintain project history.

# 📦 Django REST Framework (DRF)
Purpose: A powerful toolkit built on top of Django for building Web APIs. Used in this project to simplify the creation of robust and customizable RESTful APIs.


# 🗄️ Database Design
This section outlines the key entities in the database and how they are related to one another.

# 👤 Users
Represents the individuals using the platform (both hosts and guests).
Key Fields:

id (Primary Key)

name

email

password_hash

role (e.g., host, guest)

# 🏠 Properties
Represents listings created by hosts.
Key Fields:

id (Primary Key)

title

description

location

price_per_night

owner_id (Foreign Key → Users)

# 📅 Bookings
Represents reservations made by guests for specific properties.
Key Fields:

id (Primary Key)

property_id (Foreign Key → Properties)

user_id (Foreign Key → Users)

start_date

end_date

# 📝 Reviews
Represents feedback from guests about a property.
Key Fields:

id (Primary Key)

user_id (Foreign Key → Users)

property_id (Foreign Key → Properties)

rating (1 to 5)

comment

# 💳 Payments
Tracks payment transactions related to bookings.
Key Fields:

id (Primary Key)

booking_id (Foreign Key → Bookings)

amount

payment_date

status (e.g., completed, pending, failed)

# 🔗 Entity Relationships
A User can own multiple Properties (one-to-many).

A User can make multiple Bookings (one-to-many).

A Property can have multiple Bookings (one-to-many).

A Booking is linked to one Payment (one-to-one).


# ✨ Feature Breakdown
This section provides an overview of the core features included in the Airbnb Clone project, explaining their roles and impact on the overall functionality.

# 👤 User Management
Allows users to register, log in, and manage their profiles. Supports role-based access (hosts and guests), enabling secure and personalized user experiences.

# 🏘️ Property Management
Enables hosts to list, update, and delete properties. Hosts can upload details such as title, description, location, price, and availability, making their spaces bookable.

# 📅 Booking System
Allows guests to browse available properties and make reservations for specific dates. It handles availability checking, conflict prevention, and links bookings to users and properties.

# 💳 Payment Integration
Facilitates secure payment processing for bookings. Guests can make payments through a simulated or real payment gateway, and all transactions are tracked and associated with bookings.

# 📝 Reviews and Ratings
Enables guests to leave feedback on properties they’ve stayed in. Reviews include comments and ratings, helping future guests make informed decisions and hosts improve their offerings.

# 🔎 Search and Filtering
Provides powerful tools for users to search for properties based on location, price, date, and other filters. This improves user experience and helps guests find the perfect stay quickly.

# 🔐 API Security
Security is a critical part of this project to protect user data and ensure safe communication between the client and server. Below are the key practices and tools used to secure the API:

Authentication & Authorization: Implemented using JWT (JSON Web Tokens) to control access to protected routes and resources.

HTTPS: Ensures all data exchanged between the client and server is encrypted.

Input Validation & Sanitization: All user inputs are validated and sanitized to prevent injection attacks.

Rate Limiting: Prevents abuse by limiting the number of requests a user can make in a certain time frame.

Error Handling: Generic error messages are used to avoid exposing sensitive implementation details.

# 🛠️ Admin Dashboard (Optional/Advanced)
A backend dashboard for site administrators to monitor users, properties, and transactions. This ensures the system is operating smoothly and helps with moderation and support.
A User can leave multiple Reviews, each for different Properties (one-to-many).

A Property can receive multiple Reviews (one-to-many).
