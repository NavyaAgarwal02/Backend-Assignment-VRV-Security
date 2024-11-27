# Voting Application for VRV Security Backend Developer Assignment [Role-Based Access Control (RBAC) UI]

This backend application for a voting system demonstrates **Authentication**, **Authorization**, and **Role-Based Access Control (RBAC)**. It simulates a real-world voting process, where users can vote for candidates and administrators can manage candidates. The application is built with a focus on security, scalability, and adherence to best practices in backend development.

## Features

### Authentication
  - Secure sign-up and login for users.
  - Uses JWT tokens for session management.
  - Passwords are hashed using bcrypt for security.

### Authorization with RBAC
  - Users are assigned roles: Admin or Voter.
  - Access to endpoints is determined by role:
    - Admins can manage candidates but cannot vote.
    - Voters can view candidates and vote (one vote per user).
   
### Voting System
  - View a list of candidates.
  - Cast a vote (ensures one user can vote only once).
  - View vote counts for each candidate (Admin only).

### Admin Panel
  - Add, update, and delete candidates.

### Technologies Used
  - Node.js
  - Express.js
  - MongoDB
  - JSON Web Tokens (JWT) for secure authentication.
  - bcrypt for password hashing.

## Installation

1. **Clone the repository:**
   `git clone https://github.com/NavyaAgarwal02/Backend-Assignment-VRV-Security` 
   
2. **Install dependencies:**
  `npm install`

3. **Configure the `.env` file with:**
  - Database URI (MongoDB)
  - JWT secret

4. **Start the server:**
  `npm start`

## API Endpoints

### Authentication
  - `POST /signup` - User sign-up with Aadhar number and password.
  - `POST /login` - User login to receive a JWT token.
    
### Candidate Management (Admin)
  - `GET /candidates` - View all candidates.
  - `POST /candidates` - Add a candidate.
  - `PUT /candidates/:id` - Update a candidate by ID.
  - `DELETE /candidates/:id` - Delete a candidate by ID.

### Voting
  - `GET /candidates/vote/count` - View vote count for each candidate (Admin).
  - `POST /candidates/vote/:id` - Vote for a candidate (Voter).

### User Management
  - `GET /users/profile` - View user profile.
  - `PUT /users/profile/password` - Change password.

## Security Features

### JWT-Based Authentication:
  - Ensures secure session handling.
  - Tokens have expiration to limit misuse.

### Role-Based Access Control (RBAC):
  - Middleware validates roles before granting access to resources.
    
### Input Validation:
  - Validates inputs for endpoints to prevent attacks like SQL injection.
    
### Password Protection:
  - Hashing ensures user credentials are securely stored.

## Evaluation Criteria Highlights
  - **Secure Authentication**: Password hashing with bcrypt and JWT tokenization.
  - **Flexible RBAC**: Middleware ensures route-specific access based on roles.
  - **Code Quality**: Modular and well-documented code for clarity.
  - **Scalability**: Designed to extend easily for new features.

## Submission Details
  - This project is hosted on GitHub:
    `https://github.com/NavyaAgarwal02/Backend-Assignment-VRV-Security`
    
### Instructions to Test
1. Clone the repository.
2. Install dependencies and configure environment variables.
3. Start the server and use tools like Postman to test endpoints.

Feel free to reach out if additional documentation or explanations are needed.

