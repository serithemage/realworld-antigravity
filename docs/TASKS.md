# Implementation Tasks

This document outlines the step-by-step tasks for implementing the RealWorld application.

## Phase 1: Project Initialization & Setup

- [x] **Repository Setup** ✅ *Closed: Issue #1*
  - [x] Initialize Git repository.
  - [x] Create `README.md` for root, backend, and frontend.
  - [x] Define Tech Stack & PRD.
  - [x] Create `docs/TASKS.md` (This file).

- [x] **Backend Setup (Go)** ✅ *Closed: Issue #2*
  - [x] Initialize Go module (`go mod init`).
  - [x] Set up project structure (`cmd/`, `internal/`, `pkg/`).
  - [x] Install dependencies (SQLite: `modernc.org/sqlite`).
  - [x] Configure `golangci-lint`.
  - [x] Create a simple "Hello World" HTTP server to verify setup.

- [x] **Frontend Setup (React)** ✅ *Closed: Issue #3*
  - [x] Initialize Vite project (`npm create vite@latest`).
  - [x] Install dependencies (`react-router-dom`, etc.).
  - [x] Set up ESLint & Prettier.
  - [x] Create a basic "Hello World" page.

- [/] **Database Setup** 🔄 *In Progress: Issue #4*
  - [x] Configure SQLite (File-based).
  - [ ] Create database schema (`realworld.db`).
  - [ ] Set up migration tool (SQL scripts).

## Phase 2: Backend Implementation (Core)

- [ ] **Database Schema**
  - [ ] Design schema for `users` table.
  - [ ] Design schema for `articles`, `tags`, `comments`, `favorites`, `follows`.
  - [ ] Write SQL migration scripts.

- [ ] **User Authentication & Profiles**
  - [ ] Implement `POST /api/users` (Registration).
  - [ ] Implement `POST /api/users/login` (Authentication & JWT generation).
  - [ ] Implement `GET /api/user` (Get Current User).
  - [ ] Implement `PUT /api/user` (Update User).
  - [ ] Implement `GET /api/profiles/:username` (Get Profile).
  - [ ] Implement `POST /api/profiles/:username/follow` (Follow User).
  - [ ] Implement `DELETE /api/profiles/:username/follow` (Unfollow User).

- [ ] **Articles Core**
  - [ ] Implement `POST /api/articles` (Create Article).
  - [ ] Implement `GET /api/articles/:slug` (Get Article).
  - [ ] Implement `PUT /api/articles/:slug` (Update Article).
  - [ ] Implement `DELETE /api/articles/:slug` (Delete Article).
  - [ ] Implement `GET /api/articles` (List Articles with filters).

## Phase 3: Backend Implementation (Advanced)

- [ ] **Comments & Tags**
  - [ ] Implement `POST /api/articles/:slug/comments` (Add Comment).
  - [ ] Implement `GET /api/articles/:slug/comments` (Get Comments).
  - [ ] Implement `DELETE /api/articles/:slug/comments/:id` (Delete Comment).
  - [ ] Implement `GET /api/tags` (Get Tags).

- [ ] **Feed & Favorites**
  - [ ] Implement `GET /api/articles/feed` (User Feed).
  - [ ] Implement `POST /api/articles/:slug/favorite` (Favorite Article).
  - [ ] Implement `DELETE /api/articles/:slug/favorite` (Unfavorite Article).

## Phase 4: Frontend Implementation (Foundation)

- [ ] **Infrastructure**
  - [ ] Set up API client helper (Axios or Fetch wrapper with Interceptors for Auth).
  - [ ] Set up Auth Context/Provider.
  - [ ] Create Layout components (Header, Footer).

- [ ] **Auth Pages**
  - [ ] Build Login Page (`/login`).
  - [ ] Build Register Page (`/register`).
  - [ ] Connect to Backend Auth APIs.

## Phase 5: Frontend Implementation (Features)

- [ ] **Home Page**
  - [ ] Build Global Feed tab.
  - [ ] Build Your Feed tab (Auth required).
  - [ ] Build Popular Tags sidebar.
  - [ ] Implement Pagination.

- [ ] **Article Page**
  - [ ] Display Article content (Markdown rendering).
  - [ ] Display Author info & Follow button.
  - [ ] Display Comments section.
  - [ ] Implement Post Comment feature.

- [ ] **Editor & Settings**
  - [ ] Build Editor Page (`/editor`, `/editor/:slug`).
  - [ ] Build Settings Page (`/settings`).

- [ ] **Profile Page**
  - [ ] Build Profile Header (User info, Follow toggle).
  - [ ] Build My Articles tab.
  - [ ] Build Favorited Articles tab.

## Phase 6: Polish & Deployment

- [ ] **Testing & Fixes**
  - [ ] Run full E2E manual test.
  - [ ] Fix any UI/UX glitches.
  - [ ] Ensure all "Agentic Coding Recommendations" are met (Simplicity, Speed).

- [ ] **Final Documentation**
  - [ ] Update READMEs with run instructions.
  - [ ] Verify API compliance.
