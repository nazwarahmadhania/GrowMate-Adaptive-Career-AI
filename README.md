# 🌱 GrowMate — Adaptive Career AI

### From Career Uncertainty to a Clear Learning Roadmap

[![Hackathon](https://img.shields.io/badge/IBM%20SkillsBuild-National%20Hackathon%202026-052FAD.svg?style=flat-square&logo=IBM&logoColor=white)](https://skillsbuild.org/)
[![Theme](https://img.shields.io/badge/Theme-Education%20%26%20Future%20of%20Work-FF6F00.svg?style=flat-square)](#-hackathon-alignment)
[![Workflow Engine](https://img.shields.io/badge/Engine-Langflow%20AI-5C2D91.svg?style=flat-square)](https://www.langflow.org/)
[![User Interface](https://img.shields.io/badge/Interface-IBM%20Bob-1F77B4.svg?style=flat-square)](#-core-architecture)
[![Protocol](https://img.shields.io/badge/Protocol-Model%20Context%20Protocol%20(MCP)-008080.svg?style=flat-square)](https://modelcontextprotocol.io/)
[![Responsible AI](https://img.shields.io/badge/Responsible%20AI-Ethics%20%26%20Fairness-2E7D32.svg?style=flat-square)](#-responsible-ai)

> **“From feeling lost on where to start, to taking clear and actionable steps.”**

GrowMate is an adaptive AI-powered career readiness and learning roadmap assistant designed to help students and early-career individuals turn their career goals into clear, personalized, and actionable learning plans.

Instead of only recommending skills or courses, GrowMate analyzes the user's current profile, researches the target career, identifies skill gaps, prioritizes skills, creates a personalized learning timeline and roadmap, provides learning resources, tracks progress, and adapts the roadmap when the user's situation changes.

GrowMate is designed as an integrated system using **IBM Bob as the user-facing interface** and **Langflow as the workflow and AI processing engine**, with a **Canonical Roadmap Data** structure serving as the single source of truth across the system.

---

## 🎯 Problem

Many students and early-career individuals know the career they want to pursue, but still struggle with questions such as:

- What skills are actually required for the target career?
- Which skills do I already have?
- What skills am I missing?
- Which skills should I learn first?
- How much time should I allocate for learning?
- Where should I start?
- What learning resources are relevant?
- How can I organize my learning schedule?
- How do I know whether I am making progress?
- What should I do when my available time, priorities, or career goals change?

Existing career and learning platforms often provide information or recommendations, but users may still need to connect those recommendations into one realistic and actionable learning plan.

### The Gap

The challenge is not only finding information.

The challenge is turning:

**Career Goal → Required Skills → Skill Gaps → Priorities → Timeline → Learning Activities → Progress → Adaptation**

into one connected and personalized process.

---

# 💡 Solution

GrowMate connects career analysis, skill-gap analysis, learning planning, progress monitoring, and adaptive replanning into one workflow.

The system guides users through:

```text
User Profile
      ↓
Career Research
      ↓
Skill Gap Analysis
      ↓
Skill Prioritization
      ↓
Career Readiness Indicator (CRI)
      ↓
Personal Learning Timeline
      ↓
Theme Selection
      ↓
Personalized Learning Roadmap
      ↓
To-Do List
      ↓
Learning Resources
      ↓
Output Destination
      ↓
Roadmap Report (Optional)
      ↓
Progress Monitoring
      ↓
Adaptive Replanning
```

This allows GrowMate to move beyond static recommendations and provide a learning plan that can evolve together with the user's progress and changing circumstances.

---

# ✨ Key Features

## 1. 👤 User Profile Analysis

GrowMate starts by understanding the user's current situation, including:

* Educational background
* Current skills
* Existing experience
* Career interests
* Learning availability
* Learning capacity
* Target career

The system uses the information provided by the user instead of assuming missing information.

---

## 2. 🔎 Career Research

GrowMate analyzes the selected target career to identify relevant information such as:

* Required skills
* Technical skills
* Supporting skills
* Expected competencies
* Career-related requirements
* Supporting research sources and evidence

The research results become the basis for the subsequent skill-gap analysis.

---

## 3. 📊 Skill Gap Analysis

GrowMate compares the user's current capabilities with the skills required for the target career.

The analysis distinguishes between:

* Known skill mastery
* Unknown information
* Skills that cannot yet be assessed
* Existing skill gaps

GrowMate does not automatically treat unknown information as zero mastery.

---

## 4. 🎯 Skill Prioritization

Not every skill needs to be learned at the same time.

GrowMate prioritizes skills based on the user's career target, current profile, skill gaps, and learning capacity.

This helps users understand:

**What should I learn first?**

---

## 5. 📈 Career Readiness Indicator (CRI)

GrowMate can generate a **Career Readiness Indicator (CRI)** when sufficient information is available.

The CRI is intended to provide an overview of the user's current readiness relative to the selected career target.

If the available data is insufficient, GrowMate does not fabricate a score.

---

## 6. 🗓️ Personalized Learning Timeline

GrowMate considers:

* Target timeline
* Available learning time
* Learning capacity

The resulting timeline is used to determine a realistic learning plan instead of generating a generic roadmap.

---

## 7. 🗺️ Personalized Learning Roadmap

GrowMate converts the analysis into a structured learning roadmap containing:

* Learning sessions
* Learning objectives
* Activities
* Tasks
* Estimated duration
* Priority
* Deadlines
* Learning resources
* Progress status

The roadmap is generated according to the user's learning capacity and target timeline.

---

## 8. ✅ To-Do List

The roadmap is converted into actionable tasks so users can clearly see:

* What needs to be done
* Which task has priority
* Estimated duration
* Deadline
* Current status

Supported statuses include:

* ⬜ Not Started
* 🔄 In Progress
* ✅ Completed

---

## 9. 📚 Learning Resources

GrowMate provides relevant learning resources for roadmap activities.

Resources are connected to the learning objectives instead of being presented as an unrelated list of links.

---

## 10. 🎨 Adaptive Theme

Users can select a presentation theme for their roadmap.

For example, a Formula 1-inspired theme may present roadmap elements using concepts such as:

* Race Strategy
* Lap
* High Priority
* Resources
* Finish Line

The theme changes the **presentation**, not the underlying roadmap data.

This allows users to personalize the experience while keeping the actual career analysis and learning plan consistent.

---

## 11. 📝 Notion Integration

If selected and authorized by the user, GrowMate can create or update a roadmap in Notion.

Notion can also be used as one of the available sources for progress monitoring when connected and authorized.

GrowMate does not claim to access Notion data when the integration is not connected.

---

## 12. 📅 Google Calendar Integration

If selected and authorized by the user, GrowMate can create or update learning schedules and reminders in Google Calendar.

Calendar events represent scheduled learning activities.

A calendar event does **not** automatically mean that the corresponding task has been completed.

---

## 13. 📄 Roadmap Report

After the roadmap and selected output destinations are completed, users can optionally request a **Roadmap Report in HTML format**.

The report is generated from the same Canonical Roadmap Data used by GrowMate.

The system does not create a separate roadmap just for the report.

---

## 14. 📊 Progress Monitoring

GrowMate monitors learning progress using available valid sources, including:

* User conversations
* To-Do List status
* Notion status when connected and authorized
* Other valid progress information available to the system

For example:

```text
Completed Sessions
------------------ × 100
Total Sessions
```

Progress updates are based on evidence provided by the user or valid connected sources.

A Google Calendar event being created, opened, or reaching its deadline does not automatically mark a task as completed.

---

## 15. 🔄 Adaptive Replanning

GrowMate is designed to adapt the roadmap when the user's circumstances change.

Replanning may be triggered when:

* The deadline is missed
* Available learning time changes
* The user completes learning faster than expected
* The user experiences difficulty
* Skill mastery changes
* The target career changes
* Skill priorities change

The adaptive process follows:

```text
Progress
   ↓
Evaluate
   ↓
Replan
   ↓
Update
   ↓
Continue
```

Only the affected parts of the roadmap should be updated when possible.

---

# 🧠 Core Architecture

GrowMate uses a centralized data approach to keep the system consistent.

```text
                    ┌─────────────────┐
                    │      USER       │
                    └────────┬────────┘
                             ↕
                    ┌─────────────────┐
                    │    IBM BOB      │
                    │ User Interface  │
                    └────────┬────────┘
                             ↕
                    ┌─────────────────┐
                    │    LANGFLOW     │
                    │ Workflow Engine │
                    └────────┬────────┘
                             ↕
              ┌──────────────────────────────┐
              │ CANONICAL ROADMAP DATA      │
              │ Single Source of Truth      │
              └──────────────┬───────────────┘
                             │
          ┌──────────────────┼──────────────────┐
          ↓                  ↓                  ↓
      ┌────────┐       ┌────────────┐      ┌────────────┐
      │ Notion │       │  Calendar  │      │   Report   │
      └────────┘       └────────────┘      └────────────┘
                             │
                             ↓
                    ┌─────────────────┐
                    │    Progress     │
                    │    Monitoring   │
                    └────────┬────────┘
                             ↓
                    ┌─────────────────┐
                    │ Adaptive        │
                    │ Replanning      │
                    └─────────────────┘
```

### Single Source of Truth

**Canonical Roadmap Data** is the central source of truth for GrowMate.

The following outputs must remain consistent with it:

* IBM Bob
* Roadmap
* Roadmap Report
* Notion
* Google Calendar
* Progress Tracking
* Adaptive Replanning

IBM Bob and Langflow are designed to represent the same GrowMate state.

They must not independently create conflicting:

* Skill Gap
* Skill Priority
* CRI
* Timeline
* Roadmap
* Status
* Progress
* Target Career

If information changes, the change is processed through the GrowMate workflow and the updated state is propagated to the relevant outputs.

---

# 🔄 End-to-End Workflow

```text
1. User Profile
       ↓
2. Career Research
       ↓
3. Full Skill Gap Analysis
       ↓
4. Skill Prioritization
       ↓
5. Career Readiness Analysis
       ↓
6. Personal Learning Timeline
       ↓
7. Theme Selection
       ↓
8. Personalized Learning Roadmap
       ↓
9. To-Do List
       ↓
10. Learning Resources
       ↓
11. Output Destination
       ↓
12. Selected Output
       ↓
13. Roadmap Report Approval
       ↓
14. Roadmap Report (Optional)
       ↓
15. Progress Monitoring
       ↓
16. Adaptive Replanning
```

GrowMate follows checkpoint-based interaction and waits for required user decisions before moving to dependent stages.

---

# 🛡️ Responsible AI

Responsible AI is incorporated into the workflow through several safeguards.

### 1. No Fabricated Skill Mastery

GrowMate does not assume that a user has mastered a skill simply because they:

* Have a certificate
* Completed a course
* Mentioned a related activity

Evidence and user-provided information are considered before assessing mastery.

### 2. Unknown Data Is Not Zero

GrowMate distinguishes between:

* `Unknown / Not Yet Known`
* `Unassessed / Cannot Be Evaluated Yet`
* `0% (Explicitly Unlearned)`

Missing information is not automatically converted into a zero score.

### 3. CRI Requires Sufficient Data

GrowMate does not generate a Career Readiness Indicator when the available information is insufficient.

### 4. Human Approval for External Actions

External actions such as:

* Creating or updating Notion content
* Creating or updating Google Calendar events
* Generating the Roadmap Report

are handled through explicit user choices or approval checkpoints.

### 5. No Silent Modification

Changes affecting important roadmap data should be processed through the GrowMate workflow rather than silently modifying the state.

### 6. No False Success Claims

GrowMate should not claim that an external action was successful when the action fails.

### 7. Data Consistency

The system uses Canonical Roadmap Data to prevent different platforms from presenting conflicting versions of the user's roadmap.

---

# 👥 Target Users

GrowMate is primarily designed for:

* University students
* Fresh graduates
* Early-career individuals
* Career switchers
* Learners who are unsure where to start
* Users who need structured career-oriented learning plans

The initial focus is on users who have a career goal but need help translating that goal into a practical learning path.

---

# 🌍 User Impact

GrowMate aims to help users:

### Before GrowMate

```text
“I know what career I want,
but I don't know what I should learn first.”
```

### With GrowMate

```text
Career Goal
     ↓
Required Skills
     ↓
Skill Gaps
     ↓
Priority
     ↓
Timeline
     ↓
Learning Roadmap
     ↓
To-Do
     ↓
Progress
     ↓
Adaptive Replanning
```

The intended benefits include:

* Greater clarity about required skills
* Better understanding of personal skill gaps
* More structured learning priorities
* A realistic learning schedule
* Easier task management
* Progress visibility
* A roadmap that can adapt to changing circumstances

---

# 💼 Business Model

GrowMate is currently developed as a prototype.

A potential future business model includes:

### Freemium

**Free**

* Career profile analysis
* Basic skill-gap analysis
* Basic learning roadmap
* Basic progress tracking

**Premium**

* Advanced career research
* More detailed roadmap customization
* Advanced adaptive replanning
* Additional integrations
* Advanced reports and analytics

### Institutional / B2B

GrowMate could also be offered to:

* Universities
* Career centers
* Student development programs
* Training institutions
* Workforce development programs

Institutional plans could provide structured career-readiness support for students and learners.

> The business model above represents a future monetization direction and is not claimed as an implemented feature of the current prototype.

---

# 🧪 Testing & Validation Approach

GrowMate should be validated using scenario-based testing covering the complete workflow.

### Core Scenarios

| Scenario                       | Expected Behavior                               |
| ------------------------------ | ----------------------------------------------- |
| New user creates a roadmap     | Profile → career research → skill gap → roadmap |
| Missing skill information      | Remains unknown instead of becoming 0%          |
| Insufficient data for CRI      | CRI is not fabricated                           |
| User selects Notion            | Notion action occurs only after user approval   |
| User selects Calendar          | Calendar action occurs only after user approval |
| User selects Calendar + Notion | Both selected destinations are processed        |
| User selects "Not Now" / "Skip" | No external action is performed                 |
| User reports completed session | Session status becomes Completed                |
| User reports active session    | Session status becomes In Progress              |
| Calendar event exists          | Does not automatically mark task Completed      |
| Learning time changes          | Affected roadmap is reconsidered                |
| Target career changes          | Relevant analysis and roadmap are updated       |
| Roadmap Report = No            | No HTML report is generated                     |
| Roadmap Report = Yes           | Report uses Canonical Roadmap Data              |

The validation process focuses on:

* Workflow correctness
* Data consistency
* Checkpoint behavior
* External action approval
* Progress accuracy
* Adaptive replanning
* Prevention of unsupported claims
* Prevention of duplicate actions

---

# ⚙️ Technical Stack

| Technology                  | Role                                                                |
| --------------------------- | ------------------------------------------------------------------- |
| **Langflow**                | AI workflow and processing engine                                   |
| **IBM Bob**                 | User-facing interface and interaction layer                         |
| **Google Generative AI**    | Language model provider configured in the current Langflow workflow |
| **MCP / Tool Integrations** | Bridge between the workflow and external services                   |
| **Notion**                  | Optional roadmap storage and progress source                        |
| **Google Calendar**         | Optional learning schedule and reminder integration                 |
| **Git**                     | Version control                                                     |
| **GitHub**                  | Public project repository                                           |

> The current Langflow export contains Google Generative AI model configuration. IBM Bob and Langflow provide the primary hackathon-facing application architecture.

---

# 📁 Project Structure

```text
GrowMate-Adaptive-Career-AI/
│
├── GrowMate – Adaptive Career AI.json
│   └── Main Langflow workflow export
│
├── ibm-bob-mcp-config.json
│   └── IBM Bob MCP configuration
│
└── README.md
    └── Project documentation
```

---

# 🚀 Installation & Setup

GrowMate is primarily configured through **Langflow and IBM Bob** rather than a traditional Node.js application workflow.

There is no requirement to run:

```bash
npm install
npm run dev
```

for the core GrowMate workflow.

## 1. Clone the Repository

```bash
git clone https://github.com/nazwarahmadhania/GrowMate-Adaptive-Career-AI.git
```

```bash
cd GrowMate-Adaptive-Career-AI
```

## 2. Import the Langflow Workflow

Open Langflow and import:

```text
GrowMate – Adaptive Career AI.json
```

The workflow contains the main GrowMate agent, workflow instructions, tool integrations, and roadmap-processing logic.

## 3. Configure the Model Provider

Configure the required language model/API credentials in the Langflow environment.

The current workflow contains Google Generative AI model configuration.

## 4. Configure IBM Bob

Use:

```text
ibm-bob-mcp-config.json
```

to configure the required MCP connection between IBM Bob and the GrowMate workflow.

IBM Bob acts as the primary user-facing interface.

## 5. Configure Optional Integrations

If required, configure:

* Notion
* Google Calendar

These integrations are optional and depend on the user's authorization and available credentials.

## 6. Run GrowMate

Start the Langflow workflow and access GrowMate through the configured IBM Bob interface.

---

# 🔐 External Actions & Permissions

GrowMate does not automatically perform external actions without user selection or approval.

Possible external actions include:

```text
GrowMate
   ↓
User chooses destination
   ↓
Approval / Confirmation
   ↓
Notion and/or Google Calendar
```

Available output destination options include:

1. 📝 Notion
2. 📅 Google Calendar
3. 📅📝 Google Calendar + Notion
4. ⏭️ Not Now / Skip

---

# 📸 Screenshots

Screenshots demonstrate the working prototype and key components of GrowMate.

### Langflow Workflow

GrowMate uses Langflow as a workflow and processing engine that connects IBM Bob with supporting tools and services, such as Web Search, Notion, and Google Calendar. This workflow processes user input and generates responses through the Agent in an integrated manner.

![Langflow Workflow](https://github.com/nazwarahmadhania/GrowMate-Adaptive-Career-AI/blob/9e8ba2935b567ca6e9e8e34d689a8a76768dd8c7/Screenshot%202026-09-25%20142223.png)

### IBM Bob Interface

IBM Bob serves as GrowMate’s main interface, where users interact with the agent throughout the roadmap generation process, from providing their profile to receiving a personalized learning roadmap.

![IBM Bob Interface](https://github.com/nazwarahmadhania/GrowMate-Adaptive-Career-AI/blob/d47b9764b9fac580b340a1320f754e24dfd92edb/Screenshot%202026-09-26%20023701.png)

![Personalized Learning Roadmap](https://github.com/nazwarahmadhania/GrowMate-Adaptive-Career-AI/blob/b6a38d5de6746044d79f584b5f0dd8d9f5f328e1/Screenshot%202026-09-26%20040026.png)

### Progress Monitoring

GrowMate monitors learning progress by tracking completed tasks, current sessions, and the next learning focus.

![Progress Monitoring](https://github.com/nazwarahmadhania/GrowMate-Adaptive-Career-AI/blob/60af542dee1b5bfe6bcbb00d2184ea431f654f5d/Screenshot%202026-09-26%20040644.png)


### Adaptive Replanning

*Add screenshot here.*

```text
![Adaptive Replanning](screenshots/adaptive-replanning.png)
```

![Notion Integration](screenshots/notion.png)

### Google Calendar Integration

...

![Google Calendar Integration](screenshots/google-calendar.png)

### Roadmap Report

...

![Roadmap Report](screenshots/roadmap-report.png)
---

# ⚠️ Current Limitations

As a prototype, GrowMate still has several limitations:

* External integrations depend on valid user credentials and permissions.
* The quality of career research and recommendations depends on the available information and model output.
* Some integrations may have API or platform limitations.
* Real-world career readiness cannot be fully represented by a single indicator.
* Learning resources may change availability over time.
* The current prototype has not yet been evaluated as a production-scale career platform.
* Large-scale user testing and quantitative impact measurement remain future work.

These limitations are considered part of the prototype's development scope.

---

# 🔮 Future Development

Potential future improvements include:

* Larger-scale user testing
* Quantitative measurement of user outcomes
* Improved career research and evidence retrieval
* More career domains
* More learning-resource providers
* Enhanced progress analytics
* More adaptive replanning strategies
* Improved accessibility
* Mobile-friendly experience
* Additional productivity integrations
* Institutional deployment for universities and career centers
* More advanced personalization based on long-term learning behavior

---

# 🏆 Hackathon Alignment

GrowMate is designed for the **Education & Future of Work** theme.

The project addresses career-readiness and learning-planning challenges by combining:

* AI-powered career research
* Skill-gap analysis
* Skill prioritization
* Career readiness assessment
* Personalized learning roadmap generation
* Progress monitoring
* Adaptive replanning

### Alignment with the Evaluation Areas

| Evaluation Area                          | GrowMate Implementation                                                                                                 |
| ---------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **Problem Clarity & Relevance**          | Addresses career-readiness and learning-planning challenges faced by students and early-career users                    |
| **Innovation, Creativity & Feasibility** | Combines career analysis, personalized roadmap generation, progress monitoring, and adaptive replanning in one workflow |
| **User Impact & Benefits**               | Helps users transform career goals into structured and actionable learning steps                                        |
| **Technical Execution**                  | Uses IBM Bob, Langflow, MCP/tool integrations, Canonical Roadmap Data, and external services                            |
| **Responsible AI**                       | Includes approval checkpoints, data consistency rules, no fabricated mastery, and safeguards against unsupported claims |
| **Scalability**                          | Designed to support additional career domains, resources, integrations, and institutional use cases                     |

The hackathon's judging criteria include problem clarity and relevance, innovation/feasibility/monetization, user impact, technical execution and prototype functionality, and responsible AI. 

---

# 📌 Project Information

**Project Name:** GrowMate — Adaptive Career AI

**Theme:** Education & Future of Work

**Core Technologies:** IBM Bob, Langflow, Google Generative AI, MCP

**Repository:**
[https://github.com/nazwarahmadhania/GrowMate-Adaptive-Career-AI](https://github.com/nazwarahmadhania/GrowMate-Adaptive-Career-AI)

**Project Type:** AI-powered career readiness and personalized learning roadmap assistant

**Status:** Prototype

---

# 🙏 Acknowledgements

This project was developed as part of the **Hacktiv8 x IBM SkillsBuild University 2026 National Hackathon**.

Special thanks to the organizers, mentors, and the communities supporting the development of AI-powered solutions for education and future-of-work challenges.

---

# 👩‍💻 Author

### Nazwa Rahmadhania

* GitHub: [https://github.com/nazwarahmadhania](https://github.com/nazwarahmadhania)
* LinkedIn: [https://www.linkedin.com/in/nazwa-rahmadhania](https://www.linkedin.com/in/nazwa-rahmadhania)

---

# 📄 License

This project is created for educational and hackathon purposes.

Unless otherwise stated, the project source code and documentation are provided for evaluation and demonstration purposes.
