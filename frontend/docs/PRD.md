# Frontend Product Requirements Document (PRD) - RealWorld App

## 1. Introduction
This document outlines the frontend requirements for the RealWorld application. The frontend will be a Single Page Application (SPA) that consumes the backend REST API.

## 2. Core Pages & UI

### 2.1 Home Page
- **Global Feed**: Display latest articles from all users.
- **Your Feed**: Display articles from followed users (requires login).
- **Popular Tags**: List of popular tags. Clicking a tag filters the feed.
- **Pagination**: Navigate through article lists.

### 2.2 Sign In / Sign Up
- **Login Form**: Email and password.
- **Register Form**: Username, email, password.
- **Validation**: Client-side validation for required fields.

### 2.3 Article Page
- **Article Content**: Title, description, body (rendered Markdown), tags.
- **Author Info**: Name, image, follow button.
- **Meta Actions**: Edit/Delete (if author), Favorite/Unfavorite.
- **Comments Section**: List comments, add new comment (if logged in), delete comment (if author).

### 2.4 Editor Page
- **Create/Edit Article**: Form with title, description, body, and tags.
- **Validation**: Ensure required fields are present.

### 2.5 Settings Page
- **Update User**: Form to update URL, username, bio, email, password.
- **Logout**: Button to clear session and redirect to home.

### 2.6 Profile Page
- **User Info**: Image, username, bio, follow/unfollow button.
- **My Articles**: Tab to show articles written by the user.
- **Favorited Articles**: Tab to show articles favorited by the user.

## 3. Functional Requirements
- **Routing**: Client-side routing (e.g., `/login`, `/register`, `/article/:slug`, `/editor`, `/settings`, `/profile/:username`).
- **Authentication**: Store JWT in `localStorage` and attach to API requests.
- **State Management**: Manage user session, article lists, and form states.

## 4. Design & UX
- **Responsive Design**: Works on mobile and desktop.
- **Aesthetics**: Modern, clean, "premium" feel (as per system instructions).
- **Feedback**: Loading states, error messages, success notifications.
