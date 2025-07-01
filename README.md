# CruitFit: Your Smart Resume Ranker 🚀

CruitFit is a powerful, NLP-driven tool designed to automate and enhance the resume screening process. It intelligently ranks candidates by analyzing a job description against a folder of resumes, saving you time, reducing bias, and helping you find the best fit for the role.

---

## 📖 Table of Contents

- [What is CruitFit?](#what-is-cruitfit)
- [Key Features](#-key-features)
- [How It Works](#️-how-it-works)
- [Technology Stack](#-tech-we-used)
- [Installation Guide](#-how-to-get-started)
- [How to Use](#️-the-workflow-from-start-to-finish)
- [Future Roadmap](#-whats-next)
- [Contributing](#-contributing)
- [License](#-license)
- [Creator](#creator)

---

## What is CruitFit?

CruitFit is a resume ranking system built with Python and NLP. It scores, ranks, and analyzes resumes against a job description to help hiring teams quickly identify the best candidates.

---

## ✨ Key Features

- **Intelligent Skill Matching**  
  Goes beyond keywords to analyze skill importance in the job description and proficiency levels in resumes.

- **ATS Friendliness Score**  
  Evaluates how well a resume is optimized for Applicant Tracking Systems (ATS), considering parsing, structure, and content.

- **Automated SWOT Analysis**  
  Generates a Strengths, Weaknesses, Opportunities, and Threats analysis for each candidate profile.

- **Data-Driven Ranking**  
  Provides a ranked list of candidates with a final match score, helping you focus on top contenders.

- **Educational Verification**  
  Automatically checks if candidates meet the minimum educational requirements for the role.

- **Visual Insights**  
  Generates a treemap visualization of the most critical skills required for the job.

---

## ⚙️ How It Works

The system follows a multi-step process to evaluate candidates:

### 1. Analyzing the Job Description
- Extracts skills using a contextual keyword-based engine.
- Assigns importance scores using phrases like "must have", "preferred", etc.

### 2. Analyzing the Resumes
- **Skill Proficiency**: Assesses how proficient a candidate is in key skills.
- **Education**: Compares degrees against job requirements.
- **ATS Score**:
  - Parsing Compatibility
  - Structural Quality
  - Content Optimization
  - Formatting & Readability
  - Keyword Density

### 3. Scoring and Ranking
- Calculates:
  - **Skill Match Score** based on importance vs. proficiency.
  - **Final Score** combining all metrics.

### 4. Generating the SWOT Analysis
- **Strengths**: High-proficiency skills critical to the job.
- **Weaknesses**: Important skills with low proficiency.
- **Opportunities**: Bonus skills not required by the job.
- **Threats**: Critical job skills missing in the resume.

---

## 🛠️ Tech We Used

Built using Python 3 with the following libraries:

- **spaCy** – NLP engine
- **PyMuPDF (fitz)** – PDF text extraction
- **NumPy** – Numerical analysis
- **Matplotlib + Squarify** – Skill treemap visualization
- **Textstat** – Resume readability analysis
- **NLTK** – Language processing support
- **language-tool-python** – Grammar/style checking

---

## 💻 How to Get Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/CruitFit_Resume_Ranker.git
cd CruitFit_Resume_Ranker
