CruitFit: Your Smart Resume Ranker
Created by: Naman Pandey
Version: 1.0
Find the code here: [Link to GitHub Repository]

What is CruitFit?
Screening resumes is one of the most time-consuming parts of hiring. It's a manual process that can be slow, subjective, and prone to unconscious bias. CruitFit is a powerful tool engineered to make the initial screening process significantly easier, faster, and more objective.

Using state-of-the-art Natural Language Processing (NLP), CruitFit analyzes a job description and a folder of resumes to intelligently rank each candidate. It goes beyond simple keyword matching to understand how critical a skill is for the role and to estimate the candidate's proficiency. The result is a clear, ranked list of applicants, complete with an ATS (Applicant Tracking System) compatibility score and a concise SWOT analysis (Strengths, Weaknesses, Opportunities, Threats) for each profile. CruitFit is designed to give you a smart, data-backed head start in your hiring process.

How It Works
The system operates in a few key steps, breaking down the text from the job description and resumes to perform a comprehensive analysis.

1. Analyzing the Job Description
First, CruitFit determines the core requirements of the role by analyzing the job description.

Identifying Key Skills: The tool references an extensive list of skills to identify relevant competencies in the job description. It then weighs the importance of each skill based on contextual keywords. For instance, words like "must have" or "required" signify a critical skill, while "nice to have" or "familiar with" indicate a bonus. This process generates a "skill importance" score for the role.

2. Analyzing the Resumes
Next, CruitFit performs a deep dive into each resume PDF to evaluate how candidates measure up.

Gauging Skill Levels: It identifies skills in the resume and assigns a "proficiency" score based on context. This score considers not only the presence of a skill but also phrases like "expert in," "managed," or "developed," which suggest a higher level of experience than "exposure to" or "learning."

Checking Education: The tool extracts educational qualifications (e.g., Bachelor's, Master's, PhD) and verifies them against the requirements specified in the job description.

The ATS Friendliness Score: This score predicts how well a resume will be parsed by automated screening software. It's a composite metric calculated from several factors:

| Factor | What it Means in Plain English |
| Parsing Compatibility | Can a computer read this? Checks for non-standard file types, special characters, or complex layouts that can confuse an ATS. |
| Structural Quality | Is it well-organized? Looks for standard sections (Experience, Education, Skills), clear contact information, and consistent date formats. |
| Content Optimization | Is the content impactful? Checks for action verbs ("led," "created," "improved") and quantifiable achievements (e.g., "increased sales by 20%"). |
| Formatting & Readability | Is it easy to read? Assesses document length, white space, and overall readability for a human reviewer. |
| Keyword Density | Are the right keywords included? Checks for relevant skills without "keyword stuffing," which can be penalized. |

3. Scoring and Ranking
This is where all the data points converge. CruitFit calculates a final score to rank every candidate.

Skill Match Score: The system combines the "importance" of a skill from the job description with the candidate's estimated "proficiency" from their resume.

Final Score: All individual skill scores are aggregated. This total score is then benchmarked against the maximum possible score for the role, yielding a final percentage that represents the candidate's alignment.

The Ranked List: Candidates are sorted from highest to lowest score. Anyone who doesn't meet the minimum educational requirements is flagged and listed separately, allowing for informed decision-making.

4. The SWOT Analysis
For a quick, strategic overview, the tool generates a SWOT analysis for each candidate:

Strengths: High-proficiency skills that are also critical for the job.

Weaknesses: Important skills for the job where the candidate appears to have low proficiency.

Opportunities: High-proficiency skills the candidate possesses that are not a primary requirement for the role (valuable bonus skills).

Threats: Critical job skills that appear to be missing from the resume.

The Workflow: From Start to Finish
You Provide:

The job description (copy-pasted into the terminal).

The path to a folder containing resumes in PDF format.

CruitFit Processes:

It analyzes the JD, determines what's important, and generates a visual treemap (jd_skill_treemap.png) of the key skills.

It systematically processes every resume.

It extracts all key information—skills, degrees, etc.

It calculates the final score, ATS score, and SWOT analysis for each candidate.

You Get:

A clean, ranked list of candidates printed to your terminal.

Each candidate's entry includes their final score and ATS-friendliness score.

A summary of their top skills, degrees, and the full SWOT analysis is provided.

A separate list identifies candidates who do not meet the educational requirements.

Tech We Used
This tool is built with Python 3 and several powerful open-source libraries:

spaCy: The core engine for all advanced language processing.

PyMuPDF (fitz): For reliable and efficient text extraction from PDFs.

NumPy: For the numerical computations behind the scoring algorithms.

Matplotlib & Squarify: To generate the skill importance treemap visualization.

Textstat: To calculate readability metrics.

NLTK & language-tool-python: For supplementary language analysis.

How to Get Started
Ready to run the tool? Just follow these steps.

Download the Code:

git clone https://github.com/your-username/CruitFit-Resume-Ranker.git
cd CruitFit-Resume-Ranker


Install the Tools:
It's best practice to use a virtual environment for Python projects.

python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`


Now, install the required packages:

pip install spacy pymupdf matplotlib squarify numpy language-tool-python nltk textstat


Download the Language Model:
spaCy requires its English language model to function correctly.

python -m spacy download en_core_web_sm


Run the Program:
Execute the script from your terminal.

python cruitfit_ranker.py # or whatever you named the script


The program will then prompt you to:

Paste in the job description.

Provide the path to your folder of resumes.

What's Next?
This tool provides a solid foundation, but there's always room for growth. Here are some ideas for future development:

Smarter AI: Incorporate more advanced models (like BERT) for an even deeper contextual understanding of skills and experience.

Make it Your Own: Allow users to easily customize the skill library or importance keywords for specific industries.

A Friendly Interface: Build a simple web page or desktop application to make the tool accessible to non-technical users.

Fighting Bias: Continue to research and implement fairness algorithms to actively identify and mitigate potential biases in the analysis.
