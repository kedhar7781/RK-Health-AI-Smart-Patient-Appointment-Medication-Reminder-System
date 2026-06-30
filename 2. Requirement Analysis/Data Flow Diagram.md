# Phase 2: Data Flow Diagram (DFD)

This document maps the flow of data within the **RK Health** application, highlighting input interfaces, local databases, and external cloud integrations.

---

## 1. DFD Architecture Flow

```
[ User UI Interaction ]
         │
         │ (POST/GET JSON Payload)
         ▼
[ Flask Controller (app.py) ]
    ├──► [ SQLite local DB ] (Reads/writes users, appts, meds, notes)
    │
    ├──► [ Twilio SMS Client ] (Dispatches reminder alerts to patient)
    │
    ├──► [ OpenAI API Gateway ] (Sends compiled clinical context, returns report)
    │
    └──► [ Google Apps Script URL ] (Forwards synchronization actions)
                  │
                  ▼
         [ Google Apps Script (code.js) ]
              ├──► [ Google Calendar API ] (Creates default calendar events)
              └──► [ Google Sheets Sheets ] (Writes rows to spreadsheet database)
```

---

## 2. Key Data Transactions

### A. Appointment Scheduling Sync
1. The user fills in patient details and doctor specialization on the HTML dashboard.
2. The frontend triggers `POST /api/appointments` carrying form values.
3. The Flask endpoint validates the request, logs the row into SQLite, and fires a POST request to `GOOGLE_APPS_SCRIPT_URL`.
4. The Apps Script opens the Google Sheet, appends the appointment details as a database row, logs a Google Calendar event, and returns the unique `google_event_id`.
5. The Flask backend updates the local database row with the `google_event_id` and returns the final synchronized appointment.

### B. Twilio Alert Dispatch
1. The user logs a medication schedule checking the SMS alert box.
2. The database updates the `phone_reminder` column to `1`.
3. The Flask app accesses user contact information, cleanses the phone number structure (converts to E.164), and sends the SMS body to Twilio.
4. Twilio delivers the alert to the patient's phone and returns the delivery status SID.

### C. AI summary Generation
1. The patient clicks **"Generate AI Summary"** in the web dashboard.
2. The server queries the SQLite database, gathering all appointments, medications, and notes logged under the user's ID.
3. The gathered context is compiled into a detailed prompt template and sent to the OpenAI-compatible gateway.
4. The response markdown is returned to the frontend, parsed by a custom JS regex markdown compiler, and displayed as a report card.
