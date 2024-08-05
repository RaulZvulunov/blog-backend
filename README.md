# Blog Backend

## Introduction

This project is the backend for a blog website, built using Node.js and Express. It handles user authentication, blog post management, and comment functionality. The backend communicates with a MongoDB database.

## Project Structure

- **index.js**: Main entry point of the application, exporting controllers.
- **controllers/PostController.js**: Handles blog post operations including creating, updating, fetching, and deleting posts.
- **middleware/handleValidationErrors.js**: Middleware for handling validation errors.

## Features

- **User Authentication**: Register, login, and manage users (assumed to be implemented in `UserController`).
- **Blog Management**: Create, read, update, and delete blog posts.
- **Comments**: Manage comments on blog posts (to be implemented).

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/RaulZvulunov/blog-backend.git
   cd blog-backend/mern-blog-backend-master
   ```

2. Install dependencies:
   ```sh
   npm install
   ```

3. Create a `.env` file and add your environment variables:
   ```sh
   MONGODB_URI=<your-mongodb-uri>
   JWT_SECRET=<your-jwt-secret>
   ```

4. Run the server:
   ```sh
   npm start
   ```

## API Endpoints

### Posts

- **Get all posts**
  ```sh
  GET /api/posts
  ```

- **Get post by ID**
  ```sh
  GET /api/posts/:id
  ```

- **Create a new post**
  ```sh
  POST /api/posts
  Headers: { "Authorization": "Bearer <token>" }
  Body: { "title": "Title", "text": "Content", "imageUrl": "URL", "tags": "tag1,tag2" }
  ```

- **Update a post**
  ```sh
  PATCH /api/posts/:id
  Headers: { "Authorization": "Bearer <token>" }
  Body: { "title": "Updated Title", "text": "Updated Content", "imageUrl": "Updated URL", "tags": "tag1,tag2" }
  ```

- **Delete a post**
  ```sh
  DELETE /api/posts/:id
  Headers: { "Authorization": "Bearer <token>" }
  ```

### Comments

- (To be implemented)

## Error Handling

- **Validation Errors**: Handled by `handleValidationErrors.js` middleware.
- **General Errors**: Appropriate status codes and messages are returned for different error cases.

