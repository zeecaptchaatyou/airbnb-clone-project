
🏠 AirBnB Clone Project

**Team Roles**
Team Member
Role/Responsibility
Zainab Jummah
Project Lead, Backend Developer
Each member of the team plays a unique role in ensuring smooth development and deployment of the project — from user interface creation to server logic, data persistence, and continuous integration.

**Technology Stack**
The AirBnB Clone Project  leverages a robust and scalable technology stack to ensure reliability, maintainability, and performance across all components of the system.
Category
Technology
Purpose
Programming Language
Python 3.8+
Core backend language
Web Framework
Flask
RESTful API development and routing
Frontend
HTML5, CSS3, JavaScript
Client-side rendering and interactivity
Database
MySQL / SQLAlchemy
Persistent data storage and ORM
Version Control
Git & GitHub
Source code management and collaboration
Testing
Unittest / Pytest
Automated testing framework
Deployment
Render / Railway / Docker
Application hosting and containerization
CI/CD
GitHub Actions
Automated testing and deployment pipeline
Security
JWT / HTTPS / Flask-Login
Authentication, authorization, and secure communication

This stack provides flexibility and modularity, ensuring the system can evolve easily while maintaining code quality and efficiency.

**Database Design**
The database architecture follows a relational model to handle relationships between users, properties, reviews, and locations efficiently.
🧱 Entity Relationship Model (ERM)
The system consists of the following key entities:
Entity
Attributes
Relationships
User
id, name, email, password
1-to-many with Place, 1-to-many with Review
Place
id, name, description, city_id, user_id
many-to-1 with City, many-to-1 with User
City
id, name, state_id
1-to-many with Place
State
id, name
1-to-many with City
Review
id, text, user_id, place_id
many-to-1 with User, many-to-1 with Place
Amenity
id, name
many-to-many with Place

The database supports two storage modes:
FileStorage (JSON) — used for development and local testing.


DBStorage (MySQL) — used for production environments.



Feature Breakdown
The project implements a modular architecture where each component focuses on a specific function of the Airbnb system.
Feature
Description
User Management
Registration, login, logout, and profile editing
Property Management
Add, update, or delete listings (Places)
Search & Filtering
Filter properties by location, amenities, and price
Booking System
Reserve and manage accommodation dates
Review System
Users can review and rate their stays
Admin Dashboard
Manage users, properties, and reports
API Endpoints
RESTful API for frontend and external integrations

Each feature is implemented with scalability and security in mind, following RESTful conventions and adhering to ALX software design standards.

API Security
Security is a top priority in the AirBnB Clone Project. The following measures ensure data integrity and safe interactions between clients and servers:
Authentication: Implemented using JWT tokens and Flask-Login for session management.


Authorization: Role-based access control to restrict actions to specific users.


Data Encryption: Sensitive user data (passwords) hashed using bcrypt.


HTTPS Protocol: All communications secured using SSL certificates.


Input Validation: Prevents SQL Injection and XSS attacks.


CORS Configuration: Restricts access to trusted domains only.


Example of protected route in Flask:
@app.route('/api/v1/users', methods=['GET'])
@jwt_required()
def get_users():
    current_user = get_jwt_identity()
    return jsonify({"user": current_user}), 200


CI/CD Pipeline
The Continuous Integration and Continuous Deployment (CI/CD) pipeline automates code testing, building, and deployment.
⚙️ Tools Used:
GitHub Actions: Automates testing and deployment.


Docker: Containerizes the app for consistency across environments.


Render / Railway: Deploys the containerized application.


pytest & flake8: Run automatically on every push or pull request.


🧩 Workflow:
Code Commit: Developers push code to the main branch.


Automated Testing: Unit tests and style checks run automatically.


Build Stage: Docker builds the application image.


Deployment: If tests pass, deployment occurs automatically to staging or production servers.


Notifications: Developers receive CI/CD status via GitHub notifications.


This ensures code quality, eliminates manual deployment errors, and maintains a continuous integration process for a stable production environment.



