# Phase 2: Solution Requirements

This document outlines the functional and non-functional requirements for the **RK Health** portal, mapping clinical workflows to system specs.

---

## 1. Functional Requirements

### FR1: Patient Authentication
- **Description**: Users can sign up with a unique username, email, phone number, and password, and log in securely.
- **Spec**: Passwords must be hashed using PBKDF2. Session cookies secure subsequent API requests.

### FR2: Smart Appointment Scheduling
- **Description**: Authenticated patients can schedule doctor consultations, search past appointments by doctor name or date, edit details, and cancel visits.
- **Spec**: Syncs automatically with Google Sheets and Google Calendar via a backend Apps Script execution.

### FR3: Medication Regimen Tracker
- **Description**: Patients can log pill names, dosages, time frequencies (morning, evening, as needed), toggle Twilio SMS reminders, and update compliance state (Active, Paused, Completed).
- **Spec**: Supports manual SMS testing directly from the tables.

### FR4: Vitals & Health Notes Log
- **Description**: Patients can write observations regarding physical experiences, vital readings, or side effects.
- **Spec**: Notes support text search matching.

### FR5: Generative AI summary Report
- **Description**: Compiles patient datasets (appointments, pill schedules, notes) and calls OpenAI-compatible APIs to generate patient-friendly health advice.
- **Spec**: Custom HTML formatting parser renders output in an attractive card.

---

## 2. Non-Functional Requirements

- **N1: Low Latency UI**: Dashboard rendering must complete under 150ms.
- **N2: Responsiveness**: Layouts must dynamically support mobile viewports (collapsible menus, responsive table scrolls).
- **N3: Safe Fallbacks**: If external integrations (Twilio, Google, OpenAI) fail or lack credentials, the server must log warnings and continue running local databases without crashing.
