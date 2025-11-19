# Backend Tech Stack

Based on **Armin Ronacher's Agentic Coding Recommendations**, we prioritize simplicity, stability, and "dumb" code that is easy for agents to read and maintain.

## 1. Core Technologies
- **Language**: **Go (Golang) 1.25.4**
  - *Reason*: **Explicitly recommended by Armin Ronacher** for agentic coding. Verified latest stable version as of Nov 2025.
  - *Benefits*: Static typing, simplicity, explicit error handling, fast compilation, and stability. Agents handle Go's "boring" and explicit nature very well.
- **Web Framework**: **Standard Library (`net/http`)**
  - *Reason*: Go 1.22+ has a powerful router. Using the standard library avoids framework "magic" and dependency churn, aligning with the "dumbest possible thing" philosophy.
- **Database**: **PostgreSQL 18.1**
  - *Reason*: Latest stable production release (Nov 2025).
- **Database Interaction**: **`pgx` (Jackc/pgx) v5+**
  - *Reason*: High-performance, pure Go driver.
  - *Methodology*: **Raw SQL**. No ORMs (GORM, etc.). Agents write excellent SQL. We will use explicit SQL queries for maximum clarity and control.

## 2. Development Tools
- **Linting**: **golangci-lint**
  - *Reason*: Standard, comprehensive linter for Go.
- **Testing**: **Standard `testing` package**
  - *Reason*: Simple, explicit, no complex fixture magic (unlike Pytest).
- **Dependency Management**: **Go Modules**
  - *Reason*: Native, standard.

## 3. Architecture Patterns
- **Standard Layout**: Follow standard Go project layout (`cmd/`, `internal/`, `pkg/`).
- **Service/Repository Pattern**: Clear separation of concerns.
  - *Handler*: HTTP transport logic.
  - *Service*: Business logic.
  - *Repository*: Database access (Raw SQL).
- **Explicit Error Handling**: `if err != nil` everywhere. No hidden exceptions.
