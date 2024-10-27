<h1 align="center">MERN-SECURE-AUTHENTICATION 🔒 </h1>

[Website link](https://mern-secure-authentication.onrender.com)

## 📚 Comprehensive Documentation

### 🔐 System Overview
A robust MERN stack authentication system implementing industry-standard security practices with features like JWT authentication, email verification, and password reset functionality.

### 🛠️ Tech Stack
- MongoDB: Database management
- Express.js: Backend framework
- React.js: Frontend library
- Node.js: Runtime environment
- Redux: State management
- JWT: Authentication tokens
- Bcrypt: Password hashing


### 📂 Project Structure

#### Frontend Architecture
  
  - **src/**
    - **components/** 🌐 _Reusable UI Components_
      - **Auth/**
        - `Login.jsx`
        - `Register.jsx`
        - `ResetPassword.jsx`
      - **Common/**
        - `Navbar.jsx`
        - `Footer.jsx`
    - **pages/** 🗂️ _Application Pages_
      - `HomePage.jsx`
      - `DashboardPage.jsx`
      - `ProfilePage.jsx`
    - **redux/** 🗄️ _State Management_
      - `store.js`
      - **slices/**
        - `authSlice.js`
        - `userSlice.js`
      - **actions/**
    - **utils/** 🔧 _Helper Functions_
      - `authUtils.js`
      - `validators.js`
      - `apiService.js`
    - `App.js` 📌 _Root Component_
</details>

#### Backend Architecture
<details>
<summary><strong>backend/</strong></summary>
  
  - **controllers/** 🎛️ _Request Handlers_
    - `authController.js`
    - `userController.js`
  - **middleware/** 🔒 _Custom Middleware_
    - `authMiddleware.js`
    - `validator.js`
    - `errorHandler.js`
  - **models/** 🗃️ _Database Schemas_
    - `userModel.js`
    - `tokenModel.js`
  - **routes/** 🛣️ _API Routes_
    - `authRoutes.js`
    - `userRoutes.js`
  - **config/** ⚙️ _Configuration_
    - `database.js`
    - `mailer.js`
  - `server.js` 🚀 _Entry Point_
</details>


### 🔑 Key Features
- User Registration & Login
- Email Verification
- Password Reset Flow
- Protected Routes
- JWT Authentication
- Real-time Validation
- Responsive Design

### 🛣️ API Endpoints
- POST /api/auth/register - User registration
- POST /api/auth/login - User authentication
- POST /api/auth/verify - Email verification
- POST /api/auth/forgot-password - Password reset request
- PUT /api/auth/reset-password - Password update
- GET /api/auth/check - Authentication check

### 🔒 Security Implementation
- Password hashing with Bcrypt
- JWT token-based authentication
- HTTP-only cookies
- XSS protection
- Input sanitization
- Rate limiting

### 🗄️ Database Schema
```javascript
User {
    email: String,
    password: String,
    name: String,
    verified: Boolean,
    resetToken: String,
    createdAt: Date
}
```

About This Project:
🔧 Backend Setup
🗄️ Database Setup
🔐 Signup Endpoint
📧 Sending Verify Account Email
🔍 Verify Email Endpoint
📄 Building a Welcome Email Template
🚪 Logout Endpoint
🔑 Login Endpoint
🔄 Forgot Password Endpoint
🔁 Reset Password Endpoint
✔️ Check Auth Endpoint
🌐 Frontend Setup
📋 Signup Page UI
🔓 Login Page UI
✅ Email Verification Page UI
📤 Implementing Signup
📧 Implementing Email Verification
🔒 Protecting Our Routes
🔑 Implementing Login
🏠 Dashboard Page
🔄 Implementing Forgot Password
🚀 Super Detailed Deployment

🚀 Setup Instructions
Environment Variables (.env)

MONGO_URI=your_mongo_uri
PORT=5000
JWT_SECRET=your_secret_key
NODE_ENV=development
MAILTRAP_TOKEN=your_mailtrap_token
MAILTRAP_ENDPOINT=https://send.api.mailtrap.io/
CLIENT_URL= http://localhost:5173

Installation

# Build the app
npm run build

# Start the app
npm run start

🔄 Future Enhancements
Two-factor authentication
OAuth integration
Advanced user roles
Activity logging
Enhanced security features
🌟 Best Practices Implemented
Clean code architecture
Comprehensive error handling
Secure authentication flow
Efficient state management
Responsive design patterns
I'll see you in the next one! 🚀
