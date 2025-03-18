# Resume-scoring-system

**Overview**

This Resume Scoring System is a Python-based tool that evaluates resumes based on various criteria such as language quality, experience, location match, and job relevance. The system processes PDF and DOCX resumes, extracts text, and assigns scores to help recruiters shortlist the best candidates efficiently.

**Features**

Processes PDF & DOCX resumes

Extracts job-relevant details such as experience, skills, and location

Analyzes language quality (readability, grammar)

Calculates job match scores using NLP (Spacy embeddings & keyword analysis)

Considers location proximity to give preference to local candidates

Multi-processing enabled for handling multiple resumes efficiently

Configurable weights for scoring customization

**Installation**

Ensure you have Python installed (preferably 3.8+). Install dependencies using:

pip install -r requirements.txt

**Usage**

(1) Prepare Your Files

Place resumes in a folder (e.g., resumes/)

Define your job description, location, and country

(2️) Run the Script

from resume_scoring import batch_process

weights = {'language_quality': 0.2, 'experience_quality': 0.2, 'years_of_experience': 0.2, 'location': 0.2, 'job_match': 0.2}
city = "New York"
country = "USA"
job_description = "Looking for a Software Engineer skilled in Python, Machine Learning, and Cloud Computing."
cv_files = ["resumes/Resume1.pdf", "resumes/Resume2.docx"]

scores = batch_process(cv_files, weights, city, country, job_description)
print("Candidate Scores:", scores)

**Scoring Criteria**

Language Quality (20%) - Evaluates grammar and readability of the resume.
Experience Quality (20%) - Measures relevance of work experience to the job.
Years of Experience (20%) - Calculates total work experience in years.
Location Match (20%) - Gives preference to candidates closer to the job location.
Job Match Score (20%) - Uses NLP to determine how well the resume matches the job description.

**Dependencies**

PyPDF2 (PDF text extraction)

docx (DOCX file handling)

nltk (Text processing)

spacy (NLP-based similarity matching)

textstat (Readability analysis)

language_tool_python (Grammar checking)

multiprocessing (Parallel processing for efficiency)

**Next Steps**

✅ Improve resume keyword extraction

✅ Deploy as a web API or GUI for better accessibility

✅ Optimize for large-scale resume processing

📩 Contributions & Feedback Welcome! 🚀

