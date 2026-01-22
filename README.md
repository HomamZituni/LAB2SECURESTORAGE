# Secure Notes API

A simple secure notes REST API. Each user can register, log in, and manage only their own notes.

## Features

- User registration and login with hashed passwords.
- JWT authentication for protected routes.
- Create, read, update, and delete notes.
- Authorization checks so users can only modify their own notes.
- MongoDB data storage using Mongoose models.

## Tech Stack

- Node.js
- Express
- MongoDB + Mongoose
- JSON Web Tokens (JWT)
- bcrypt for password hashing
- dotenv for environment variables

How to Test Auth Rotes
Register
POST /api/users/register
{
  "username": "testuser",
  "email": "test@example.com",
  "password": "password123"
}

Login
POST /api/users/login
{
  "email": "test@example.com",
  "password": "password123"
}

Create a Note
POST /api/notes
{
  "title": "My Note",
  "content": "This is the content"
}

Update a note
PUT /api/notes/:id
{
  "title": "Updated title",
  "content": "Updated content"
}

Delete a note
DELETE /api/notes/:id
Only the owner is authorized to delete expect a 403 if you try to circumvent 

