🤖 AI-Powered Regulatory Compliance Checker for Contracts

AI-powered system for automated contract compliance analysis using Large Language Models (LLMs).
Detects GDPR & HIPAA risks, generates safe amendments, and produces audit-ready compliance reports.

🚀 Project Overview

Manual contract compliance review is time-consuming, error-prone, and hard to scale.
This project automates the entire compliance lifecycle using LLMs.

The system is modular, explainable, reliable, and production-ready.
🧠 Key Features

📂 PDF Contract Upload

🔍 Clause Extraction using Generative AI

⚠️ Clause-Level Risk Analysis

📜 GDPR & HIPAA Compliance Checks

✏️ Automatic Amendment Generation (High-Risk Clauses Only)

🧱 Safe Contract Rebuilding

📊 Compliance Reports (JSON, CSV)

📄 Updated Contract Output (TXT & PDF)

🔔 Email & Slack Notifications

📈 Google Sheets Audit Logging

🛡️ LLM Fail-Safe & Fallback Mechanisms

🏗️ System Architecture

Streamlit UI
↓
Pipeline Orchestrator (run.py)
↓
PDF Extraction → Text Cleaning → Chunking
↓
Clause Extraction (LLM)
↓
Risk Analysis (LLM)
↓
Compliance Gap Detection
↓
Amendment Generation (High Risk Only)
↓
Contract Rebuilding
↓
Outputs + Notifications + Audit Logs


🧩 Project Structure
.
├── app.py                         # Streamlit UI
├── run.py                         # Main pipeline orchestrator
├── src/
│   ├── clause_engine/
│   ├── risk_engine/
│   ├── contract_modification/
│   ├── regulatory/
│   ├── llm/
│   ├── integrations/
│   └── utils/
├── data/
│   ├── raw/
│   ├── processed/
│   └── regulations/
├── results/
├── .env                           # Environment variables (ignored)
└── README.md
🧠 LLM Strategy

Primary Model

Groq – llama-3.3-70b-versatile

Fallbacks

OpenRouter (LLaMA 3.1 8B)

Hard JSON fallback

Pipeline never crashes on LLM failure

⚙️ Installation & Setup
1️⃣ Clone Repository
git clone https://github.com/gulsan-ram/AI-Powered-Regulatory-Compliance-Checker-for-Contracts.git
cd AI-Powered-Regulatory-Compliance-Checker-for-Contracts

2️⃣ Create Virtual Environment
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

3️⃣ Install Dependencies
pip install -r requirements.txt

🔑 Environment Variables (.env)
GROQ_API_KEY=your_groq_key
OPENROUTER_API_KEY=your_openrouter_key

SENDER_EMAIL=your_email@gmail.com
EMAIL_APP_PASSWORD=your_app_password

SLACK_WEBHOOK_URL=your_slack_webhook

RAW_DIR=./data/raw
OUTPUT_DIR=./data/processed

MAX_CHUNK_TOKENS=1500
CHUNK_OVERLAP=200

▶️ Running the Application
streamlit run app.py


Open:

http://localhost:8501

📊 Generated Outputs
File	Purpose
_m2_output.json	Clause-level risk analysis
_m2_annotations.csv	Clause annotations
_m3_compliance_report.json	Compliance summary
_updated_contract.txt	Updated contract
_updated_contract.pdf	Final PDF contract
🔔 Notifications & Integrations

Slack → High-risk issues, regulatory updates

Email → High / Critical severity alerts

Google Sheets

Contracts Overview

Compliance Issues

Audit Logs

🧪 Reliability & Fail-Safe Design

Pipeline never crashes on LLM failure

Safe default outputs

Severity-based automation

Full audit trail for compliance

🌱 Future Enhancements

Retrieval-Augmented Generation (RAG)

Support for ISO, SOC2, PCI-DSS

Multilingual contract analysis

Human-in-the-loop approvals

Cloud deployment with REST APIs

📄 License

This project is licensed under the MIT License.

👥 Contributors

Charan — Project Lead & Mentor

⭐ If you like this project, give it a star on GitHub!