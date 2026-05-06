# 🔐 Identity and Access Management (IAM) System

## 📌 Project Description

This project is a prototype Identity and Access Management (IAM) system designed to provide secure authentication and role-based access control for organizational systems.

The system centralizes user authentication, authorization, and access management to reduce security risks and administrative overhead.

---

## 📌 Project Scope

This project focuses on developing the core backend components of an Identity and Access Management (IAM) system, including API development, user management, and secure token-based communication.

The system is implemented as a functional prototype with essential capabilities.

Advanced features such as a full frontend interface, multi-factor authentication (MFA), and cloud deployment are considered future improvements and are not the primary focus of this stage, as the project is focused on demonstrating core IAM concepts within limited time and scope.

---

## ⚙️ System Flow (How It Works)

When a user interacts with the system, the request follows a structured flow:

- The user sends a request to the API (e.g., login or access a resource)
- The request is handled by Express routes
- The controller processes the request logic
- User credentials are verified using bcrypt
- If authentication is successful, a JSON Web Token (JWT) is generated
- The token is returned to the client
- For protected routes, the system verifies the JWT and extracts the user role
- The system checks permissions using Role-Based Access Control (RBAC)
- Access is granted or denied based on the user’s role
- All actions are recorded in the audit logs

This flow demonstrates how authentication, authorization, and security mechanisms work together in a centralized system.

---

## 🎯 Main Features

### 🔑 User Authentication
Secure login, registration, and password recovery.  
Passwords are hashed using bcrypt to ensure they are never stored in plain text.

### 🛡️ Role-Based Access Control (RBAC)
Assign roles (Admin, Manager, Employee) to control access to different resources.  
Each role defines what actions a user is allowed to perform.

### 🔐 Token-Based Security
Use JSON Web Tokens (JWT) for secure API access.  
After login, users receive a token that must be included in every request to access protected resources.

### 📊 Audit Logging
Track user actions such as login attempts, role changes, and access requests.  
This ensures accountability and supports compliance with standards like GDPR or HIPAA.

### 🔌 API Integration
Allow internal systems (e.g., payroll, project management tools, internal databases) to securely connect to the IAM system via API.

External systems can send requests with a JWT token to verify user identity and permissions before granting access to their resources.

This demonstrates how centralized authentication and authorization work in real-world enterprise environments.

### 👥 User Management
Provide a programmatic interface for administrators to add, modify, and revoke users.  
This simulates how organizations manage employee access to internal systems.

---

## 🛠️ Technology Plan

### Backend / API
- Node.js with Express

### Database
- PostgreSQL (via pgAdmin)

### Security
- JSON Web Tokens (JWT) for authentication  
- bcryptjs for password hashing  

### Environment Variables
- dotenv for secure configuration management

### Documentation
- API documentation provided in the project folder

---

## 🧾 Summary

This project demonstrates how a centralized IAM system can securely manage user authentication, authorization, and access control across multiple systems.

It highlights how organizations can reduce security risks, improve access management, and ensure proper control over user permissions using a structured backend architecture.

