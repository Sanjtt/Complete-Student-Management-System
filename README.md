# Complete-Student-Management-System-new

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
```text
.
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
```

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
   7. Open `http://localhost:3000` in a browser. You should see a JSON message if the database connection succeeds.

## API endpoints

Base URL: `http://localhost:3000`

| Method | Endpoint | Purpose |
| --- | --- | --- |
| GET | `/` | API welcome message |
| GET | `/health` | Health check |
| POST | `/api/students` | Create a student |
| GET | `/api/students` | Get all students |
| GET | `/api/students/:id` | Get a student by ID |
| PUT | `/api/students/:id` | Update a student |
| DELETE | `/api/students/:id` | Delete a student |

### Example POST body

Send this JSON in Postman to `POST http://localhost:3000/api/students`:

```json
{
  "name": "Rahul Sharma",
  "email": "rahul@example.com",
  "course": "B.Tech CSE",
  "year": 2
}
```

Use the `_id` returned in the response when testing GET-by-ID, PUT, and DELETE.

## Postman testing

For POST and PUT requests, select **Body → raw → JSON** and provide a valid JSON body. Test GET requests first, then use the `_id` returned from the create request to test the individual-record endpoints.

## Security notes

- Do not commit your `.env` file or publish database credentials.
- `.env.example` contains only a placeholder and is safe to commit.
- Do not share your MongoDB password publicly.

## Learning objectives

This project demonstrates Express routing, controller functions, a Mongoose model, MongoDB connectivity, and the four CRUD operations. Review the code and test the endpoints before presenting the project.

