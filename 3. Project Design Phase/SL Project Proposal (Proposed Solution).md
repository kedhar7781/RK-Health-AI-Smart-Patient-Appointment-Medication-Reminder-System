# Phase 3: Project Proposal (Proposed Solution)

**Project Title**: RK Health – AI Smart Patient Appointment & Medication Reminder System
**Target Track**: AI Specialist Capstone Project

---

## 1. Project Objectives
RK Health provides a secure patient dashboard that solves three main healthcare compliance problems:
1. Schedules appointments on Google Calendar and Google Sheets database.
2. Tracks medication schedules and daily timelines, dispatching Twilio text reminders.
3. Translates clinical notes and symptoms into patient-friendly summaries using generative AI.

---

## 2. Proposed Scope of Work
The system consists of three modules:
- **API Server & SQLite Engine**: Implements JWT-like Flask sessions, secures credentials, and manages local CRUD transactions.
- **Microservices Integrations**: Validates E.164 phone formats, forwards data payloads to Google Web Script URLs, and connects to OpenAI chat gateways.
- **Vibrant Responsive Client**: Renders real-time Chart.js diagrams, supports dark/light themes, and compiles markdown notes.

---

## 3. Anticipated Deliverables
- **Codebase**: Fully working Flask API server containerized via Docker.
- **Database Schema**: SQLite engine containing tables for users, notes, pills, and schedules.
- **Documentation**: Design topologies, API lists, setup guides, and slides.
- **QA Suite**: Automated pytest isolation test files verifying 100% path coverage.
