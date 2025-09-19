# Job Portal Application

This is a full-stack job portal application built with the MERN stack (MongoDB, Express.js, React, Node.js). It allows recruiters to post job openings and job seekers to apply for them.

## Tech Stack

-   **Frontend**: React, Vite, Redux Toolkit, Tailwind CSS, Axios
-   **Backend**: Node.js, Express.js, MongoDB, Mongoose
-   **Authentication**: JSON Web Tokens (JWT)
-   **File Storage**: Cloudinary for resume and profile picture uploads.

## Features

-   Dual user roles: `student` (job seeker) and `recruiter`.
-   Secure user registration and login with password hashing and JWT authentication.
-   Recruiters can post, view, and manage job listings.
-   Students can browse jobs and submit applications.
-   Profile management with resume upload functionality.

## Project Structure

The project is organized into two main directories in a monorepo-style structure:

-   `./frontend`: The React client application built with Vite.
-   `./backend`: The Node.js/Express REST API server.

The root directory contains scripts to install dependencies and run both applications concurrently.

## Getting Started

### Prerequisites

-   Node.js (v18.x or newer)
-   npm
-   MongoDB (a local instance or a cloud-hosted service like MongoDB Atlas)

### Setup & Installation

1.  **Clone the repository:**
    ```bash
    git clone <your-repository-url>
    cd job-portal
    ```

2.  **Configure Environment Variables:**

    *   **Backend:** Create a `.env` file in the `backend` directory (`backend/.env`) and add the following variables:
        ```env
        MONGO_URI=<your_mongodb_connection_string>
        PORT=8000
        JWT_SECRET=<your_jwt_secret_key>
        CLOUDINARY_CLOUD_NAME=<your_cloudinary_cloud_name>
        CLOUDINARY_API_KEY=<your_cloudinary_api_key>
        CLOUDINARY_API_SECRET=<your_cloudinary_api_secret>
        ```

    *   **Frontend:** Create a `.env` file in the `frontend` directory (`frontend/.env`) to define the backend API endpoint:
        ```env
        VITE_API_BASE_URL=http://localhost:8000/api/v1
        ```

3.  **Install Dependencies:**
    From the root `job-portal` directory, run the `install-all` script. This will install dependencies for both the frontend and backend.
    ```bash
    npm run install-all
    ```

### Running the Application

Start both the frontend and backend development servers concurrently by running the `dev` script from the root directory.

```bash
npm run dev
```

-   The React development server will start on `http://localhost:5173`.
-   The Node.js backend server will start on `http://localhost:8000`.