# 🌱 GrowMate — Adaptive Career AI

> **From Career Confusion to a Clear, Actionable Learning Roadmap.**

[![Hackathon](https://img.shields.io/badge/IBM%20SkillsBuild-National%20Hackathon%202026-052FAD.svg?style=flat-square&logo=IBM&logoColor=white)](https://skillsbuild.org/)
[![Theme](https://img.shields.io/badge/Theme-Education%20%26%20Future%20of%20Work-FF6F00.svg?style=flat-square)]()
[![Workflow Engine](https://img.shields.io/badge/Engine-Langflow%20AI-5C2D91.svg?style=flat-square)](https://www.langflow.org/)
[![User Interface](https://img.shields.io/badge/Interface-IBM%20Bob-1F77B4.svg?style=flat-square)]()
[![Protocol](https://img.shields.io/badge/Protocol-Model%20Context%20Protocol%20(MCP)-008080.svg?style=flat-square)](https://modelcontextprotocol.io/)
[![Responsible AI](https://img.shields.io/badge/Responsible%20AI-Ethics%20%26%20Fairness-2E7D32.svg?style=flat-square)]()

**GrowMate** is an Adaptive AI Career Readiness & Personalized Learning Roadmap Assistant designed to help students, fresh graduates, and career switchers analyze their current profile, bridge skill gaps through real-time market research, and execute concrete learning habits via Notion and Google Calendar.

GrowMate leverages **Langflow** as its AI reasoning and orchestration engine and **IBM Bob** as the conversational interface, interconnected seamlessly via the **Model Context Protocol (MCP)**.

---

## 🎯 Problem & Solution

### The Problem
Early-career seekers and students frequently suffer from **analysis paralysis** and **tutorial hell**:
* They know their desired career (e.g., Data Scientist or AI Engineer) but don't know where to start.
* Academic curricula often lag behind real-time industry demands and evolving tooling.
* Generic online roadmaps assume unlimited time and uniform capability, leading to burnout and abandoned plans.

### The Solution
GrowMate transforms static career advice into an **adaptive, capacity-locked execution pipeline**:

$$\text{Career Research} \longrightarrow \text{Skill Gap} \longrightarrow \text{Prioritization} \longrightarrow \text{CRI} \longrightarrow \text{Roadmap} \longrightarrow \text{Execution (Calendar/Notion)} \longrightarrow \text{Replanning}$$

---

## ✨ Features

- 👤 **Comprehensive Profile Checkpoint**: Analyzes academic background, 3-tier isolated experiences (work/freelance, volunteer/orgs, projects), and optional CV upload without bias.
- 🔎 **Grounded Career Research**: Integrates live Web Search to extract real-world job requirements, required tools, and competency benchmarks with evidence citations.
- 📊 **Objective Skill Gap Analysis**: Enforces a strict 3-tier rule distinguishing *Owned*, *Basic*, *0% (Explicitly Unlearned)*, *Unknown Level*, and *Unassessed Requirements* (anti-hallucination).
- ⚖️ **Dependency-Aware Prioritization**: Structures learning order logically: $\text{Fundamentals} \rightarrow \text{Practice} \rightarrow \text{Project} \rightarrow \text{Review} \rightarrow \text{Advanced}$.
- 📈 **Career Readiness Indicator (CRI)**: Computes an analytical compatibility score with transparent weighting ($\sum \text{Skill Mastery} \times \text{Weight}$) and honest limitation reporting.
- ⏱️ **Capacity Lock & Timeline**: Locks target deadlines and realistic study hours (e.g., 2 hours every 2 days) to prevent overpromising.
- 🗺️ **Personalized Roadmap & To-Do Lists**: Generates modular sessions with specific learning objectives, granular tasks, and verified resources.
- 📅 **Session-Based Calendar Scheduling**: Maps every session into a real calendar commitment (**1 Session = 1 Calendar Event**) with reminders and duration.
- 📝 **Notion Workspace Sync**: Keeps an active, organized database with session order, status tracking, and subtasks.
- 📄 **Interactive Roadmap Report**: Generates an optional, exportable HTML summary report.
- 🔄 **Adaptive Replanning**: Dynamically adjusts timelines and unfinished sessions when life events or study delays happen.
- 🎨 **Adaptive Themes**: Personalizes tone and presentation (e.g., Ferrari / F1 Race Strategy) without altering the integrity of underlying data.

---

## 🏗️ System Architecture

GrowMate separates concerns between the user-facing client (**IBM Bob**) and the AI workflow orchestrator (**Langflow**) via **MCP**:

```text
                         USER
                           ↕
                       IBM BOB (Chat UI)
                           ↕ Model Context Protocol (MCP)
                       LANGFLOW (Workflow Engine)
                           ↕
                CANONICAL ROADMAP DATA (Single Source of Truth)
                  ↙       ↓        ↘
              NOTION   CALENDAR   HTML REPORT
                           ↓
                  PROGRESS MONITORING
                           ↓
                  ADAPTIVE REPLANNING
```

### Components:
* **IBM Bob**: Front-end conversational agent interacting with users and resolving intent.
* **Model Context Protocol (MCP)**: Standardized protocol exposing Langflow endpoints and Composio tool connectors to IBM Bob.
* **Langflow Engine**: Executes agent logic, 63 guardrail checkpoints, web search, and data mapping.
* **Canonical Roadmap Data**: Ensures complete state consistency—preventing desynchronization across IBM Bob, Notion, and Google Calendar.

---

## 🔄 GrowMate Workflow

```text
User Input
  ↓
User Profile Verification (Education, 3 Experience Groups, Skills, CV)
  ↓
Live Career Research (Web Search Grounding)
  ↓
Skill Gap Matrix (3-Tier Mastery Rules)
  ↓
Skill Prioritization (High / Medium / Low)
  ↓
Career Readiness Indicator (CRI) Calculation
  ↓
Personal Learning Timeline & Capacity Lock
  ↓
Theme Selection (Visual & Presentation Styling)
  ↓
Personalized Learning Roadmap
  ↓
Granular To-Do List & Curated Learning Resources
  ↓
Canonical Roadmap Data Lock
  ↓
Output Selection (Notion / Google Calendar / Chat Only)
  ↓
Optional Roadmap Report (HTML Export)
  ↓
Progress Monitoring & Adaptive Replanning
```

---

## 🛡️ Responsible AI Implementation

GrowMate strictly complies with the **IBM SkillsBuild Responsible AI Framework**:

1. **Human Agency & Oversight**: AI is an advisor, not a decider. The user always selects their target career. External actions (Notion database creation, Google Calendar events) **always require explicit user confirmation**.
2. **Explainability & Grounding**: Career requirements are grounded in verified web search citations rather than LLM assumptions. The CRI formula and data limitations are openly explained.
3. **Fairness & Anti-Bias**: Skill evaluations follow an explicit *Evidence Hierarchy* without socioeconomic, campus, or demographic bias.
4. **Privacy & Data Security**: Zero hardcoded credentials. All integrations utilize environment variables/MCP placeholders. CV uploading is completely optional and processed locally.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **Langflow** | AI workflow modeling and multi-agent orchestration |
| **IBM Bob** | User interface and agent interaction client |
| **Model Context Protocol (MCP)** | Standardized bridge connecting IBM Bob with Langflow & tools |
| **Google Gemini / IBM Granite** | Reasoning engine for profiling and roadmap synthesis |
| **Composio** | Tool integrations for Google Calendar and Notion API |
| **Unified Web Search** | Real-time industry research and trend validation |
| **HTML5 / CSS3** | Portable, responsive Roadmap Report generator |

---

## 📂 Project Structure

```text
GrowMate-Adaptive-Career-AI/
│
├── Code IBM bob/
│   └── .bob/
│       └── mcp.json                       # IBM Bob Model Context Protocol configuration
│
├── GrowMate – Adaptive Career AI.json     # Langflow workflow export (Nodes, Prompts, Guardrails)
├── ibm-bob-mcp-config.json                # Root MCP config template (with placeholders)
└── README.md                              # Comprehensive project documentation
```

---

## 🚀 Setup & Installation

GrowMate is built with **Langflow and IBM Bob**, requiring no complicated compile steps.

### 1. Clone the repository
```bash
git clone https://github.com/nazwarahmadhania/GrowMate-Adaptive-Career-AI.git
cd GrowMate-Adaptive-Career-AI
```

### 2. Run Langflow Engine
1. Install Langflow if not already installed:
   ```bash
   pip install langflow
   langflow run
   ```
2. Open `http://localhost:7860` in your browser.
3. Click **Import** and select `GrowMate – Adaptive Career AI.json`.
4. Configure required API keys (Gemini, Web Search, and Composio) within Langflow component settings.

### 3. Connect IBM Bob via MCP
1. Open your IBM Bob configuration (`Code IBM bob/.bob/mcp.json` or `ibm-bob-mcp-config.json`).
2. Point the MCP server URL to your running Langflow instance:
   ```json
   {
     "mcpServers": {
       "langflow-growmate": {
         "type": "streamable-http",
         "url": "http://127.0.0.1:7860/api/v1/mcp/project/<PROJECT_ID>/streamable",
         "headers": {
           "x-api-key": "YOUR_LANGFLOW_API_KEY"
         },
         "alwaysAllow": ["growmate_adaptive_career_ai"]
       }
     }
   }
   ```
3. Restart MCP in IBM Bob and start chatting with GrowMate!

---

## 📅 Calendar & Notion Integrations

### Session-Based Scheduling
GrowMate avoids overwhelming weekly blobs by adhering to:

$$\text{1 Session} = \text{1 Calendar Event}$$

Each calendar event includes the session number, target skill, estimated duration, granular to-do items, and study deadline derived from the user's *Start Learning Date*.

---

## 📸 Screenshots

| IBM Bob Interface | Langflow Workflow |
|---|---|
| *(Screenshot of conversational profiling & CRI output)* | *(Screenshot of the 12 Langflow nodes & tools)* |

| Google Calendar Integration | Notion Learning Database |
|---|---|
| *(Screenshot of session events & reminders)* | *(Screenshot of roadmap tasks and to-do lists)* |

---

## 🙏 Acknowledgements

Developed as part of the **Hacktiv8 x IBM SkillsBuild University 2026** program. Special gratitude to mentors, organizers, and resources that supported the development of GrowMate.

---

## 📌 Project Information

* **Project Name:** GrowMate — Adaptive Career AI
* **Competition:** Hacktiv8 National Hackathon 2026
* **Program:** IBM SkillsBuild University Education 2026
* **Theme:** Education & Future of Work
* **Project Status:** Prototype / Hackathon Submission

---

## 👩‍💻 Author

**Nazwa Rahmadhania**
* GitHub: [github.com/nazwarahmadhania](https://github.com/nazwarahmadhania)
* LinkedIn: [linkedin.com/in/nazwa-rahmadhania](https://www.linkedin.com/in/nazwa-rahmadhania)

---

## 📄 License

This project is licensed under the MIT License — shared for learning, experimentation, and portfolio purposes.

© 2026 Nazwa Rahmadhania. All rights reserved.