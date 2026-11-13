# AuraSync Wellness Mart - RAG Health & E-Commerce Assistant

An academic Retrieval-Augmented Generation (RAG) assistant built for **AuraSync Wellness Mart** in Karachi, Pakistan. The system provides reliable answers regarding product stock, PKR pricing, and store policies backed by official vector documents, combined with explicit Python tool functions.

---

## 🛠️ Tech Stack & Architecture
- **Frontend UI:** Streamlit (`app.py`)
- **Backend Pipeline:** Procedural Python RAG logic (`rag_pipeline.py`)
- **Custom Tools:** LangChain `@tool` decorated functions (`tools.py`)
- **Vector Store:** ChromaDB with **HNSW Indexing** and **Cosine Similarity** (`collection_metadata={"hnsw:space": "cosine"}`)
- **Embeddings:** Free local HuggingFace model (`all-MiniLM-L6-v2`)
- **LLM API:** Groq Free Tier (`llama3-8b-8192`) via official Groq SDK
- **Environment:** `python-dotenv` (`.env`)

---

## 📁 Project Directory Structure
```text
aurasync_rag_project/
│
├── venv/                     # Python Virtual Environment
├── knowledge_base/           # Official PDF knowledge base
│   ├── company_overview.pdf
│   ├── products_services.pdf
│   ├── current_policy_v2.pdf
│   ├── previous_policy_v1.pdf
│   └── operations_faqs.pdf
│
├── tools.py                  # @tool decorated functions (calculate, check_medical_safety)
├── rag_pipeline.py           # Vector database setup and execution flow
├── app.py                    # Streamlit chat interface & evidence inspector
├── requirements.txt          # Package dependencies
└── README.md                 # Project documentation


🚀 SETUP & INSTALLATION GUIDE:

*  Step 1: Create a Python Virtual Environment (venv)
   Open your terminal inside the project root folder and run the following command to create a virtual environment named venv:

  Bash: 

     python -m venv venv

*  Step 2: Activate the Virtual Environment
    Activate the virtual environment depending on your operating system:

    Windows (Command Prompt / PowerShell):

     venv\Scripts\activate

    macOS / Linux:

     source venv/bin/activate

*  Step 3: Install Requirements
    With your virtual environment activated, install all necessary libraries using requirements.txt:

    Bash:

     pip install -r requirements.txt

*  Step 4: Configure Environment Variables
    Create a .env file in your root project directory and add your Groq API key:

    Code snippet:

     GROQ_API_KEY=your_actual_groq_api_key_here

*  Step 5: Run the Assistant
    Execute the final command in your terminal to start the Streamlit web application:

    Bash:

     streamlit run app.py

### DEMO VIDEO OF PROJECT :
[Watch Demo Video]https://drive.google.com/file/d/13cP3Q5wE6DRwFjDadbv4tHRD4_0MYqtQ/view?usp=sharing

