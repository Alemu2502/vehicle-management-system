# Vehicle Management System

This project is a Vehicle Management System built using MERN (MongoDB, Express, React, Node.js) stack. It includes user authentication, vehicle management functionalities, password reset features, and pagination for vehicle listings.

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [API Endpoints](#api-endpoints)
6. [Folder Structure](#folder-structure)
7. [Dependencies](#dependencies)
8. [Pagination Implementation](#pagination-implementation)

## Introduction

The Vehicle Management System is designed to manage vehicle records and includes features like user registration, authentication, password reset, and more. It is built using the MERN stack and follows best practices for coding and project structure.

## Features

- User Registration with email verification
- User Login
- Password Reset
- Vehicle Management (CRUD operations)
- Authentication and Authorization
- Responsive UI with React and Bootstrap
- Pagination for vehicle listings
#### Installation

### Follow these steps to set up the project locally:
- Clone the repository:
- git clone https://github.com/Alemu2502/vehicle-management-system.git
- cd vehicle-management-system

#### Install server dependencies:

cd server
npm install

#### Install client dependencies:

cd ../client
npm install

#### Set up environment variables: Create a .env file in the server directory and add the following:

bash
PORT=3000
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
REFRESH_TOKEN_SECRET=your_refresh_token_secret
EMAIL_VERIFICATION_SECRET=your_email_verification_secret
EMAIL_USER=your_email_user
EMAIL_PASS=your_email_pass
CLIENT_URL=http://localhost:3001
EMAIL_FROM=your_email_from_address
Run the server:

npm start
Run the client:

cd ../client

npm start

## Usage

**User Registration:** Users can register by providing their name, email, and password. An email verification link will be sent to their email.

**User Login:** Users can log in using their email and password. If the email is not verified, an appropriate message will be shown.

**Password Reset:** Users can reset their password by providing their registered email. They will receive a password reset link in their email.

## API Endpoints
#### via postman

#### Authentication
```POST /api/auth/register``` Register a new user.

```POST /api/auth/login```: Authenticate an existing user.
```POST /api/auth/userinfo```: get user info.
```POST /api/auth/request-password-reset```: Request a password reset link.
```POST /api/auth/reset-password/:token```: Reset the password using the token.
```GET /api/auth/verify-email/:token```: Verify the user's email.

#### Vehicle Management (Protected Routes)

```GET /api/vehicles/all```: Get all vehicles.
```POST /api/vehicles/add```: Add a new vehicle.
```PUT /api/vehicles/update/:id```: Update an existing vehicle.
```DELETE /api/vehicles/delete/:id```: Delete a vehicle.

## Folder Structure

vehicle-management-system/
  ├── client/                    # React front-end application
  │   ├── public/                # Public assets
  │   ├── src/                   # Source files
  │   │   ├── components/        # React components
  │   │   ├── helpers/           # Helper functions
  │   │   ├── services/          # Services
  │   │   ├── utility/           # Utility functions
  │   │   ├── setupTest.js       # Test setup file
  │   │   ├── app.tests.js       # Application tests
  │   │   ├── App.js             # Main App component
  │   │   └── index.js           # Entry point
  │   ├── .gitignore             # Git ignore file
  │   ├── package.json           # NPM dependencies and scripts
  │   ├── package-lock.json      # Lock file for npm dependencies
  │   └── .env                   # Environment variables
  ├── server/                    # Node.js back-end application
  │   ├── controllers/           # API route controllers
  │   ├── models/                # Database models
  │   ├── routes/                # API routes
  │   ├── utils/                 # Utility functions
  │   ├── config/                # Configuration files
  │   ├── middlewares/           # Middleware functions
  │   ├── server.js              # Server entry point
  │   ├── .gitignore             # Git ignore file
  │   ├── package.json           # NPM dependencies and scripts
  │   ├── package-lock.json      # Lock file for npm dependencies
  │   └── .env                   # Environment variables
  └── README.md                  # Project documentation


## Pagination Implementation
Pagination is implemented to manage large sets of vehicle data efficiently. 

#### Server

**express:** Fast, unopinionated, minimalist web framework for Node.js
**mongoose**: MongoDB object modeling for Node.js
**jsonwebtoken:** JSON Web Token implementation (JWT)
**bcryptjs:** Library to hash passwords
**nodemailer:** Send emails from Node.js
**dotenv:** Loads environment variables from a .env file

#### Client

**react:** JavaScript library for building user interfaces
**axios:** Promise-based HTTP client for the browser and Node.js
**react-router-dom:** DOM bindings for React Router
**bootstrap:** CSS framework for developing responsive and mobile-first websites
