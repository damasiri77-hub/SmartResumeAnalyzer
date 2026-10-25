# Smart Resume Analyzer with AI-Based Feedback
## Project Report

**Project type:** AI Capstone Prototype  
**Application:** Web-based resume analysis  
**Technology:** Python, Flask, HTML, CSS, PyMuPDF, python-docx

## 1. Abstract
The Smart Resume Analyzer is a web application prototype intended to help students review their resumes against a selected job role. It extracts text from PDF or DOCX documents, checks for common resume sections, compares literal keywords with a role-specific checklist, calculates an explainable heuristic score, and produces improvement suggestions. The prototype demonstrates basic text processing, rule-based decision logic, and web application integration.

## 2. Problem Statement
Students may be unsure whether their resumes clearly present contact information, education, skills, projects, experience, and certifications. They may also overlook skills mentioned in job descriptions. The project provides a simple first-pass checklist and role-keyword comparison to support resume improvement.

## 3. Objectives
- Accept a resume in PDF or DOCX format.
- Extract readable text from the uploaded document.
- Calculate a transparent score using predefined rules.
- Compare resume text with keywords associated with a chosen role.
- Identify sections and keywords that were not detected.
- Display actionable feedback through a browser-based dashboard.

## 4. Scope
The prototype supports four target roles: Data Analyst, Web Developer, AI Engineer, and Cloud Engineer. It uses a small, hand-authored keyword list for each role. It does not train a machine-learning model or make hiring decisions.

## 5. Technology Stack
- **Python:** core logic and text processing.
- **Flask:** web routing and request handling.
- **PyMuPDF:** text extraction from text-based PDF files.
- **python-docx:** text extraction from DOCX files.
- **HTML/CSS:** user interface and responsive dashboard.
- **Regular expressions:** word counting and simple text handling.

## 6. System Workflow
1. User opens the web page.
2. User uploads a PDF or DOCX resume and selects a target role.
3. Flask validates the file extension and size.
4. The extraction module reads the document text.
5. The analyzer checks for common sections and action words.
6. The analyzer compares role keywords with resume text.
7. The application calculates a heuristic score and prepares feedback.
8. The dashboard presents results and allows printing/saving the report.

## 7. Module Description
### Module 1: Resume Upload and Parsing
The form accepts PDF and DOCX files. PyMuPDF extracts PDF text, while python-docx reads DOCX paragraphs and tables. Unsupported or unreadable files display an error message.

### Module 2: Resume Score Analyzer
The score is based on section presence, approximate word-count range, action verbs, email presence, and role-keyword coverage. The result is a heuristic out of 100 intended for demonstration, not an official ATS rating.

### Module 3: ATS Keyword Checker
Each supported job role has a predefined list of keywords. The application checks whether each phrase occurs in the extracted text and lists matched and missing terms.

### Module 4: Smart Feedback System
Feedback is generated from missing sections and missing role keywords. It also suggests adding measurable results where appropriate. Users should include only accurate skills and experiences.

### Module 5: Dashboard and Report
The dashboard shows the score, word count, keyword counts, section checklist, and suggestions. A print control lets users print or save the result as a PDF.

## 8. Scoring Logic
The score combines:
- Section checklist: up to 40 points.
- Word-count range: up to 20 points.
- Action verbs: up to 15 points.
- Email presence: up to 10 points.
- Role keyword coverage: up to 15 points.

The total is capped at 100. The weights are prototype design choices and have not been validated against recruiter or ATS outcomes.

## 9. Testing Plan
Test cases to run before submission:
1. Upload a text-based PDF and confirm analysis appears.
2. Upload a DOCX and confirm analysis appears.
3. Select different roles and confirm keyword results change.
4. Upload a file with an unsupported extension and confirm a helpful error appears.
5. Submit the form without a file and confirm validation feedback appears.
6. Test a scanned PDF and document the limitation if no text can be extracted.
7. Use the print control and save a sample report as PDF.

**Record actual outcomes after running the app. Do not claim tests passed until you have executed them.**

## 10. Limitations
- Literal keyword matching does not understand synonyms or meaning.
- Scanned PDFs without embedded text are not supported by OCR.
- Keyword lists are small and manually defined.
- The scoring weights are heuristic and are not an official ATS metric.
- The app is a local prototype and has not been production-hardened.
- The project does not guarantee interviews, job offers, or hiring success.

## 11. Future Enhancements
- Add OCR for scanned documents.
- Allow users to paste a job description and extract relevant skills.
- Expand and maintain role-specific skill dictionaries.
- Add tests and accessibility checks.
- Add an optional database with explicit consent and secure data retention.
- Evaluate the scoring method using a carefully designed, consent-based sample dataset.
- Deploy to a hosting platform after configuring production settings.

## 12. Conclusion
The Smart Resume Analyzer demonstrates a practical workflow combining file handling, text extraction, rule-based scoring, keyword matching, feedback generation, and a web dashboard. It is a useful educational prototype that can be extended with more robust NLP and evaluation methods.

## References
- Flask documentation: https://flask.palletsprojects.com/
- PyMuPDF documentation: https://pymupdf.readthedocs.io/
- python-docx documentation: https://python-docx.readthedocs.io/
- Python documentation: https://docs.python.org/3/

## Submission Checklist
- [ ] Run the app locally and test PDF and DOCX uploads.
- [ ] Capture screenshots of the running application.
- [ ] Replace any placeholders in the presentation/report with actual details.
- [ ] Create a GitHub repository and upload the source code.
- [ ] Deploy the application if required and verify the public URL.
- [ ] Record a short demo video.
