# Phase 2: Customer Journey Map

This document tracks a patient's emotional journey and touchpoints while using the **RK Health** portal, illustrating the before, during, and after scenarios.

---

## 1. Journey Map Lifecycle

```
[ Stage 1: Consultation ] ──> [ Stage 2: Portal Setup ] ──> [ Stage 3: Daily Reminders ] ──> [ Stage 4: AI Analysis ]
```

### Stage 1: Medical Consultation (Before RK Health)
- **Patient Action**: Sarah visits Dr. Sarah Jenkins (Cardiologist), gets diagnosed, and receives a prescription (Lisinopril, Atorvastatin) and an ECG review appointment.
- **Emotion**: Overwhelmed, worried about heart parameters.
- **Touchpoint**: Prescriptions printed on paper.

### Stage 2: Portal Setup (Adoption)
- **Patient Action**: Sarah signs up on the RK Health portal, inputs her doctor consultation dates, inputs her medications regimen, and inputs symptom logs.
- **Emotion**: Hopeful, appreciates the dark-mode layout.
- **Touchpoint**: Dashboard cards, signup forms.

### Stage 3: Daily Reminders (Usage)
- **Patient Action**: Sarah receives a daily SMS reminder via Twilio at 08:00 to take her Lisinopril. She checks her compliance charts.
- **Emotion**: Confident, feels in control of her health.
- **Touchpoint**: Twilio SMS texts on her mobile phone, compliance timeline.

### Stage 4: AI Report Generation (Prevention)
- **Patient Action**: Sarah navigates to the "AI Health Report" and clicks **"Generate AI Summary"**. She exports and prints a plain-text overview translating "ECG" and listing heart-rate tips.
- **Emotion**: Reassured, understands her cardiology details.
- **Touchpoint**: Custom print layout, AI Markdown card.

---

## 2. Touchpoints & Key Opportunities
- **Critical Opportunity**: Twilio phone format verification prevents users from registering invalid numbers, ensuring they never miss a critical SMS text.
- **Visual Feedback**: Real-time compliance charts immediately highlight if pills are being neglected, reinforcing consistent habits.
