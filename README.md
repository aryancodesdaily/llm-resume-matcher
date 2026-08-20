# LLM Resume Matcher

An LLM-based resume screening tool that compares candidate resumes with a given job description and generates a match score.

The application first sends the job description to an LLM and extracts structured information such as role, required skills, preferred skills, experience, education requirements, and responsibilities. Resumes are then read from PDF or DOCX files, their text is extracted, and an LLM converts the resume into structured information such as skills, education, projects, experience, and certifications.

The structured job requirements and candidate resume are then compared by an LLM to evaluate technical skill match, experience, project relevance, education, preferred skills, and overall suitability. Multiple resumes can be processed from the resumes folder and are ranked according to their generated match scores.

Tech Stack: Python, Groq API, LLM (openai/gpt-oss-120b), Pydantic, pypdf, python-docx, python-dotenv, uv.

Project structure:
```text
llm_project1/
├── resumes/
│   ├── 1_resume.docx
│   ├── 2_resume.pdf
│   └── 3_resume.docx
├── src/
├── .gitignore
├── .python-version
├── README.md
├── main.py
├── pyproject.toml
└── uv.lock
```
Setup:

Install dependencies using:

uv sync

Create a .env file in the project root and add:

GROQ_API_KEY=your_api_key_here

Place PDF or DOCX resumes inside the resumes folder and run:

uv run python main.py

The application processes each resume, extracts structured information, evaluates it against the job requirements, generates a match score, and ranks the resumes.

The resumes included in this repository are synthetic test resumes created for testing the system. The generated score is an LLM-based assessment and should not be treated as a definitive hiring decision.
