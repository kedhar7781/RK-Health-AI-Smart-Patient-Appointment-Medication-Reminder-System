# Phase 8: Scalability & Future Plan

This document outlines the optimization, hosting scale-ups, and roadmap enhancements planned for the **RK Health** portal.

---

## 1. Cloud Scaling Strategies
- **Server Deployment**: Transition from Render's free tier container to a load-balanced Amazon ECS or Google Cloud Run cluster to handle high patient loads.
- **Database Scaling**: Swap local SQLite3 engine for a fully managed Amazon RDS PostgreSQL or MySQL cluster, supporting connection pools and database replication.
- **Microservices Orchestration**: Run background tasks (like cron-based scheduled Twilio reminders) using Celery and Redis rather than single-threaded synchronous loops.

---

## 2. Product Roadmap Enhancements

### A. Wearables Integration
- **Concept**: Connect Apple HealthKit and Fitbit APIs to automatically sync steps, sleep data, and live resting heart rate.
- **Feature**: AI summary cards can adapt warnings if palpitations correspond with high resting heart rates.

### B. Patient Consultation Chatbot
- **Concept**: Add a real-time conversational chat box widget in the dashboard.
- **Feature**: Patients can ask: *"Can I take Lisinopril with grapefruit?"* or *"What did the cardiologist say about my ECG?"* and receive immediate clinical answers.

### C. Multi-Patient Clinician Portal
- **Concept**: Create a practitioner view for doctors.
- **Feature**: Doctors can monitor adherence scores across all their patients and push prescription updates directly.
