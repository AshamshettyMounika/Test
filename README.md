# Test Project – Frontend Enhancements and Backend Authentication

This project includes both frontend UI improvements and the implementation of a backend authentication system.

Frontend Changes:
The following UI changes were implemented in the existing project:
• Updated the product rating stars color to yellow.
• Modified the product layout to display items in 3 columns instead of 4.
• Changed the cursor style to a custom cursor instead of the default circular cursor.
• Added a hover animation on products where the image zooms in and a light grey mask appears from top to bottom.

Backend Authentication:
A backend authentication system was implemented using Node.js, Express, MongoDB Atlas, JWT, and bcrypt.

Features implemented:
• User registration API
• User login API
• Password hashing using bcrypt for security
• JWT token generation for authentication
• Authentication middleware to protect routes
• MongoDB Atlas database integration

Backend Structure:
src/backend/
middleware/authMiddleware.js – JWT authentication middleware
models/User.js – User schema for MongoDB
routes/auth.js – Register and login API routes
server.js – Express server configuration

Authentication API Endpoints:

Register User
POST /api/auth/register

Example request body:
{
"name": "User",
"email": "user@email.com",
"password": "123456"
}

Login User
POST /api/auth/login

Example request body:
{
"email": "user@email.com",
"password": "123456"
}

Example response:
{
"token": "JWT_TOKEN",
"user": {
"_id": "user_id",
"name": "User",
"email": "user@email.com"
}
}

Tech Stack Used:
Frontend: React, Tailwind CSS, JavaScript
Backend: Node.js, Express, MongoDB Atlas, JWT, bcrypt

Running the Project:

Install frontend dependencies:
npm install

Run frontend:
npm run dev

Run backend server:
cd src/backend
npm install
node server.js

Backend server runs on:
http://localhost:5000

Environment variables such as MongoDB URI and JWT secret are stored in the .env file and excluded from GitHub using .gitignore.
