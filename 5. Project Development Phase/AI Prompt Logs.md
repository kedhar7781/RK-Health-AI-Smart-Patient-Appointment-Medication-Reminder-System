# Phase 5: AI Prompt Logs & Tool Analysis

This document details the AI prompt engineering and AI tools used during the development of the **RK Health** portal.

---

## 1. AI Prompt Logs (Summary Generation)

We use the following detailed prompt template in `ai_service.py` to compile patient summaries:

```text
You are RK Health AI, a highly empathetic and knowledgeable clinical assistant.
Your task is to analyze the patient's health data below and generate a friendly, professional, and clear health report summary.

{patient_appointments_medications_notes}

Please structure your response exactly with the following five sections, using clear Markdown headings:
# Patient Visit Summary
# Medicine Instructions
# Follow-up Advice
# Health & Wellness Tips
# Patient-Friendly Medical Explanations
```

---

## 2. AI Tools Used

During development, the following AI systems supported the project:
1. **Coding Assistant (Google Gemini)**: Used to write the SQLite database structures, JWT-like session check routes, and Chart.js frontend canvas loops.
2. **Generative Summarizer API**: OpenAI-compatible API endpoints (Grok / Llama) used to generate clinical plain-text summaries from patients' raw notes.
3. **UI/Mockup Generator**: Used to construct design mockups and verify layouts.
