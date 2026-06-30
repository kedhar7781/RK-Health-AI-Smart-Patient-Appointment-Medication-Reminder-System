# Phase 2: Technology Stack

This document details the software, frameworks, and APIs powering the **RK Health** application.

---

## 1. Frontend Layer
- **HTML5**: Form validation, responsive modals, print markup styles.
- **Vanilla CSS3**: Design system variables, dark/light theme, custom scrollbars, animations.
- **JavaScript (ES6)**: State manager, DOM parser, Chart.js integrations, session validator.
- **Chart.js (via CDN)**: Live medication compliance graphs.

## 2. Backend Server Layer
- **Python (v3.10+)**: High-performance backend execution language.
- **Flask (v2.3.3)**: Web server gateway routing API blueprints.
- **Flask-CORS (v4.0.0)**: Coordinates Cross-Origin Resource Sharing.
- **Werkzeug (v2.3.7)**: Decrypts/encrypts patient credentials.

## 3. Database & Storage Layer
- **SQLite3**: Fast local relational SQL database for patient login records.
- **Google Sheets Spreadsheet**: Cloud spreadsheet database backup.

## 4. Integration APIs & Services
- **Google Apps Script**: Handles Sheet CRUD and Google Calendar updates.
- **Twilio SMS REST Client (v8.5.0)**: Telephone E.164 verification checks and alerts.
- **OpenAI chat completions**: GPT-3.5/GPT-4 compatible text summarizations.
