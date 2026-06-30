# Phase 5: Code-Layout, Readability, and Reusability

This document details the code architecture, folder layouts, and software design principles applied in **RK Health**.

---

## 1. Directory Modularity

We structured the project using modular components to ensure clean separation of concerns:
- **`backend/routes/`**: Grouped endpoints by business function (Auth, Appointments, Meds, Notes, Summary).
- **`backend/services/`**: Encapsulates external APIs (Twilio, Google Script, OpenAI), separating core business logic from network clients.
- **`backend/database.py`**: A single database orchestrator handling initializations and table schema configurations.
- **`frontend/`**: Grouped styles and JS controllers in clean subfolders (`/css/styles.css` and `/js/app.js`).

---

## 2. Reusability Principles
- **Decorator Patterns**: Created the `@login_required` wrapper to reuse session verification logic across all clinical routes.
- **SQLite Row Factories**: Configured `sqlite3.Row` dictionary models globally, enabling consistent object conversions and reducing JSON mapping boilerplate.
- **Clean Fallbacks**: Created rules-based generators in our Twilio and AI service wrappers to reuse the client flows without breaking during local offline sandboxed development.
