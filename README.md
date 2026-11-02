# Complete-Student-Management-System-new

# Backend Tutorial: Node.js, Express.js and MongoDB

A beginner-friendly REST API project demonstrating CRUD operations with Node.js, Express, MongoDB Atlas and Mongoose.

## Features

- Create a student
- Retrieve all students
- Retrieve one student by ID
- Update a student
- Delete a student
- Basic health-check endpoint
- Input validation through a Mongoose schema

## Technologies

- Node.js
- Express.js
- MongoDB Atlas
- Mongoose
- Postman

## Project structure
├── controllers/
│   └── studentController.js
├── models/
│   └── studentModel.js
├── routes/
│   └── studentRoutes.js
├── .env.example
├── .gitignore
├── package.json
├── README.md
└── server.js

## Setup

1. Install Node.js (LTS).
2. Clone or download this repository.
3. Install dependencies:

   ```bash
   npm install
   ```

4. Create a file named `.env` in the project root. Copy the contents of `.env.example` into it and replace the placeholder `MONGODB_URI` with your own MongoDB Atlas connection string.
5. In MongoDB Atlas, create a database user and allow your current IP address in Network Access. Keep your database password private.
6. Start the app:

   ```bash
   npm start
   ```

   For development with automatic restarts:

   ```bash
   npm run dev
   ```
