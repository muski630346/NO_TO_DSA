# NO_TO_DSA
agentic ai skill craft hiring process
# SkillPrint

AI-powered bias-blind hiring platform that evaluates real-world engineering skills instead of DSA-based filtering.

SkillPrint analyzes practical project work and generates skill intelligence to help companies hire based on ability, not algorithm memorization.

---

## Problem Statement

Modern hiring systems rely heavily on Data Structures & Algorithms (DSA) rounds that often fail to reflect real-world job skills.

As a result:
- Capable engineers are filtered out unfairly.
- Designers and frontend developers are judged on irrelevant algorithm questions.
- Tier 2 and Tier 3 talent remains invisible.
- Companies miss high-performing candidates.

SkillPrint addresses this gap by evaluating real-world project contributions instead of test-based elimination.

---

## Solution Overview

SkillPrint connects to a candidate’s GitHub profile and analyzes repositories to generate:

- AI Skill Graph (multi-dimensional skill scoring)
- Role-Fit Score (Job Description vs real skills)
- Bias-Blind Screening
- Real-World Challenge Generation
- Skill Gap Roadmap (improvement guidance)

AI provides signal.
Humans make the final hiring decision.
No automated rejection.

---

## Core Features

### 1. AI Skill Graph
Analyzes:
- Repository count
- Language usage
- Code activity
- Contribution patterns
- Project diversity
- Open-source engagement

Outputs a structured skill profile.

### 2. Role-Fit Engine
Paste any Job Description and receive:
- Match percentage
- Skill alignment breakdown
- Reasoning summary

### 3. Bias-Blind Screening
- College name hidden until final round
- Evaluation based only on skills
- Reduces institutional bias

### 4. Real-World Challenge Generator
Generates practical role-based tasks such as:
- Build a paginated search filter
- Create REST API with authentication
- Optimize frontend performance

Not Leetcode.
Actual day-one job simulations.

### 5. Skill Gap Roadmap
Identifies missing competencies and generates:
- 30-day improvement roadmap
- Technology focus areas
- Suggested build projects

---

## System Architecture

### Frontend
- React + TypeScript
- Tailwind CSS
- REST API Integration

### Backend
- Python 3.11
- FastAPI
- Pydantic
- Uvicorn

### AI / Analysis Layer
- GitHub API v3
- Embedding-based text matching
- ONNX Runtime (future scaling)

### Database (Optional Extension)
- PostgreSQL
- Supabase

---

## Project Structure

```
skillprint/
│
├── backend/
│   ├── main.py
│   ├── skill_analyzer.py
│   ├── role_fit.py
│   ├── models.py
│   └── requirements.txt
│
├── frontend/
│   ├── src/
│   ├── components/
│   ├── pages/
│   └── services/
│
└── README.md
```

---

## Backend Installation

```bash
git clone https://github.com/your-username/skillprint.git
cd skillprint/backend

python -m venv venv

# Windows
venv\Scripts\activate

# Mac/Linux
source venv/bin/activate

pip install -r requirements.txt

uvicorn main:app --reload
```

Server runs at:
http://localhost:8000

---

## Frontend Installation

```bash
cd frontend

npm install
npm run dev
```

Frontend runs at:
http://localhost:5173

---

## API Endpoints

### Analyze GitHub Profile

POST `/analyze`

Request:
```json
{
  "username": "github_username"
}
```

Response:
```json
{
  "skills": {
    "total_repositories": 12,
    "total_stars": 35,
    "top_languages": {
      "JavaScript": 6,
      "Python": 4
    }
  }
}
```

---

### Role-Fit Score

POST `/role-fit`

Request:
```json
{
  "skills": { },
  "job_description": "Looking for a React frontend developer with API experience"
}
```

Response:
```json
{
  "role_fit_score": 82
}
```

---

## Screenshots

Create a folder named `screenshots` in the project root and add your images.

### Candidate Skill Graph
![Skill Graph](screenshots/skill-graph.png)

### Company Leaderboard
![Leaderboard](screenshots/leaderboard.png)

### Real-World Challenge Generator
![Challenge](screenshots/challenge.png)

### Skill Gap Roadmap
![Roadmap](screenshots/roadmap.png)

### Architecture Diagram
![Architecture](screenshots/architecture.png)

---

## Business Model

B2B SaaS:
₹4,999 – ₹40,000 per month

Freemium for Candidates:
₹299 per month

B2B2C for Colleges:
₹2–5 Lakhs per year

---

## Roadmap

- Advanced skill embeddings
- On-device AI inference
- Multi-language JD support
- Enterprise hiring analytics
- National-scale repository analysis

---

## Core Principle

No automated rejection.
AI assists.
Humans decide.

---

