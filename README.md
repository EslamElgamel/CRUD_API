# CRUD_API

A professional RESTful API for managing users and courses, built with Node.js and Express. This project demonstrates best practices in API design, authentication, validation, error handling, and modular code structure.

## Features
- User registration and authentication (JWT)
- CRUD operations for users and courses
- Input validation and error handling
- Modular controllers, models, and routes
- Middleware for async handling and token verification

## Technologies Used
- Node.js
- Express.js
- MongoDB (Mongoose)
- JSON Web Tokens (JWT)
- Joi (validation)

## Project Structure
```
index.js
package.json
controllers/
  courses.controllers.js
  users.controllers.js
middlewares/
  asyncwrapper.js
  validationSchema.js
  verfiyToken.js
models/
  courses.model.js
  user.model.js
routes/
  courses.routes.js
  users.route.js
utils/
  appError.js
  generateJWT.js
  httpsStatusText.js
```

## Getting Started

### Prerequisites
- Node.js >= 14.x
- MongoDB instance (local or cloud)

### Installation
1. Clone the repository:
   ```bash
   git clone <repo-url>
   cd CRUD_API
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Configure environment variables:
   - Create a `.env` file in the root directory
   - Add your MongoDB URI and JWT secret:
     ```env
     MONGODB_URI=your_mongodb_uri
     JWT_SECRET=your_jwt_secret
     ```

### Running the API
```bash
npm start
```
The server will start on the port specified in your `.env` file (default: 3000).

## API Endpoints

### Users
- `POST /api/users/register` — Register a new user
- `POST /api/users/login` — Login and receive JWT
- `GET /api/users` — Get all users (protected)
- `GET /api/users/:id` — Get user by ID (protected)
- `PUT /api/users/:id` — Update user (protected)
- `DELETE /api/users/:id` — Delete user (protected)

### Courses
- `GET /api/courses` — Get all courses
- `GET /api/courses/:id` — Get course by ID
- `POST /api/courses` — Create a new course (protected)
- `PUT /api/courses/:id` — Update course (protected)
- `DELETE /api/courses/:id` — Delete course (protected)

## Middleware
- **Async Wrapper:** Handles async errors in controllers
- **Validation Schema:** Validates request bodies
- **Verify Token:** Protects routes using JWT

## Error Handling
Centralized error handling using custom `appError` utility and HTTP status text responses.

## Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

## License
This project is licensed under the MIT License.

## Author
- [Your Name](https://github.com/yourusername)
