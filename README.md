# JanAudit ⚖️

### AI-Assisted Government Expenditure Analysis & RTI Support Platform

JanAudit is a civic-tech platform that uses **Artificial Intelligence, data analytics, and Retrieval-Augmented Generation (RAG)** to make government financial information easier to analyze and understand.

The platform takes government expenditure reports, extracts useful financial information, identifies potentially unusual spending patterns, and provides citizens with relevant legal context and an automatically generated **Right to Information (RTI)** draft that can be reviewed and customized before submission.

---

## 🎯 Problem Statement

Government financial documents are often available publicly, but they can be difficult for ordinary citizens to analyze because they may contain:

* Large and complex expenditure tables
* Unstructured PDF documents
* Thousands of financial records
* Difficult-to-identify spending patterns
* Legal terminology and procedures

As a result, potentially important financial irregularities may remain difficult to identify.

**JanAudit aims to reduce this barrier by combining document intelligence, statistical analysis, and legal information retrieval in a single platform.**

---

## 💡 How JanAudit Works

The application follows a simple analysis pipeline:

```text
Government Financial Report
            ↓
      PDF Processing
            ↓
   Structured Data Extraction
            ↓
    Financial Data Analysis
            ↓
   Anomaly / Pattern Detection
            ↓
   Legal Context Retrieval
            ↓
       RTI Draft Generation
            ↓
      Citizen Review & Action
```

---

## 🔍 Core Capabilities

### 1. Government Document Processing

Upload financial reports in PDF format and extract relevant expenditure information from the document.

The processing pipeline handles:

* PDF text extraction
* Tabular data processing
* Data cleaning
* Conversion into structured records

---

### 2. Financial Anomaly Analysis

JanAudit analyzes expenditure records to identify transactions that deserve further investigation.

The system can use techniques such as:

* **Z-score analysis**
* **Interquartile Range (IQR)**
* Duplicate transaction checks
* Unusual or repeated values
* Round-number spending patterns
* Statistical outlier detection

The system does **not** claim that an anomaly is automatically fraudulent. Instead, it highlights records that may warrant additional scrutiny.

---

### 3. Legal Information Retrieval

The platform uses a **RAG-based approach** to retrieve relevant information from the **Right to Information Act, 2005**.

Relevant legal information can help users understand:

* What information can be requested
* Which provisions may be relevant
* How an RTI request can be structured
* What additional clarification may be useful

This provides legal context alongside the financial analysis.

---

### 4. AI-Assisted RTI Generation

After analyzing suspicious or unusual expenditure records, JanAudit can generate a structured RTI application draft.

The generated draft can include:

* Applicant information
* Relevant department
* Questions regarding the expenditure
* References to identified records
* Information requested from the concerned authority

Users can review and modify the generated draft before using it.

---

### 5. Expenditure Dashboard

The frontend provides an interactive interface for exploring analyzed financial information.

The dashboard can display:

* Department-wise expenditure
* Spending trends
* Anomaly indicators
* Financial summaries
* Data visualizations

This makes large financial datasets easier to understand.

---

## 🧠 AI & Data Processing Architecture

JanAudit combines several techniques instead of relying on a single AI model.

### Document Intelligence

```text
PDF
 ↓
pdfplumber
 ↓
Text / Tables
 ↓
Cleaning & Structuring
 ↓
Financial Dataset
```

### Anomaly Detection

```text
Financial Records
       ↓
Data Preprocessing
       ↓
Statistical Analysis
       ↓
Outlier Detection
       ↓
Potential Anomalies
```

### Legal RAG Pipeline

```text
RTI Act Documents
       ↓
Text Processing
       ↓
Embeddings
       ↓
FAISS Vector Index
       ↓
Similarity Search
       ↓
Relevant Legal Context
```

---

## 🏗️ Technology Stack

| Layer             | Technologies               |
| ----------------- | -------------------------- |
| Frontend          | React, Vite, Chart.js, CSS |
| Backend           | Python, FastAPI            |
| Data Processing   | Pandas, NumPy, pdfplumber  |
| Machine Learning  | Scikit-learn               |
| Vector Search     | FAISS                      |
| Validation        | Pydantic                   |
| ORM               | SQLAlchemy                 |
| Database          | SQLite                     |
| API Communication | REST APIs                  |

---

## 📁 Repository Layout

```text
JanAudit/
│
├── backend/
│   ├── main.py
│   ├── ...
│   ├── requirements.txt
│   └── ...
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── ...
│
├── README.md
└── .gitignore
```

The repository contains both application layers so that the complete project can be cloned and run from a single repository.

---

## ⚙️ Running the Application Locally

### Requirements

Make sure the following are installed:

* Python 3.10 or later
* Node.js 18 or later
* npm

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
```

### 2. Start the backend

```bash
cd backend
```

Create and activate a virtual environment:

**Windows**

```bash
python -m venv venv
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start the FastAPI server:

```bash
python -m uvicorn main:app --reload
```

The backend will be available locally through the FastAPI development server.

---

### 3. Start the frontend

Open another terminal:

```bash
cd frontend
npm install
npm run dev
```

Open the local URL displayed by Vite in your browser.

---

## 🔐 Security & Configuration

Environment-specific configuration and credentials should be stored outside the repository.

For example:

```text
.env
```

should not be committed to GitHub.

A `.env.example` file can be used to document the required environment variables without exposing actual credentials.

---

## 📊 Intended Use

JanAudit is designed as an **investigative assistance and civic transparency tool**.

An anomaly detected by the system should be treated as a signal for further investigation rather than proof of financial misconduct.

The platform helps users:

**Find → Understand → Verify → Ask**

---

## 🚀 Future Improvements

Potential extensions include:

* Multilingual RTI generation
* Support for additional government datasets
* Advanced document understanding using LLMs
* Improved table extraction from scanned PDFs
* More sophisticated anomaly detection models
* Department and scheme-level comparisons
* Citation-aware legal responses
* Human-in-the-loop verification
* Deployment using cloud infrastructure
* Support for additional Indian transparency laws and regulations

---

## 👥 Project

**JanAudit** was developed as an AI-driven civic-tech project focused on improving accessibility and transparency in public financial information.

### Key Areas

`Artificial Intelligence` · `RAG` · `Document Intelligence` · `Data Analytics` · `Anomal
