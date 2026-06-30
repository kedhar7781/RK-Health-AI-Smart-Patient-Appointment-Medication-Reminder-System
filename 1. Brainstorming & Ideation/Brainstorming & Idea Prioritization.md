# Phase 1: Brainstorming & Idea Prioritization

This document details the feature brainstorming, comparison, and prioritization matrix utilized during the design of the **RK Health** application.

---

## 1. Feature Ideation Log

During the initial scoping, the following ideas were brainstormed:
- **Idea A: Fully Local SQLite app**: Great for security, but lacks cloud synchronization and remote calendar alerts.
- **Idea B: Cloud OAuth Google Sync**: Direct connection from frontend to Google Calendar API using client secrets. (Rejected: Requires distributing private Google client keys, creating security risks).
- **Idea C: Google Apps Script Web App Bridge**: Flask communicates with an Apps Script deployed on Google Drive. (Selected: Decouples server operations, keeps credentials safe, and simplifies setups).
- **Idea D: Twilio SMS Reminder Portal**: Integrates with Twilio API to validate phone formats and schedule text reminders.
- **Idea E: AI Summary Translation**: Sends notes and schedules to Llama/Grok/OpenAI to generate plain-text explanations.

---

## 2. Prioritization Matrix (Eisenhower Matrix)

We classified and prioritized the features to create our MVP:

| Feature | Impact | Feasibility | Priority | Description |
| :--- | :--- | :--- | :--- | :--- |
| **Auth Session Portal** | High | High | **High (P1)** | Registers users and encrypts passwords. |
| **SQLite CRUD Operations** | High | High | **High (P1)** | Instantly saves schedules locally. |
| **Google Sheets & Calendar Sync** | High | Medium | **High (P1)** | Syncs files and calendars via Apps Script. |
| **Twilio SMS Alerts** | High | Medium | **Medium (P2)** | Dispatches text message reminders. |
| **AI Translation Reports** | High | Medium | **Medium (P2)** | Translates medical terms to summaries. |
| **Wearable Heart Rate Sync** | Medium | Low | **Low (P3)** | Syncs Fitbit/Apple Health metrics (Roadmap). |

---

## 3. Technology Rationale
- **Frontend**: Vanilla Javascript and CSS Variables to ensure sub-100ms load speeds without compiling overhead.
- **Backend**: Flask (Python) for fast API prototyping and robust package support.
- **Database**: SQLite3 locally for offline speed, with cloud backup via Google Sheets.
