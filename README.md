# 🔐 Node.js Authentication System with Passport.js

> A full-stack authentication application featuring secure user registration, login, session management, and protected routes using industry-standard security practices.

[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Node.js](https://img.shields.io/badge/Node.js-43853D?style=flat&logo=node.js&logoColor=white)](https://nodejs.org/)
[![Express.js](https://img.shields.io/badge/Express.js-404D59?style=flat)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=flat&logo=mongodb&logoColor=white)](https://www.mongodb.com/)

## 📋 Table of Contents
- [Overview](#overview)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Screenshots](#screenshots)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Security Features](#security-features)
- [What I Learned](#what-i-learned)
- [Future Enhancements](#future-enhancements)

## 🎯 Overview

This project demonstrates my ability to build secure, production-ready authentication systems. I developed this full-stack web application to showcase fundamental software engineering skills including:
- **Backend Development**: RESTful API design with Express.js
- **Database Management**: MongoDB integration with Mongoose ODM
- **Security Implementation**: Password hashing, session management, and route protection
- **Full-Stack Integration**: Server-side rendering with EJS templating
- **DevOps**: Docker containerization for consistent development environments

Built as part of my portfolio to demonstrate proficiency in Node.js backend development and secure authentication workflows.

## ✨ Key Features

### Authentication & Authorization
- ✅ **User Registration** with email validation and password strength requirements
- ✅ **Secure Login System** using Passport.js local strategy
- ✅ **Password Encryption** with bcrypt hashing algorithm (10 salt rounds)
- ✅ **Session Management** with express-session and MongoDB store
- ✅ **Protected Routes** with authentication middleware
- ✅ **Logout Functionality** with proper session destruction

### Technical Implementation
- ✅ **RESTful API Design** following best practices
- ✅ **MVC Architecture** for organized code structure
- ✅ **MongoDB Integration** with Mongoose ODM for data persistence
- ✅ **Docker Support** for easy development setup and deployment
- ✅ **EJS Templating** for dynamic server-side rendering
- ✅ **Input Validation** to prevent malicious data
- ✅ **Error Handling** with user-friendly flash messages

## 🛠️ Tech Stack

### Backend
- **Node.js** - JavaScript runtime environment
- **Express.js** - Web application framework
- **Passport.js** - Authentication middleware
- **Mongoose** - MongoDB object modeling

### Database
- **MongoDB** - NoSQL document database
- **Docker** - Containerized MongoDB instance

### Security
- **bcrypt.js** - Password hashing library
- **express-session** - Session middleware
- **connect-flash** - Flash message middleware

### Frontend
- **EJS** - Embedded JavaScript templating
- **CSS3** - Custom styling

## 📸 Screenshots

### Home Page
![Home](https://github.com/user-attachments/assets/d221db76-b3af-47eb-94da-20566ad371b1)

### Login Interface
![Login](https://github.com/user-attachments/assets/53b1f6d9-b68b-4ea1-ad9d-d970be9d9e821)

### Registration Form
![Register](https://github.com/user-attachments/assets/0bfbba50-3818-4c87-8790-838627ab2617)

## 🚀 Installation

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local installation or Docker)
- npm or yarn package manager

### Setup Instructions

1. **Clone the repository**
```bash
git clone https://github.com/GeroJun/Passport_Login_Application.git
cd Passport_Login_Application
```

2. **Install dependencies**
```bash
npm install
```

3. **Set up MongoDB with Docker (recommended)**
```bash
# Pull and run MongoDB container
docker run -d -p 27017:27017 --name mongodb mongo:latest

# Verify MongoDB is running
docker ps
```

4. **Configure environment variables** (optional)
```bash
# Create .env file
touch .env

# Add your configuration
PORT=5000
MONGODB_URI=mongodb://localhost:27017/passport-auth
SESSION_SECRET=your_secret_key_here
```

5. **Start the application**
```bash
# Development mode with nodemon
npm run dev

# Production mode
npm start
```

6. **Access the application**
   - Open your browser and navigate to `http://localhost:5000`

## 💡 Usage

### Creating an Account
1. Click the "Register" button on the home page
2. Enter your name, email, and password
3. Confirm your password
4. Submit the form to create your account
5. You'll be automatically redirected to the dashboard

### Logging In
1. Click the "Login" button
2. Enter your registered email and password
3. Access your protected dashboard upon successful authentication

### Protected Routes
- `/dashboard` - Only accessible when logged in
- Automatic redirects to login page for unauthorized access attempts

## 📁 Project Structure

```
Passport_Login_Application/
├── config/
│   └── passport.js          # Passport.js configuration & strategies
├── models/
│   └── User.js              # Mongoose User schema
├── routes/
│   ├── index.js             # Public routes (home, login, register)
│   └── users.js             # Authentication routes
├── views/
│   ├── layout.ejs           # Base template
│   ├── welcome.ejs          # Landing page
│   ├── login.ejs            # Login form
│   ├── register.ejs         # Registration form
│   └── dashboard.ejs        # Protected user dashboard
├── app.js                   # Express app configuration
├── package.json             # Project dependencies
└── README.md               # Documentation
```

## 🔒 Security Features

This project implements multiple layers of security:

### Password Security
- **Bcrypt Hashing**: Passwords are hashed with 10 salt rounds before storage
- **Never Store Plain Text**: Original passwords are never saved to the database
- **Password Confirmation**: Validates matching passwords during registration

### Session Management
- **Secure Sessions**: HTTP-only session cookies prevent XSS attacks
- **Session Store**: Sessions persisted in MongoDB for scalability
- **Automatic Expiration**: Sessions expire after period of inactivity

### Route Protection
- **Authentication Middleware**: Prevents unauthorized access to protected routes
- **Automatic Redirects**: Unauthenticated users redirected to login
- **Flash Messages**: User-friendly error and success notifications

### Input Validation
- **Email Validation**: Ensures valid email format
- **Password Requirements**: Enforces minimum security standards
- **Sanitization**: Prevents malicious input injection

## 📚 What I Learned

Developing this project strengthened my skills in:

### Backend Development
- Implementing secure authentication flows with Passport.js strategies
- Designing RESTful APIs with Express.js middleware
- Managing asynchronous operations with async/await patterns
- Structuring Node.js applications using MVC architecture

### Database Management
- MongoDB schema design with Mongoose
- CRUD operations and data validation
- Database indexing for query optimization
- Docker containerization for database deployment

### Security Best Practices
- Password hashing and salting techniques
- Session-based authentication vs token-based authentication
- Protecting against common vulnerabilities (XSS, CSRF, SQL injection)
- Implementing authorization and access control

### Software Engineering
- Version control with Git and GitHub
- Code organization and modular design
- Error handling and logging strategies
- Documentation and README best practices

## 🚀 Future Enhancements

Planned improvements to expand functionality:

- [ ] **OAuth Integration** - Add social login (Google, GitHub, LinkedIn)
- [ ] **JWT Authentication** - Implement token-based auth for mobile/SPA
- [ ] **Email Verification** - Send confirmation emails via SendGrid/Mailgun
- [ ] **Password Reset** - Forgot password functionality with email tokens
- [ ] **Two-Factor Authentication** - SMS/authenticator app 2FA
- [ ] **Rate Limiting** - Prevent brute force attacks on login endpoints
- [ ] **Password Strength Meter** - Visual feedback during registration
- [ ] **Account Settings** - Allow users to update profile information
- [ ] **Remember Me** - Persistent login functionality
- [ ] **Audit Logging** - Track authentication events and suspicious activity
- [ ] **Admin Dashboard** - User management interface
- [ ] **API Documentation** - Swagger/OpenAPI specification
- [ ] **Unit & Integration Tests** - Jest/Mocha test coverage
- [ ] **CI/CD Pipeline** - Automated testing and deployment

## 👤 Author

**Victor (Gero) Jun**
- 🎓 Computer Science Student | Azusa Pacific University
- 💼 Software Engineer Intern
- 🔗 [LinkedIn](https://www.linkedin.com/in/gerojun)
- 🐱 [GitHub](https://github.com/GeroJun)

## 📝 License

This project is open source and available for educational purposes.

---

⭐ **If you found this project helpful, please consider giving it a star!**

*Built with ❤️ as part of my software engineering portfolio*
