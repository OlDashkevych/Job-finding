# Job-finding
# Express.js Authentication App

This is a simple Express.js application for user authentication using email and password. The app uses MongoDB for data storage and is designed for deployment on [Render](https://render.com).

## Features

- User registration with email and password
- User login and JWT-based authentication
- Protected routes for authenticated users
- MongoDB for data persistence
- Deployment on Render

## Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MongoDB (Mongoose)
- **Authentication**: JWT, bcrypt
- **Deployment**: Render

## Prerequisites

Before you begin, ensure you have met the following requirements:

- **Node.js**: v14.x or higher
- **MongoDB**: Access to a MongoDB instance
- **Render Account**: For deployment

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Set Up Environment Variables

Create a `.env` file in the root directory with the following variables:

```plaintext
MONGO_URI=your_mongo_connection_string
JWT_SECRET=your_jwt_secret_key
PORT=5000
```

### 4. Start the Application

```bash
npm start
```

The application will be available at `http://localhost:5000`.

## Running the App

### Development Mode

To start the application in development mode with hot-reloading:

```bash
npm run dev
```

### Production Mode

To start the application in production mode:

```bash
npm start
```

## API Endpoints

### User Authentication

- **POST /register**
  - Registers a new user.
  - **Request body**: `{ "email": "user@example.com", "password": "yourpassword" }`

- **POST /login**
  - Logs in a user and returns a JWT.
  - **Request body**: `{ "email": "user@example.com", "password": "yourpassword" }`

### Protected Routes

- **GET /me**
  - Requires a valid JWT in the `Authorization` header.

## Environment Variables

The following environment variables are used in this project:

- `MONGO_URI`: Your MongoDB connection string.
- `JWT_SECRET`: Secret key used to sign JWTs.
- `PORT`: The port on which the server will run (default: 5000).

## Deployment

### Deploy on Render

To deploy the application on Render:

1. **Connect Repository**: Go to [Render](https://dashboard.render.com/), create a new web service, and connect your GitHub repository.
2. **Set Environment Variables**: In Render's environment settings, add `MONGO_URI`, `JWT_SECRET`, and `PORT`.
3. **Deploy**: Render will automatically build and deploy your application.
