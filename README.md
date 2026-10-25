# Smart Resume Analyzer with AI-Based Feedback

A beginner-friendly Flask web prototype for resume text extraction, rule-based scoring, role-keyword matching, and feedback.

## Features
- Upload a text-based PDF or DOCX resume (maximum 5 MB)
- Select Data Analyst, Web Developer, AI Engineer, or Cloud Engineer
- Check for common resume sections
- Calculate an explainable prototype score out of 100
- Compare literal keywords with a role checklist
- Generate suggestions and print/save the results as PDF

## Requirements
- Python 3.10 or later recommended
- Internet connection for the first-time package installation

## Run on Windows
1. Extract this ZIP file.
2. Open the `Smart_Resume_Analyzer` folder in File Explorer.
3. Click the folder address bar, type `cmd`, and press Enter.
4. Create a virtual environment:
   `py -m venv .venv`
5. Activate it:
   `.venv\\Scripts\\activate`
6. Install dependencies:
   `python -m pip install -r requirements.txt`
7. Start the app:
   `python app.py`
8. Open `http://127.0.0.1:5000` in your browser.
9. Upload a sample resume and test different roles.

If `py` does not work, try `python` in its place. If installation fails, copy the exact terminal error and troubleshoot it before the demo.

## How it works
1. Flask receives the uploaded file.
2. PyMuPDF extracts PDF text; python-docx extracts DOCX text.
3. Rule-based checks look for common resume sections and action words.
4. A role-specific keyword list is compared with the extracted text.
5. The page displays a score, detected sections, matched/missing keywords, and suggestions.

## Limitations
- This is an educational prototype, not a real commercial ATS.
- The score is heuristic and is not validated against hiring outcomes.
- Keyword matching is literal; synonyms and context may be missed.
- Scanned/image-only PDFs may need OCR, which is not included.
- No resume is intentionally written to a database or disk by the app.
- The Flask development server is for local demonstrations, not production deployment.
- Never add fake skills or experience to a real resume.

## Suggested demo
1. Start the app.
2. Upload a text-based sample resume.
3. Select AI Engineer.
4. Show score, section checklist, matched and missing keywords, and feedback.
5. Repeat with Data Analyst to demonstrate role-specific keyword matching.
6. Use Print / Save report as PDF.

## Project deliverables
- Source code: `app.py`, `templates/`, `static/`
- Documentation: `PROJECT_REPORT.md`
- Presentation outline: `PRESENTATION_OUTLINE.md`
- Demo narration: `DEMO_SCRIPT.md`
- GitHub and deployment: see the report and README. Create these links yourself after publishing; no repository or deployment has been created automatically.
