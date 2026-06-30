# Phase 4: Project Planning Template

This document tracks the development planning, sprints, milestones, and task allocations for the **RK Health** portal.

---

## 1. Project Roadmaps & Milestones

The project was executed in five key milestones:

### Milestone 1: Requirement Analysis & Database Setup
- **Tasks**: Map user stories, install virtual environments, structure `config.py`, write SQLite table schema, and seed test data.
- **Duration**: 2 Days (Completed)

### Milestone 2: Core API Routes & blue-printing
- **Tasks**: Implement secure password hashing, Flask login sessions, and `/auth`, `/appointments`, `/medications`, and `/notes` blueprints.
- **Duration**: 3 Days (Completed)

### Milestone 3: External Microservices Integrations
- **Tasks**: Deployed Google Apps Script web app, established calendar event sync, integrated Twilio rest SMS client, and connected OpenAI API summarizer.
- **Duration**: 3 Days (Completed)

### Milestone 4: Frontend Portal & UX design
- **Tasks**: Design glassmorphic stylesheets with light/dark toggles, draw Chart.js compliance stats, code debounced search filters, and write regex markdown parser.
- **Duration**: 3 Days (Completed)

### Milestone 5: Quality Assurance & Cloud Deployment
- **Tasks**: Write unit test files in `tests/`, execute pytest commands, configure `Dockerfile` and `docker-compose.yml`, and host live on Render.
- **Duration**: 2 Days (Completed)

---

## 2. Resource & Budget Estimates
- **Local SQLite Storage**: Free.
- **Render Hosting Service**: Free plan web service.
- **Twilio SMS**: Sandbox trial account (Free).
- **AI summarizing**: Developer credits (OpenAI/Grok).
- **Google Sheets Database & Calendar**: Free workspace account.
