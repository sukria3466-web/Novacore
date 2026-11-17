# Novacore — RAG MVP

A starter retrieval-augmented chat app with a mobile-friendly web interface.

## What is included
- FastAPI backend
- Upload PDF, DOCX, TXT and Markdown documents
- Local SQLite document/chunk storage
- Sentence-transformer embeddings and cosine retrieval
- Optional Gemini answer generation (without exposing the API key to the browser)
- Responsive web chat UI

## Run locally
1. Install Python 3.11 or newer.
2. Open a terminal in `backend/`.
3. Create a virtual environment and install dependencies:
   `python -m venv .venv`
   `pip install -r requirements.txt`
4. Copy `.env.example` to `.env` and optionally add a Gemini API key.
5. Start the API:
   `uvicorn main:app --host 0.0.0.0 --port 8000`
6. Serve `frontend/` with any static web server, then set `API_BASE` in `frontend/app.js` to your backend URL.

For deployment, deploy the backend as a Python web service with persistent disk storage and set `GEMINI_API_KEY` as a server-side environment variable. Do not commit `.env`.

## Important
This is an MVP starter, not a published Android APK or a deployed service. The backend must be hosted before the app works over the internet. The first embedding-model download needs internet access.
