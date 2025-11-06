# 🧠 Codebase Genius


**Codebase Genius** is an AI-powered, agentic system designed to automatically generate **comprehensive documentation** for any given GitHub repository.

---

## 🚀 Overview

The system uses a **multi-agent architecture** where each agent performs a specific task—file structure parsing, semantic understanding, diagram generation, and final documentation writing.  
These agents **collaborate in a pipeline** to analyze repositories (especially those in **Python** and **Jac**) and produce structured markdown documentation with visual diagrams.

---

## 🎯 Project Scope

- Accept a **GitHub repository URL**
- Analyze its **file structure** and **code relationships**
- Build a **Code Context Graph (CCG)**
- Automatically generate **human-readable markdown documentation** and **visual diagrams**

---

## 🧩 Core Agents

- **Supervisor (Code Genius Agent):** Oversees workflow and ensures cohesive outputs  
- **Repo Mapper:** Maps the file tree and summarizes the README  
- **Code Analyzer:** Parses and interprets source code relationships  
- **DocGenie:** Generates the final markdown documentation and diagrams  

---

## 🔄 Workflow

```mermaid
flowchart LR
    A[Clone Repo] --> B[Analyze Structure]
    B --> C[Summarize README]
    C --> D[Plan Documentation]
    D --> E[Analyze Code]
    E --> F[Generate Final Docs]

## 🪛Installation
1.Install Python3.12 or higher

2.Set up a virtual environment:
```
python -m venv jac-env
source jac-env/bin/activate   # Linux/Mac
jac-env\Scripts\activate      # Windows
```
3.Install Dependancies:
```bash
## Backend dependancies
pip install jaseci
pip install astroid
pip install jedi
pip install gitpython
pip install byllm
pip install python-dotenv

## frontend dependancies
pip install streamlit
pip install requests
```

4. Set up your GEMINI API key
```
export GEMINI_API_KEY="your_api_key_here"   # Linux/Mac
setx GEMINI_API_KEY "your_api_key_here"     # Windows
```


### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Catemwas/codebase.git
cd <codebase >

## Running the application
### 1. Start the Backend Server
From the project root directory:
```bash
cd backend
jac serve main.jac
```
The  server will start on `http://localhost:8000`

### 2. Start the Frontend Application
In a new terminal, from the project root directory:
```bash
cd frontend
streamlit run app.py
```
The Streamlit interface will open in your default web browser at `http://localhost:8501`

## Output and Documentation
- Generated documentation and analysis results are stored in the `outputs/repository` directory
- Documentation is generated in markdown format (`docs.md`)

## License
This project is licensed under the MIT License - see the LICENSE file for details.
