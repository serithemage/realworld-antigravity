# Frontend Tech Stack

Based on **Armin Ronacher's Agentic Coding Recommendations** (simplicity, stability) and standard modern web development practices.

## 1. Core Technologies
- **Runtime Environment**: **Node.js 24 LTS**
  - *Reason*: Latest Active LTS version (as of Oct 2025), ensuring stability and long-term support.
- **Framework**: **React 19.2.0**
  - *Reason*: Latest stable release (Nov 2025). Stable, vast ecosystem, simple component model.
- **Build Tool**: **Vite 6**
  - *Reason*: Fast, simple configuration, modern standard.
- **Language**: **JavaScript (ES6+)**
  - *Reason*: Keeping it simple. (TypeScript could be used, but "Simple Code" often implies avoiding type gymnastics if not strictly necessary, though TS is standard now. We will stick to JS or simple TS. Let's assume **JavaScript** for maximum simplicity/agility unless strict type safety is requested).

## 2. Styling
- **CSS**: **Vanilla CSS**
  - *Reason*: Explicitly requested by system instructions ("Use Vanilla CSS"). Also aligns with "Simple Code" (no complex build steps for CSS-in-JS or Tailwind configuration if not needed).
  - *Methodology*: CSS Variables for theming, scoped CSS or simple BEM naming.

## 3. State Management & Data Fetching
- **State Management**: **React Context + Hooks**
  - *Reason*: Built-in, simple, no external heavy libraries like Redux.
- **Data Fetching**: **Fetch API** (wrapped in a simple utility)
  - *Reason*: Native, simple, no need for Axios if not needed.

## 4. Architecture
- **Component-Based**: Small, reusable functional components.
- **Hooks**: Custom hooks for logic reuse (e.g., `useAuth`, `useArticles`).
- **No Class Components**: Functional components only.
