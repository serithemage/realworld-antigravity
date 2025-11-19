# Backend Product Requirements Document (PRD) - RealWorld App

## 1. Introduction
This document outlines the backend requirements for the RealWorld application, a social blogging platform similar to Medium. The backend will provide a RESTful API to support the frontend application.

## 2. Core Features

### 2.1 Authentication & User Management
- **Registration**: Users can register with username, email, and password.
- **Login**: Users can login with email and password to receive a JWT.
- **Update User**: Authenticated users can update their email, username, password, image, and bio.
- **Get Current User**: Retrieve details of the currently logged-in user.
- **Profile**: View other users' profiles (username, bio, image, following status).
- **Follow/Unfollow**: Authenticated users can follow or unfollow other users.

### 2.2 Articles
- **CRUD Operations**:
  - Create an article (title, description, body, tags).
  - Read an article (by slug).
  - Update an article.
  - Delete an article.
- **List Articles**:
  - Filter by tag, author, favorited by user.
  - Pagination (limit, offset).
- **Feed**: Return articles from users followed by the current user.
- **Favorite/Unfavorite**: Authenticated users can favorite/unfavorite articles.

### 2.3 Comments
- **Create Comment**: Authenticated users can add comments to articles.
- **Get Comments**: Retrieve all comments for an article.
- **Delete Comment**: Authors can delete their own comments.

### 2.4 Tags
- **List Tags**: Return a list of all tags used in the system.

## 3. API Specifications
The API must adhere to the RealWorld API Spec:
- **Base URL**: `/api`
- **Response Format**: JSON
- **Authentication**: Bearer Token (JWT) in `Authorization` header.
- **Error Handling**: Standard HTTP status codes (200, 201, 401, 403, 404, 422) with error messages in the response body.

## 4. Non-Functional Requirements
- **Security**: Passwords must be hashed (e.g., bcrypt).
- **Performance**: Efficient database queries (avoid N+1 problems).
- **Statelessness**: The API should be stateless (RESTful).
