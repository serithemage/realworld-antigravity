---
trigger: model_decision
description: rules for backend works
---

# Backend Rules

## General
- **Language**: Respond in Korean.
- **Context**: Always check related files before making changes.
- **Safety**: Do not delete files without confirmation.

## Tech Stack
- **Language**: Go
- **Framework**: Gin / Echo / Standard Library
- **Database**: PostgreSQL / MySQL / SQLite

## Coding Style
- **Naming**: Use camelCase for variables/functions, PascalCase for types/components.
- **Comments**: Write comments in Korean (as requested).
- **Formatting**: Use GoFmt.
- **Error Handling**: Handle errors explicitly (Go style).
- **Context**: Use context for cancellation/timeouts.

## Design Principles (SOLID)
- **S**ingle Responsibility (SRP): 하나의 모듈/클래스는 하나의 변경 이유만 가져야 합니다.
- **O**pen/Closed (OCP): 확장에 열려 있고, 수정에 닫혀 있어야 합니다.
- **L**iskov Substitution (LSP): 서브타입은 언제나 기반 타입으로 교체할 수 있어야 합니다.
- **I**nterface Segregation (ISP): 클라이언트는 사용하지 않는 인터페이스에 의존하지 않아야 합니다.
- **D**ependency Inversion (DIP): 추상화에 의존해야 하며, 구체화에 의존하면 안 됩니다.