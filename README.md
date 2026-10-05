AI Job Description Matcher

📌 Project Overview

AI Job Description Matcher is an AI/ML-based application that helps job seekers understand how well their resume matches a particular job description.

The user uploads a resume and provides a job description. The system analyzes both and generates a match report containing:

Match percentage

Matching skills

Missing skills

Recommended skills to learn

The project combines a Flutter frontend with a Python/FastAPI AI backend.

🎯 Objectives

Compare a candidate's resume with a job description.

Identify skills that match the job requirements.

Detect missing or insufficient skills.

Calculate an overall resume-job match percentage.

Recommend skills that can improve the candidate's profile.

Provide the result through a simple and user-friendly interface.

🏗️ Proposed Architecture

User
  │
  ▼
Flutter Mobile/Web App
  │
  │ REST API / JSON
  ▼
FastAPI Backend
  │
  ├── Resume Parser
  ├── Skill Extractor
  ├── NLP / Embeddings
  ├── Matching Engine
  └── Recommendation Module
  │
  ▼
Analysis Result
  │
  ▼
Flutter Result Screen

🛠️ Technology Stack

Frontend

Flutter

Dart

HTTP package

File Picker

Backend

Python

FastAPI

Uvicorn

AI/ML & NLP

Sentence Transformers

scikit-learn

NLP-based text processing

Resume and job-description similarity

Resume Processing

PDF text extraction using PyPDF

Future Database Options

Firebase

MongoDB

✨ Main Features

1. Resume Upload

The user can select and upload a resume, preferably in PDF format.

2. Job Description Input

The user can paste the job description into the application.

3. Resume Parsing

The backend extracts readable text from the uploaded resume.

4. Skill Extraction

Important technical and job-related skills are identified from the resume and job description.

5. Match Percentage

The system calculates an overall similarity/match score.

6. Matching Skills

Skills found in both the resume and job description are displayed.

7. Missing Skills

Important job requirements that are not found in the resume are displayed.

8. Skill Recommendations

The system recommends skills that the candidate can learn to improve their match.

🔌 API Contract

Endpoint

POST /api/analyze

Input

Resume PDF

Job description text

Example Output

{
  "match_percentage": 78.5,
  "matching_skills": [
    "Python",
    "SQL",
    "Machine Learning"
  ],
  "missing_skills": [
    "Docker",
    "AWS"
  ],
  "recommended_skills": [
    "Docker",
    "AWS",
    "FastAPI"
  ]
}

📁 Suggested Project Structure

AI-Job-Description-Matcher/
│
├── frontend/
│   └── job_matcher_app/
│       ├── lib/
│       │   ├── main.dart
│       │   ├── screens/
│       │   ├── services/
│       │   ├── models/
│       │   └── widgets/
│       └── pubspec.yaml
│
├── backend/
│   ├── main.py
│   ├── requirements.txt
│   ├── api/
│   ├── services/
│   │   ├── resume_parser.py
│   │   ├── skill_extractor.py
│   │   ├── matcher.py
│   │   └── recommender.py
│   ├── models/
│   │   └── schemas.py
│   └── tests/
│
└── README.md

👥 Team Members

Madhu Chauhan — AI/ML & Backend Developer

Responsibilities:

Python backend

FastAPI APIs

Resume PDF parsing

NLP processing

Skill extraction

Resume-JD matching

Match percentage calculation

Missing skill detection

Skill recommendation logic

Backend testing

Anand Kumar — Flutter/App Developer

Responsibilities:

Flutter UI

Resume upload screen

Job description input

Result screen

API integration

Loading states

Error handling

Frontend testing

User experience

🔄 Development Workflow

Build the Flutter UI.

Create the FastAPI backend.

Create the /api/analyze endpoint.

First connect Flutter with dummy JSON data.

Test the complete frontend-backend flow.

Add PDF resume extraction.

Add skill extraction.

Add NLP/embedding-based matching.

Add missing-skill detection.

Add recommendations.

Test with different resumes and job descriptions.

Improve accuracy and UI.

🚀 Getting Started

Frontend

cd frontend
flutter pub get
flutter run

Backend

cd backend
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload

Backend API:

http://127.0.0.1:8000

Swagger API documentation:

http://127.0.0.1:8000/docs

📊 Example Result

Match Percentage: 78.5%

Matching Skills:
✓ Python
✓ SQL
✓ Machine Learning

Missing Skills:
✗ Docker
✗ AWS

Recommended Skills:
→ Docker
→ AWS
→ FastAPI

🔮 Future Scope

Support DOCX resumes

Improve skill extraction using advanced NLP

Add semantic similarity using transformer models

Add job recommendation

Add resume improvement suggestions

Add ATS-friendly resume analysis

Add user login and history

Store previous analyses

Add cloud deployment

Add multilingual support

📌 Project Goal

The main goal of this project is to provide a simple AI-powered tool that helps candidates understand their suitability for a job and identify the skills they should improve before applying.

👨‍💻 Team

Madhu Chauhan — AI/ML & Backend
Anand Kumar — Flutter & Frontend
