# API Documentation for SecureAuth

## Table of Contents
1. [Base URL](#base-url)
2. [Authentication](#authentication)
3. [API Endpoints](#api-endpoints)
    - [Sign Up](#sign-up)
    - [Verify Email](#verify-email)
    - [Login](#login)
    - [Logout](#logout)
4. [Error Handling](#error-handling)
5. [Contact](#contact)

---

## Base URL
```
http://localhost:5000/api/auth
```

## Authentication
All API requests require authentication via JWT tokens for protected routes. Upon successful login or signup, the server will generate a token, which should be included in the `Authorization` header of requests to protected routes.

**Authorization Header Format:**
```
Authorization: Bearer <token>
```

## API Endpoints

### Sign Up
- **Endpoint:** `/signup`
- **Method:** `POST`
- **Request Body:**
    ```json
    {
      "name": "Wanyoike Edwards",
      "email": "markeddy254@gmail.com",
      "password": "123456"
    }
    ```
- **Response:**
    - **Success (201):**
    ```json
    {
      "success": true,
      "message": "User created successfully",
      "user": {
        "email": "markeddy254@gmail.com",
        "name": "Wanyoike Edwards",
        ...
      }
    }
    ```
    - **Failure (400):**
    ```json
    {
      "success": false,
      "message": "User already exists"
    }
    ```

### Verify Email
- **Endpoint:** `/verify-email`
- **Method:** `POST`
- **Request Body:**
    ```json
    {
      "code": "123456"
    }
    ```
- **Response:**
    - **Success (200):**
    ```json
    {
      "success": true,
      "message": "Email verified successfully",
      "user": {
        ...
      }
    }
    ```
    - **Failure (400):**
    ```json
    {
      "success": false,
      "message": "Invalid or expired verification code"
    }
    ```

### Login
- **Endpoint:** `/login`
- **Method:** `POST`
- **Request Body:**
    ```json
    {
      "email": "markeddy254@gmail.com",
      "password": "123456"
    }
    ```
- **Response:**
    - **Success (200):**
    ```json
    {
      "success": true,
      "message": "Login successful",
      "token": "<JWT_TOKEN>"
    }
    ```
    - **Failure (401):**
    ```json
    {
      "success": false,
      "message": "Invalid credentials"
    }
    ```

### Logout
- **Endpoint:** `/logout`
- **Method:** `POST`
- **Response:**
    - **Success (200):**
    ```json
    {
      "success": true,
      "message": "Logout successful"
    }
    ```

## Error Handling
- All endpoints will return appropriate HTTP status codes based on the outcome of the request.
- Common error codes:
    - `400 Bad Request`: Invalid request body or parameters.
    - `401 Unauthorized`: Missing or invalid authentication token.
    - `404 Not Found`: Endpoint not found.
    - `500 Internal Server Error`: Server error.

## Contact
For support or inquiries, please reach out to:
- **Name:** Wanyoike Edwards
- **Email:** markeddy254@gmail.com
