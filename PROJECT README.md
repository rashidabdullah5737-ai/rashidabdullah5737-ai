# 🐍 SOC Report Generator

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![CI](https://img.shields.io/badge/CI-GitHub%20Actions-blue?logo=githubactions)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/status-active-success)

---
🔐 SOC Penetration Testing Report Generator




📌 Overview
soc-pentest-report-generator is a SOC-grade automated penetration testing reporting framework designed to transform raw security assessment outputs into structured, professional, client-ready PDF intelligence reports.
It standardizes offensive security documentation by converting technical scan results into executive-level security intelligence with risk classification, remediation guidance, and structured vulnerability mapping.

⚡ Key Features
🔎 Security Data Processing
Subdomain enumeration analysis (subfinder, asset discovery)
Live host validation (httpx)
Vulnerability scanning ingestion (nuclei)
Web crawling & endpoint discovery (katana, gau)
Directory brute-force analysis (dirsearch)

📊 SOC Reporting Engine
Executive summary generation
CVSS-aligned severity classification
Attack surface mapping
Structured vulnerability categorization

📄 Professional PDF Output
SOC-style security reporting format
Client-ready penetration test reports
Evidence-backed findings
Remediation and mitigation guidance

📈 Security Intelligence Layer
Risk distribution analytics
Vulnerability severity breakdown
Attack surface visualization
Security posture summary

⚙️ Automation Ready
One-command report generation
CI/CD pipeline support (GitHub Actions)
JSON/TXT structured input parsing
Multi-scan aggregation support

🧠 Supported Tools / Inputs
subfinder
httpx
nuclei
katana
gau
dirsearch
Custom JSON / TXT scan exports

📂 Project Structure
soc-pentest-report-generator/
│
├── core/                 # Parsing & analysis engine
├── templates/            # SOC PDF report templates
├── utils/                # Scoring & formatting logic
├── data/                 # Raw scan outputs
├── output/              # Generated reports
├── generate_report.py    # Main execution script
└── README.md

🚀 Installation
git clone https://github.com/yourusername/soc-pentest-report-generator.git
cd soc-pentest-report-generator
pip install -r requirements.txt

⚙️ Usage
python generate_report.py --input ./data --output SOC_Report.pdf

🔄 Workflow Example
subfinder -d target.com -o subdomains.txt
httpx -l subdomains.txt -o live.txt
nuclei -l live.txt -o vulnerabilities.txt

python generate_report.py --input ./data --output final_report.pdf
📊 Output Includes
📄 SOC-grade PDF penetration testing report
🧾 Executive security summary
📊 Risk severity dashboard
🔍 Structured vulnerability breakdown
🛡️ Remediation & mitigation recommendations
🛡️ Reporting Standard
This framework aligns with SOC-style security reporting principles:
Structured vulnerability taxonomy
Evidence-based findings
Severity-driven risk classification (Critical → Low)
Repeatable audit-friendly format
Client-ready documentation standards
⚙️ CI/CD (GitHub Actions)
Automatically generate reports on push:
name: SOC Report Build

on:
  push:
    branches: [ "main" ]

jobs:
  build-report:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v3

    - name: Set up Python
      uses: actions/setup-python@v4
      with:
        python-version: "3.10"

    - name: Install dependencies
      run: pip install -r requirements.txt

    - name: Generate SOC Report
      run: python generate_report.py --input ./data --output SOC_Report.pdf

    - name: Upload Artifact
      uses: actions/upload-artifact@v4
      with:
        name: SOC-Report
        path: SOC_Report.pdf
📈 Roadmap
🤖 AI-based vulnerability summarization engine
🌐 Web dashboard for SOC reporting
📡 Live scan ingestion pipeline
📦 Multi-target batch report generator
🧠 Threat intelligence enrichment module
🧾 License
MIT License © 2026
⭐ Support
If this project improves your security workflow or SOC reporting process, consider starring the repository.
