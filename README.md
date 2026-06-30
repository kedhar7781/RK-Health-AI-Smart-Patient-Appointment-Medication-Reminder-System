# RK Health – AI Smart Patient Appointment & Medication Reminder System

RK Health is an intelligent, patient-centric web portal that empowers patients to manage doctor appointments, schedule medication regimens, maintain health symptom logs, and receive AI-generated clinical advice.

This repository is structured in accordance with the **AI Specialist Track Capstone Project** guidelines.

---

## 🌟 Key Features

- **📊 Patient Dashboard**: Responsive grid layout featuring Chart.js health summaries, daily compliance status widgets, and upcoming appointment timelines.
- **📅 Appointment Scheduler**: Book, edit, and cancel appointments with automated synchronization to **Google Sheets Database** and **Google Calendar events**.
- **💊 Medication Regimen Tracker**: Configure medicine names, dosage volumes, exact reminder times, and frequency intervals.
- **💬 Twilio SMS Alerts**: Sends reminders and confirmations to patient phones. Supports local console log falls-backs.
- **📝 Patient Health Diary**: Record symptoms, vital metrics, and observations to share with clinical practitioners.
- **🧠 Generative AI Assistant**: Analyzes patient datasets to translate complex medical terms and generate plain-English advice.
- **🎨 Glassmorphic Theme Design**: Features custom CSS variables supporting dark/light mode toggles, micro-animations, and slide-in toasts.

---

## 🏗️ Project Architecture

```
                  +-----------------------------------+
                  |           Patient Web UI          |
                  |     (HTML5, Premium CSS3, JS)     |
                  +-----------------+-----------------+
                                    |
                                    | (REST APIs / JSON)
                                    v
                  +-----------------------------------+
                  |           Flask Backend           |
                  +-----+-----------+-----------+-----+
                        |           |           |
       (Local SQLite)   |           |           | (OpenAI / Grok / Llama API)
                        v           v           v
             +------------+   +-----------+   +-------------+
             | SQLite DB  |   |  Twilio   |   | AI Summary  |
             | (Vitals /  |   |  SMS Gate |   | Engine      |
             |  Schedules|   +-----------+   +-------------+
             +------------+
                        |
                        | (Forward/Push REST payload)
                        v
         +---------------------------------------------+
         |      Google Apps Script REST Web App        |
         +----------------------+----------------------+
                                |
                   +------------+------------+
                   |                         |
                   v                         v
         +-------------------+     +--------------------+
         |   Google Sheets   |     |   Google Calendar  |
         | (Cloud Database)  |     | (Appointment Sync) |
         +-------------------+     +--------------------+
```

---

## 📂 Repository Structure

The project deliverables are organized into the following 8 stages:

```
├── 1. Brainstorming & Ideation/
│   ├── Brainstorming & Idea Prioritization.md
│   ├── Define Problem Statements.md
│   └── Empathy Map.md
├── 2. Requirement Analysis/
│   ├── Customer Journey Map.md
│   ├── Data Flow Diagram.md
│   ├── Solution Requirements.md
│   └── Technology Stack.md
├── 3. Project Design Phase/
│   ├── API Specification.md                   # REST routes documentation
│   ├── Problem-Solution Fit.md
│   ├── SL Project Proposal.md                 # Formal project proposal
│   └── Solution Architecture.md               # Architecture design maps
├── 4. Project Planning Phase/
│   └── Project Planning Template.md           # Sprints and roadmap milestones
├── 5. Project Development Phase/              # Core Source Code & Logs
│   ├── backend/                               # Flask server submodules
│   ├── frontend/                              # Responsive Web Portal code
│   ├── google-apps-script/                    # Apps script code.js bridge
│   ├── Dockerfile
│   ├── docker-compose.yml
│   ├── requirements.txt
│   ├── AI Prompt Logs.md                      # Prompt logs used
│   ├── AI Tools Used.md                       # List of AI systems used
│   ├── Code-Layout, Readability.md            # Directory modularity notes
│   └── Functional Features included.md        # Feature specs
├── 6. Performance Testing/
│   └── Performance Testing Report.md          # Pytest automation QA results
├── 7. Documentation & Demo/
│   ├── Project Documentation.md               # User manuals and statistics
│   └── Project Execution Guide.md             # Standard setup guidelines
├── 8. Project Demonstration/
│   ├── presentation.html                      # Interactive slide deck presentation
│   ├── Communication Plan Template.md
│   ├── Demonstration of Proposed Features.md
│   ├── Project Demo Planning Template.md
│   ├── Scalability & Future Plan.md
│   └── Team Involvement in Demonstration.md
└── LICENSE                                    # MIT License
```

---

## 🚀 Quick Start Instructions

1. **Configure Environment Keys**:
   Copy `.env.example` to `.env` and fill in your API keys. If left blank, mock mode runs automatically.
   ```bash
   cp .env.example .env
   ```

2. **Launch with Docker**:
   ```bash
   docker-compose up --build
   ```
   Open `http://localhost:5000` in your web browser.

3. **Or Launch Locally (Python)**:
   ```bash
   python -m venv venv
   # Activate: .\venv\Scripts\activate (Windows) or source venv/bin/activate (macOS/Linux)
   pip install -r requirements.txt
   python backend/app.py
   ```
   Open `http://localhost:5000` in your web browser.

4. **Access Portal Demo User**:
   - **Username**: `admin`
   - **Password**: `admin123`
