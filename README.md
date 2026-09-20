# Multi-Agent Financial Research System

## 📌 Overview

The **Multi-Agent Financial Research System** is an AI-powered platform designed to analyze financial documents such as **annual reports, financial statements, and regulatory filings**.

The system uses a team of specialized AI agents that collaboratively process financial documents, extract important financial information, identify risks and anomalies, compare company performance, answer financial questions, and generate structured research reports.

The primary goal is to **reduce the time and effort required for manual financial document analysis while providing source-grounded and transparent insights**.

---

## 🎯 Problem Statement

Financial documents are often large, complex, and difficult to analyze manually. Finance students, MBA learners, investment research trainees, and junior financial analysts may need to spend significant time:

* Finding important financial metrics
* Understanding financial statements
* Identifying financial risks
* Comparing company performance
* Answering questions from annual reports
* Preparing financial research reports

Existing general-purpose AI tools can generate summaries, but they may not always provide **reliable source verification** or comprehensive financial analysis.

This project addresses these limitations using a **collaborative multi-agent architecture** with document-grounded retrieval and source citations.

---

## 💡 Proposed Solution

The proposed system uses multiple specialized AI agents, where each agent performs a specific financial research task.

### Multi-Agent Workflow

```text
                    ┌──────────────────────┐
                    │   Financial Document │
                    │   PDF / Annual Report│
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │    Document Agent    │
                    │ Parse → Chunk → Embed│
                    │      → Index         │
                    └──────────┬───────────┘
                               │
             ┌─────────────────┼─────────────────┐
             │                 │                 │
             ▼                 ▼                 ▼
     ┌──────────────┐  ┌──────────────┐  ┌──────────────┐
     │  Extraction  │  │   Red Flag   │  │  Comparison  │
     │    Agent     │  │    Agent     │  │    Agent     │
     └──────┬───────┘  └──────┬───────┘  └──────┬───────┘
            │                 │                 │
            └─────────────────┼─────────────────┘
                              │
                    ┌─────────▼─────────┐
                    │   Research Agent  │
                    │ Source-Grounded   │
                    │ Financial Q&A      │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌──────────────────────┐
                    │     Report Agent     │
                    │ Structured Analyst   │
                    │      Report          │
                    └──────────────────────┘
```

---

## 🤖 AI Agents

### 1. Document Agent

The **Document Agent** handles the initial processing of uploaded financial documents.

Responsibilities:

* Parse financial documents
* Extract text
* Split documents into meaningful chunks
* Generate embeddings
* Index document content
* Prepare information for retrieval

---

### 2. Extraction Agent

The **Extraction Agent** identifies important financial information from the uploaded documents.

It focuses on extracting:

* Financial metrics
* Key figures
* Financial statement information
* Important numerical information

---

### 3. Red Flag Agent

The **Red Flag Agent** analyzes financial information to identify potential:

* Financial risks
* Anomalies
* Unusual patterns
* Important warning indicators

The purpose is to help users quickly identify areas that may require further investigation.

---

### 4. Comparison Agent

The **Comparison Agent** helps benchmark company performance using information available in the relevant financial documents.

It can be used to compare:

* Financial performance
* Key financial metrics
* Business indicators
* Company-level financial information

---

### 5. Research Agent

The **Research Agent** provides answers to financial questions using retrieved information from the uploaded documents.

The system emphasizes:

* Source-grounded answers
* Document-based retrieval
* Evidence-backed responses
* Accurate citations

This helps reduce unsupported information and improves transparency.

---

### 6. Report Agent

The **Report Agent** generates a structured analyst-style financial research report.

The report can organize findings such as:

* Extracted financial metrics
* Identified risks
* Comparative findings
* Research question answers
* Supporting sources and citations

---

## 🔄 System Workflow

```text
1. Upload Financial Document
             ↓
2. Document Parsing
             ↓
3. Text Chunking
             ↓
4. Embedding Generation
             ↓
5. Document Indexing
             ↓
6. Financial Information Extraction
             ↓
7. Risk & Anomaly Detection
             ↓
8. Company Performance Comparison
             ↓
9. Source-Grounded Financial Q&A
             ↓
10. Structured Research Report
```

---

## ✨ Key Features

* 📄 **Financial Document Processing**
* 🤖 **Multi-Agent AI Architecture**
* 📊 **Financial Metric Extraction**
* 🚩 **Risk and Anomaly Detection**
* 🔍 **Source-Grounded Financial Question Answering**
* 📈 **Company Performance Comparison**
* 📝 **Automated Financial Research Reports**
* 📚 **Document-Based Retrieval**
* 🔗 **Source Citations**
* 🎯 **Evidence-Based Reasoning**
* 🔒 **Document-Grounded Responses**

---

## 🧠 Technology Concepts

The project combines several AI and information-retrieval concepts:

* Multi-Agent Systems
* Retrieval-Augmented Generation (RAG)
* Natural Language Processing (NLP)
* Document Parsing
* Text Chunking
* Vector Embeddings
* Vector Database / Document Indexing
* Large Language Models (LLMs)
* Source-Grounded Question Answering
* Financial Document Analysis

---

## 📂 Project Structure

```text
multi-agent-financial-research-system/
│
├── backend/
│   ├── app/
│   │   ├── agents/
│   │   │   ├── document_agent/
│   │   │   ├── extraction_agent/
│   │   │   ├── red_flag_agent/
│   │   │   ├── comparison_agent/
│   │   │   ├── research_agent/
│   │   │   └── report_agent/
│   │   │
│   │   ├── services/
│   │   ├── models/
│   │   ├── routes/
│   │   └── main.py
│   │
│   ├── uploads/
│   ├── chroma_db/
│   ├── requirements.txt
│   └── .env.example
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── ...
│
├── docs/
│
├── .gitignore
├── README.md
└── LICENSE
```

> The exact directory structure may change as development progresses.

---

## 🚀 Getting Started

### Prerequisites

Make sure the following are installed:

* Python 3.10+
* Node.js
* npm
* Git
* A supported LLM
* Vector database / embedding dependencies

---

## 🔧 Backend Setup

Clone the repository:

```bash
git clone <YOUR_REPOSITORY_URL>
cd multi-agent-financial-research-system
```

Create and activate a Python virtual environment:

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

Install backend dependencies:

```bash
pip install -r requirements.txt
```

Create your environment configuration:

```bash
.env
```

Configure the required environment variables according to the project setup.

Run the backend:

```bash
uvicorn app.main:app --reload
```

The API will be available at:

```text
http://127.0.0.1:8000
```

API documentation:

```text
http://127.0.0.1:8000/docs
```

---

## 💻 Frontend Setup

Navigate to the frontend directory:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

The frontend will then be available through the Vite development server.

---

## 📄 Supported Documents

The system is designed to analyze financial documents such as:

* Annual reports
* Financial statements
* Regulatory filings
* Other relevant financial research documents

The system focuses on information contained within the **uploaded documents**.

---

## 🎯 Target Users

The system is primarily intended for:

* Finance students
* MBA students
* Investment research trainees
* Junior financial analysts
* Business school learners
* Users learning financial statement analysis

These users can use the system to reduce the amount of manual effort required for financial document research.

---

## 🔐 Scope and Limitations

The system is designed specifically for **financial document analysis and research**.

### The system DOES:

* Analyze uploaded financial documents
* Extract financial metrics
* Identify potential financial risks and anomalies
* Compare financial information
* Answer questions using uploaded documents
* Generate structured research reports
* Provide source-backed information

### The system DOES NOT:

* Predict stock prices
* Provide investment recommendations
* Provide financial information that is not supported by the uploaded documents

These limitations are part of the defined project scope.

---

## 📊 Expected Outcomes

The expected outcome is a reliable financial research platform that reduces manual document-analysis time while maintaining trustworthy and citation-supported responses.

The project will be evaluated based on:

* Accuracy of financial metric extraction
* Effectiveness of risk detection
* Reliability of source citations
* Efficiency of multi-agent collaboration
* Quality of generated research reports

---

## 📚 Research References

1. M. Samuelsen, W. Nyström, S. Mazumdar, M. Hussain, and M. Strange, **"MimirRAG: A Multi-Agent RAG Framework for Financial Data Retrieval with Metadata Integration,"** arXiv:2605.25030, 2026.

2. X. Chen et al., **"MENTOR: A Multi-Agent Framework for Event and Narrative Trend Prediction in Financial Markets,"** Frontiers of Information Technology & Electronic Engineering, vol. 26, no. 10, pp. 1847–1861, 2025.

3. P. Islam et al., **"FinanceBench: A New Benchmark for Financial Question Answering,"** arXiv:2311.11944, 2023.

4. A. J. Yepes et al., **"Financial Report Chunking for Effective Retrieval-Augmented Generation,"** arXiv:2402.05131, 2024.

---

## 👥 Project Team

| S. No. | Name                               |
| ------ | ---------------------------------- |
| 1      | Mohana Siva Naga Jyothi Pasupuleti |
| 2      | Kusumuru Teja                      |
| 3      | Mungara Meghana                    |
| 4      | Javvadula Shanmukha Aditya Sairam  |

**Project Guide:** Mr. M Anil Kumar

---

## 📌 Project Status

🚧 **Under Development**

The system is being developed as a multi-agent financial research platform with document processing, financial analysis, source-grounded question answering, and automated report generation.

---

## ⭐ Future Enhancements

Possible future enhancements include:

* Improved financial metric extraction
* More advanced financial risk detection
* Enhanced company comparison
* Improved citation verification
* Support for additional financial document formats
* More sophisticated multi-agent coordination
* Improved report customization
* Enhanced user interface

---

## 📜 License

This project is developed for academic and research purposes.

Add an appropriate open-source license if the project is intended to be publicly distributed.
