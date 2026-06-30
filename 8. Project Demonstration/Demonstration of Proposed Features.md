# Phase 8: Demonstration of Proposed Features

This document provides a step-by-step presentation script to demonstrate the features of the **RK Health** application.

---

## 1. Demo Walkthrough Script

### Step 1: Secure Login Page
- **Action**: Visit `https://rk-health.onrender.com` or local host, enter username `admin`, password `admin123`.
- **Checkpoint**: Show successful authentication and redirect to dashboard.

### Step 2: Dashboard Overview
- **Action**: Display stats cards and Chart.js adherence analytics graphs.
- **Checkpoint**: Point out the pre-seeded upcoming doctors calendar list.

### Step 3: Scheduling an Appointment
- **Action**: Click "New Appointment" button, fill in doctor and patient names, date, check "Send SMS Confirmation", and click "Save".
- **Checkpoint**: Show local list update and trace the Google Sheets/Calendar sync.

### Step 4: Tracking Pill Schedules & SMS Reminders
- **Action**: Navigate to "Medications", click the paper plane icon next to a pill.
- **Checkpoint**: Show Twilio SMS alert delivery status.

### Step 5: Generating AI Diagnostic Summary
- **Action**: Go to "AI Health Report", click **"Generate AI Summary"**.
- **Checkpoint**: View formatted markdown card translating terms and providing heart wellness tips. Click "Print" to export.
