# Blog Application

This is a full-stack blog application that allows users to create, read, update, and delete blog posts. It features user authentication and a responsive user interface.

## Features

*   User registration and login
*   Create new blog posts with a rich text editor
*   View all blog posts
*   View blog posts created by a specific user
*   Edit and delete user's own blog posts
*   Responsive design for various screen sizes

## Setup and Installation

Follow these steps to get the project running on your local machine.

### Prerequisites

*   Node.js (v14 or later recommended)
*   npm (usually comes with Node.js)
*   MongoDB (Make sure your MongoDB server is running)

### Backend Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/blog-app.git
    cd blog-app
    ```
2.  **Install backend dependencies:**
    ```bash
    npm install
    ```
3.  **Environment Variables:**
    Create a `.env` file in the root directory of the project and add the following environment variables. Replace the placeholder values with your actual configuration.
    ```env
    PORT=8080
    MONGO_URL=mongodb://localhost:27017/blog-app
    JWT_SECRET=yourjwtsecretkey
    ```
    *Note: You can change `MONGO_URL` if your MongoDB instance is running elsewhere. `JWT_SECRET` should be a strong, unique key.*

4.  **Run the backend server:**
    ```bash
    npm run server
    ```
    The backend server should now be running on `http://localhost:8080` (or the port you specified).

### Frontend Setup

1.  **Navigate to the client directory:**
    ```bash
    cd client
    ```
2.  **Install frontend dependencies:**
    ```bash
    npm install
    ```
3.  **Run the frontend development server:**
    ```bash
    npm start
    ```
    The React development server will start, and the application should open automatically in your default web browser at `http://localhost:3000`.

### Running Both Simultaneously

To run both the backend and frontend servers concurrently with a single command from the root directory:
```bash
npm run dev
```

## Technologies Used

### Backend

*   **Node.js:** JavaScript runtime environment
*   **Express.js:** Web application framework for Node.js
*   **MongoDB:** NoSQL database
*   **Mongoose:** ODM library for MongoDB and Node.js
*   **bcrypt:** Library for hashing passwords
*   **JSON Web Tokens (JWT):** For user authentication
*   **cors:** Middleware for enabling Cross-Origin Resource Sharing
*   **dotenv:** Module to load environment variables from a `.env` file
*   **morgan:** HTTP request logger middleware
*   **nodemon:** Utility that monitors for changes and automatically restarts the server
*   **concurrently:** Utility to run multiple commands concurrently

### Frontend

*   **React:** JavaScript library for building user interfaces
*   **React Router DOM:** For declarative routing in React applications
*   **Redux Toolkit:** For efficient state management
*   **Material UI (MUI):** React component library for faster and easier web development
*   **Axios:** Promise-based HTTP client for the browser and Node.js
*   **React Hot Toast:** Notifications for React applications
*   **CSS:** For styling

## Project Structure

The project is organized into a monorepo structure with the backend and frontend code in separate directories.

```
blog-app/
├── client/                 # React frontend application
│   ├── public/             # Public assets
│   ├── src/                # Frontend source code
│   │   ├── components/     # Reusable React components
│   │   ├── pages/          # Page components
│   │   ├── redux/          # Redux store and slices
│   │   ├── App.js          # Main application component
│   │   └── index.js        # Entry point for the React app
│   ├── package.json
│   └── README.md           # Client-specific README
├── config/                 # Backend configuration (e.g., database connection)
│   └── db.js
├── controllers/            # Backend route handlers (business logic)
│   ├── userController.js
│   └── blogController.js
├── models/                 # Mongoose models for database schemas
│   ├── userModel.js
│   └── blogModel.js
├── routes/                 # Express route definitions
│   ├── userRoutes.js
│   └── blogRoutes.js
├── .env                    # Environment variables (needs to be created)
├── .gitignore
├── package.json            # Backend dependencies and scripts
├── README.md               # Main project README
└── server.js               # Backend server entry point
```

## Available Scripts

In the project's root directory, you can run the following scripts:

*   `npm start`
    *   Starts the backend server using `node server.js`. (Note: `npm run server` is generally preferred for development).
*   `npm run server`
    *   Starts the backend server in development mode using `nodemon`, which automatically restarts the server on file changes.
*   `npm run client`
    *   Starts the frontend React development server (from the `client` directory).
*   `npm run dev`
    *   Runs both the backend server (`npm run server`) and the frontend client (`npm run client`) concurrently.

In the `client` directory, you can run the following scripts:

*   `npm start`
    *   Starts the React development server.
*   `npm run build`
    *   Builds the app for production to the `build` folder.
*   `npm test`
    *   Launches the test runner in interactive watch mode.
*   `npm run eject`
    *   Removes the single dependency (react-scripts) and copies all configuration files and transitive dependencies into your project. This is a one-way operation.

## Contributing

Contributions are welcome! If you have suggestions for improvements or find any issues, please feel free to:

1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/YourFeature`).
3.  Make your changes.
4.  Commit your changes (`git commit -m 'Add some feature'`).
5.  Push to the branch (`git push origin feature/YourFeature`).
6.  Open a Pull Request.

Please make sure to update tests as appropriate.
