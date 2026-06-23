#  Question Generator using n8n

## Overview

AI PDF Question Generator is an automated workflow built with n8n that extracts content from PDF documents and generates educational questions using Large Language Models (LLMs).

The system is designed for teachers, content creators, and e-learning platforms to automatically create question banks from study materials. Users simply upload a PDF file, and the workflow processes the content and generates structured questions which are exported as a TXT file.

---

## Features

* Upload PDF documents through a web form
* Automatic PDF text extraction
* AI-powered question generation
* Multiple difficulty levels:
  * Easy
  * Medium
  * Hard
* CBSE-style educational question generation
* Fully automated workflow using n8n
* Export generated questions as TXT file
* No manual content extraction required

---

## Workflow

1. User uploads a PDF file.
2. n8n extracts text from the PDF.
3. Extracted content is sent to an LLM.
4. AI generates questions based on the document.
5. Questions are categorized by difficulty level.
6. Generated questions are processed.
7. Output is converted into a TXT file.
8. User downloads the generated question bank.


## Workflow Screenshot

<img width="1403" height="511" alt="Screenshot 2026-06-23 101235" src="https://github.com/user-attachments/assets/081cc40a-61ef-4700-b77a-61c6337ba87f" />
---

## Tech Stack

### Workflow Automation

* n8n

### AI Model

* Google Gemini API

### File Processing

* PDF Text Extraction Node
* Convert to File Node

### Programming

* JavaScript

### Output Format

* TXT File

---

## Project Structure

```text
AI-PDF-Question-Generator/
│
├── workflow/
│   └── Question PDF Generator.json
│
├── input/
│   └── input.pdf
│
├── output/
│   └── output.txt
│
├── screenshots/
│   ├── workflow.png
│  
│
└── README.md
```

### Input

```text
input/
└── input.pdf
```

The user uploads a PDF containing educational content.

### Output

```text
output/
└── output.txt
```

Generated question bank is exported as a TXT file.

---

## n8n Workflow Architecture

```text
Form Trigger
      ↓
PDF Upload
      ↓
Extract Text from PDF
      ↓
Google Gemini
      ↓
Generate Questions
      ↓
JavaScript Processing
      ↓
Convert to TXT File
      ↓
Download Output
```

---

## How to Use

### Prerequisites

* n8n installed
* Google Gemini API Key
* Internet Connection

### Steps

1. Clone this repository.

```bash
git clone https://github.com/your-username/ai-pdf-question-generator.git
```

2. Open n8n.

3. Import:

```text
Question PDF Generator.json
```

4. Configure your Gemini API credentials.

5. Activate the workflow.

6. Open the generated form URL.

7. Upload a PDF file.

8. Wait for processing.

9. Download the generated TXT file.

---

## Example Input

```text
Chapter: Electromagnetic Waves

Topics:
- Displacement Current
- Maxwell's Equations
- Electromagnetic Spectrum
- EM Wave Properties
```

---

## Example Output

```text
EASY LEVEL

Q1. What is displacement current?

Q2. Who predicted electromagnetic waves?

Q3. Define electromagnetic spectrum.

Q4. What is the speed of EM waves in vacuum?

Q5. Name two applications of radio waves.

MEDIUM LEVEL

Q1. Explain the role of displacement current.

Q2. Why are electric and magnetic fields perpendicular in EM waves?

Q3. Differentiate between radio waves and gamma rays.

Q4. Explain Maxwell's contribution to EM wave theory.

Q5. Describe the electromagnetic spectrum.

HARD LEVEL

Q1. Derive the relation c = 1/√(μ₀ε₀).

Q2. Calculate magnetic field strength for a given electric field.

Q3. Explain the generation of electromagnetic waves.

Q4. Analyze the significance of Maxwell's equations.

Q5. Solve a numerical problem based on EM wave propagation.
```

---

## Future Improvements

* Support DOCX and PPT files
* Generate answers along with questions
* Export directly to PDF
* Difficulty-level customization
* MCQ generation support
* Bloom's Taxonomy-based question generation
* Multi-language support
* Chapter-wise question bank generation
* Question quality scoring
* OpenAI and Claude model integration
* Database storage for generated questions
* User authentication and dashboard

---

## Use Cases

* Educational Institutions
* Teachers and Professors
* Coaching Centers
* E-learning Platforms
* Exam Preparation Portals
* Automated Question Bank Creation

