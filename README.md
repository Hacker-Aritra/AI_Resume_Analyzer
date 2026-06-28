# AI_Resume_Analyzer
AI-powered resume analyzer built with Streamlit &amp; spaCy — parses PDF resumes, predicts career fields, recommends skills/courses, scores resumes, and includes an admin analytics dashboard.


AI Resume Analyzer is a Streamlit-based web application that uses Natural Language Processing to help job seekers evaluate and improve their resumes, while giving recruiters/admins a dashboard to track applicant data.

What it does

Resume Parsing — Upload a PDF resume and the app automatically extracts key details: name, email, phone number, degree, skills, and number of pages, using `pyresparser` and `spaCy` under the hood.
Career Field Prediction — Based on the skills detected, the app classifies the candidate into a likely career track (Data Science, Web Development, Android, iOS, or UI/UX).
Skill Gap & Recommendations — Once a field is predicted, the app suggests additional in-demand skills the candidate should consider adding to stay competitive in that field.
Course Recommendations — Surfaces curated Udemy, Coursera, and free course links relevant to the predicted career field, so users have a clear next step for upskilling.
Resume Scoring — Assigns a score out of 100 based on the completeness of standard resume sections (objective, experience, education, skills, etc.), along with actionable tips for improvement.
Admin Dashboard — A separate login-protected view where an admin can see all user submissions, browse/download collected data as CSV, and explore interactive Plotly visualizations (e.g., breakdown by predicted field, experience level, location).
Feedback System — Users can rate their experience and leave comments, which are stored and visualized for the admin.

How it's built

- Frontend/UI: Streamlit (single-page interactive web app, no separate frontend framework needed)
- NLP/Parsing: spaCy + pyresparser + pdfminer3 for extracting structured data from unstructured PDF text
- Data handling: pandas / NumPy
- Visualization: Plotly for interactive charts in the admin dashboard
- Database: MySQL (via PyMySQL) to persist user submissions and feedback
- Geolocation: geocoder/geopy, likely used to map applicant location data for the admin view
- Config: Environment-variable based (`.env`) — no hard-coded credentials, DB/admin settings configurable per deployment

Why it's useful

It's a practical end-to-end example of applying NLP to a real-world HR/job-search problem — combining resume parsing, classification, and recommendation in one tool, while also demonstrating a full-stack pattern (Streamlit frontend + MySQL backend + admin analytics) that's easy to self-host and extend (e.g., the roadmap mentions DOCX support, more career fields like Cloud/DevOps/Cybersecurity, PDF report export, and Dockerizing the setup).

It's a good portfolio project to showcase NLP + data app skills, or a starting point for anyone building an internal resume-screening tool.
