# Weighing Cup Lump Rubber using 3-Dimensional Scale
HireSense is an AI-powered resume analysis web application that uses a Retrieval-Augmented Generation (RAG) pipeline to semantically search and summarize resumes.
The system enables HR users to upload PDF resumes, retrieve relevant candidates based on job requirements, and generate concise, LLM-based summaries to support faster and more accurate screening decisions.

## ⭐ Motivation
The recruitment process often requires HR teams to manually review a large number of resumes, which is time-consuming, repetitive, and prone to human bias.
As a computer engineering student with a strong interest in AI and backend systems, I wanted to explore how Large Language Models (LLMs) and vector search can be applied to solve real-world problems.
HireSense was created to experiment with an AI-powered resume analysis system that can automatically index resumes, retrieve relevant candidates based on job requirements, and generate concise summaries to support faster and more informed hiring decisions.

## 🔑 Key Features
- Resume Upload & Parsing : Upload PDF resumes and automatically extract text content for further processing.
- Semantic Resume Search (RAG-based) : Search resumes using natural language queries (e.g., “AngularJS developer”) with vector similarity instead of keyword matching.
- AI-Powered Resume Summarization : Use LLMs to summarize candidate profiles, highlight matching skills, relevant experience, and potential gaps.
- Interactive Web Interface : A modern web UI that allows HR users to upload resumes, search candidates, and view AI-generated results in real time.

<h2 align="left">🛠️ Tech Stacks</h2>

###
Python | C++ | OpenCV | Arduino IDE | 3D Camera (Intel Realsense) | blender
<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="40" alt="python logo"  />
  <img width="12" />
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/18/ISO_C%2B%2B_Logo.svg/500px-ISO_C%2B%2B_Logo.svg.png" height="40" alt="cplus logo"  />
  <img width="12" />
  <img src="https://images.icon-icons.com/2699/PNG/512/opencv_logo_icon_170887.png" height="40" alt="opencv logo"  />
  <img width="12" />
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/73/Arduino_IDE_logo.svg/960px-Arduino_IDE_logo.svg.png" height="40" alt="arduino logo"  />
  <img width="12" />
  <img src="https://www.thailand.intel.com/content/dam/www/central-libraries/us/en/images/2025-07/real-sense-logo-rgb.png" height="40" alt="realsense logo"  />
  <img width="12" />
  <img src="https://www.techspot.com/images2/downloads/topdownload/2014/06/Blender.png" height="40" alt="blender logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" height="40" alt="vscode logo"  />
</div>

## 📚 What I Learned
- How to design and implement an end-to-end Retrieval-Augmented Generation (RAG) pipeline
- Practical use of vector databases (FAISS) for semantic document retrieval
- Integrating LLMs into backend services with controlled prompts and context management
- Designing clean API architectures for AI-driven applications
- Bridging frontend and backend systems in a full-stack AI project

## ⚙️ Architecture (RAG Pipeline)
<div align="center">
  <img src="https://github.com/Wisawathep/ReadmeTools/blob/main/HireSense/HireSense%20Architecture%201.png" height="600"  />
  <img width="12" />
  <img src="https://github.com/Wisawathep/ReadmeTools/blob/main/HireSense/HireSense%20Architecture%202.png" height="600"  />
  <img width="12" />
</div>

# 🧱 File Directory Structure
```
HireSense/
├── frontend/                          # Next.js Frontend (UI Layer)
│   ├── src/app/
│   │   ├── page.js                    # Landing page
│   │   ├── workspace/
│   │   │   └── page.js                # Main workspace UI (upload, search, analyze)
│   │   └── layout.js                
│   ├── public/                        # Static assets
│   └── package.json
│
├── backend/                           # FastAPI Backend (API & AI Layer)
│   ├── app/
│   │   ├── main.py                    # FastAPI entry point
│   │   │
│   │   ├── api/                       # API routes
│   │   │   ├── health.py              # Health check endpoint
│   │   │   ├── resumes.py             # Resume upload / list / delete APIs
│   │   │   ├── search.py              # Resume search based on job requirements (RAG-based)
│   │   │   └── analyze.py             # Resume analysis (RAG-based)
│   │   │
│   │   ├── core/                      # Core configuration
│   │   │   ├── config.py              # Environment & settings
│   │   │   └── logging.py             # Logging configuration
│   │   │
│   │   ├── schemas/                   # Pydantic schemas
│   │   │   ├── resume.py              # Resume-related schemas
│   │   │   ├── search.py              # Search schemas
│   │   │   └── analyze.py             # Analysis request/response schemas
│   │   │
│   │   ├── services/                  # Business & AI logic
│   │   │   ├── parsing/
│   │   │   │   └── pdf_parser.py      # PDF resume parser
│   │   │   │
│   │   │   ├── chunking/
│   │   │   │   └── chunker.py         # Resume text chunking
│   │   │   │
│   │   │   ├── embedding/
│   │   │   │   └── embeddings.py      # Transform Chunked Text --> vector
│   │   │   │
│   │   │   ├── vector_store/
│   │   │   │   └── faiss_store.py     # FAISS vector database
│   │   │   │
│   │   │   ├── llm/
│   │   │   │   ├── provider.py        # LLM provider (Gemini)
│   │   │   │   └── .env               # LLM API keys
│   │   │   │
│   │   │   └── rag/
│   │   │       └── rag_chain.py       # RAG pipeline & agent
│   │   │
│   │   └── utils/                     # Utility helpers
│   │       └── file_handler.py        # File save / delete helpers
│   │
│   ├── requirements.txt
│   └── .env                           # Backend environment variables
│
├── .gitignore
└── README.md
```

## 📜 Result
<div align="center">
  <img src="https://github.com/Wisawathep/ReadmeTools/blob/main/HireSense/homepage_final1.png" height="600"  />
  <img width="12" />
  <img src="https://github.com/Wisawathep/ReadmeTools/blob/main/HireSense/homepage_final2.png" height="600"  />
  <img width="12" />
  <img src="https://github.com/Wisawathep/ReadmeTools/blob/main/HireSense/homepage_final4.png" height="600"  />
  <img width="12" />  
  <img src="https://github.com/Wisawathep/ReadmeTools/blob/main/HireSense/workspace_final1.png" height="600"  />
  <img width="12" />  
  <img src="https://github.com/Wisawathep/ReadmeTools/blob/main/HireSense/upload_final.png" height="600"  />
  <img width="12" />  
  <img src="https://github.com/Wisawathep/ReadmeTools/blob/main/HireSense/added_resumes_final.png" height="600"  />
  <img width="12" />  
  <img src="https://github.com/Wisawathep/ReadmeTools/blob/main/HireSense/search_final.png" height="600"  />
  <img width="12" />  
  <img src="https://github.com/Wisawathep/ReadmeTools/blob/main/HireSense/result_final.png" height="600"  />
</div>

***

<h5 align="center">COMPUTER ENGINEERING<br>KING MONGKUT'S UNIVERSITY OF TECHNOLOGY NORTH BANGKOK, A.Y. 2023/27</h5>
<p align="center">
  <img width="100" height="100" src="https://github.com/Wisawathep/ReadmeTools/blob/main/Kmutnb/Logo.png">
</p>
