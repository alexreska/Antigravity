# 🌌 Antigravity — Your AI Dream Team Operating System

> **80+ Specialized AI Agents • 709+ Agentic Skills • One-Command Client Onboarding**
>
> Turn any AI coding assistant into a full-service digital agency with specialized departments, an orchestrator, and a client builder that creates bespoke teams in seconds.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Agents](https://img.shields.io/badge/Agents-80%2B-blueviolet)](.antigravity/docs/persona_menu.md)
[![Skills](https://img.shields.io/badge/Skills-709%2B-green)](.antigravity/skills/)
[![Client Builder](https://img.shields.io/badge/Client%20Builder-Automated-orange)](client_builder.py)

---

## Table of Contents

- [🚀 What Is This?](#what-is-this)
- [🏗️ Architecture](#architecture)
- [👑 The MASTER Orchestrator](#the-master-orchestrator)
- [🏢 The Dream Team — 80+ Agents by Department](#the-dream-team--80-agents-by-department)
- [🛠️ 709+ Agentic Skills](#709-agentic-skills)
- [🤝 Client Builder — Bespoke Teams in One Command](#client-builder--bespoke-teams-in-one-command)
- [⚡ Quick Start](#quick-start)
- [📂 Project Structure](#project-structure)
- [🔧 Key System Files](#key-system-files)
- [🧩 How It All Works Together](#how-it-all-works-together)
- [🔌 Compatibility](#compatibility)
- [⚖️ License](#license)

---

## What Is This?

**Antigravity** is not just a collection of skills — it's a **complete multi-agent operating system** for AI coding assistants.

Most skill repos give you a flat list of markdown files. Antigravity gives you:

| Feature | What You Get |
|:--------|:-------------|
| **🧠 Orchestrator** | A `MASTER` agent that analyzes requests and delegates to the right specialist |
| **👥 80+ Personas** | Specialized agents organized into departments (Engineering, Marketing, Security, Legal, HR…) |
| **🛠️ 709+ Skills** | A massive library of executable knowledge modules each agent can use |
| **🤖 Client Builder** | A `RECEPTIONIST` agent interviews you, then `client_builder.py` creates an isolated Git branch with only the personas and skills your project needs |
| **🏭 Skill Creator** | Missing a skill? The `SKILL_CREATOR` agent generates new ones on demand, following the Antigravity standard |
| **📋 Agent Protocol** | A formal hierarchy (MASTER → Executive → Specialists) with engagement rules, review workflows, and guardrails |

> **Think of it as hiring an entire digital agency — CEO, CTO, CMO, Security Team, Legal, HR — that lives inside your AI assistant.**

---

## Architecture

```
┌──────────────────────────────────────────────────────────┐
│                      USER REQUEST                         │
└─────────────────────────┬────────────────────────────────┘
                          │
                          ▼
              ┌───────────────────────┐
              │    👑 THE MASTER      │
              │   Chief Orchestrator  │
              │  (Analyzes & Delegates)│
              └───────────┬───────────┘
                          │
          ┌───────────────┼───────────────┐
          ▼               ▼               ▼
   ┌─────────────┐ ┌─────────────┐ ┌─────────────┐
   │  Executive  │ │ Engineering │ │  Growth &   │
   │  & Strategy │ │ (FE/BE/Ops) │ │  Marketing  │
   │             │ │             │ │             │
   │ CHIEF_OF_   │ │ REACT_      │ │ CMO_BOT     │
   │ STAFF       │ │ EXPERT      │ │ SEO_        │
   │ PRODUCT_    │ │ FLUTTER_DEV │ │ TECHNICAL   │
   │ VISIONARY   │ │ DBA_POSTGRES│ │ COPY_CHIEF  │
   │ ...         │ │ ...         │ │ ...         │
   └─────────────┘ └─────────────┘ └─────────────┘
          │               │               │
          └───────────────┼───────────────┘
                          ▼
              ┌───────────────────────┐
              │   🛠️ 709+ SKILLS     │
              │  (Executable Knowledge │
              │   Modules)            │
              └───────────────────────┘
```

**The Hierarchy (from [`AGENT_PROTOCOL.md`](.antigravity/docs/AGENT_PROTOCOL.md)):**

| Level | Role | Examples |
|:------|:-----|:---------|
| **Level 1** | 👑 **MASTER** — Orchestrates everything, never codes directly | Delegates to specialists |
| **Level 2** | 🏛️ **Executive & Strategy** — Plans before execution | `CHIEF_OF_STAFF`, `PRODUCT_VISIONARY`, `AGILE_COACH` |
| **Level 3** | 🛠️ **Specialist Execution** — The hands that build | `REACT_EXPERT`, `DBA_POSTGRES`, `RED_TEAMER`, `CMO_BOT`… |

---

## The MASTER Orchestrator

The [`MASTER.md`](.antigravity/personas/MASTER.md) is the brain of the system. It:

1. **Analyzes** your request and identifies the domain
2. **Selects** the right specialist(s) from the [persona menu](.antigravity/docs/persona_menu.md)
3. **Delegates** the task — it never codes directly
4. **Reviews** the output before presenting it to you
5. **Calls `SKILL_CREATOR`** if a required skill is missing

**Example routing:**

| You say | Domain | Agent(s) called |
|:--------|:-------|:----------------|
| *"Write a blog post for SEO"* | Marketing | `SEO_CONTENT` + `COPY_CHIEF` |
| *"Fix this React performance issue"* | Frontend | `REACT_EXPERT` + `PERFORMANCE_TESTER` |
| *"Audit our API security"* | Security | `APPSEC_SPECIALIST` + `RED_TEAMER` |
| *"Design our database schema"* | Backend | `DBA_POSTGRES` + `BACKEND_PRINCIPAL` |
| *"Create a pitch deck"* | Executive | `STARTUP_STRATEGIST` |
| *"Run a phishing simulation"* | Security | `SOCIAL_ENGINEER` |

---

## The Dream Team — 80+ Agents by Department

Every agent is a markdown persona file in [`.antigravity/personas/`](.antigravity/personas/). Each defines a **Role**, **Goal**, **Toolkit** (linked skills), and **Instructions**.

### 🏛️ Executive & Strategy
| Agent | Mission |
|:------|:--------|
| `CHIEF_OF_STAFF` | Orchestrate cross-department execution & strategic alignment |
| `PRODUCT_VISIONARY` | Define product strategy, PRDs, and feature prioritization |
| `STARTUP_STRATEGIST` | Pitch decks, business models, fundraising |
| `AGILE_COACH` | Sprints, standups, Jira/Linear workflows |
| `COMMUNITY_HEAD` | Community management, Discord/Slack, events |

### 🚀 Growth, Marketing & Sales
| Agent | Mission |
|:------|:--------|
| `CMO_BOT` | Holistic marketing strategy & go-to-market |
| `GROWTH_HACKER` | Rapid experiments, A/B tests, viral loops |
| `SEO_TECHNICAL` | Site architecture, Core Web Vitals, schema markup |
| `SEO_CONTENT` | Keyword research, topic clusters, content strategy |
| `COPY_CHIEF` | High-converting sales copy, ads, VSL scripts |
| `EMAIL_STRATEGIST` | Automation workflows, newsletters, retention |
| `SOCIAL_X_PRO` | X/Twitter growth, threads, viral content |
| `SOCIAL_LINKEDIN` | B2B thought leadership on LinkedIn |
| `VIDEO_DIRECTOR` | Creative direction, storyboarding |
| `VIDEO_EDITOR` | Programmatic video (Remotion, FFmpeg) |
| `SALES_ENGINEER` | Technical demos, CRM integration |
| `COLD_OUTREACH` | Lead generation, cold email at scale |

### 🎨 Design & Experience
| Agent | Mission |
|:------|:--------|
| `UX_RESEARCHER` | User interviews, usability testing, empathy mapping |
| `UI_ARCHITECT` | Design systems, component libraries |
| `BRAND_GUARDIAN` | Brand consistency across all touchpoints |
| `MOTION_DESIGNER` | Micro-interactions, web animations |
| `ACCESSIBILITY_AUDITOR` | WCAG compliance |

### 🧠 Data & AI
| Agent | Mission |
|:------|:--------|
| `DATA_SCIENTIST` | Statistical modeling & insights |
| `AI_ARCHITECT` | Agent systems & cognitive architectures |
| `PROMPT_ENGINEER` | LLM optimization & system prompts |
| `RAG_SPECIALIST` | Retrieval-Augmented Generation pipelines |
| `MLOPS_ENGINEER` | Model deployment & monitoring |
| `ANALYTICS_ENGINEER` | dbt, data warehouses |
| `BI_ANALYST` | Dashboards & business reporting |
| `DATA_SCRAPER` | Web scraping & data extraction |

### 🛡️ Security (Red, Blue, Purple)
| Agent | Mission |
|:------|:--------|
| `CISO_BOT` | Security governance & risk management |
| `RED_TEAMER` | Offensive — simulate adversary attacks |
| `BLUE_DEFENDER` | Defensive — detect & mitigate threats |
| `APPSEC_SPECIALIST` | Secure SDLC & code review |
| `CLOUD_SEC_ARCHITECT` | Cloud hardening & IAM |
| `SMART_CONTRACT_AUDITOR` | Web3 smart contract audits |
| `SOCIAL_ENGINEER` | Phishing simulations |
| `PRIVACY_OFFICER` | GDPR/CCPA compliance |

### ⚡ Engineering: Frontend & Mobile
| Agent | Mission |
|:------|:--------|
| `REACT_EXPERT` | High-performance React apps |
| `ANGULAR_MASTER` | Enterprise Angular |
| `NEXTJS_GURU` | SSR & full-stack React |
| `CSS_ARTIST` | Pixel-perfect responsive layouts |
| `IOS_ENGINEER` | Native iOS (Swift/SwiftUI) |
| `ANDROID_ENGINEER` | Native Android (Kotlin) |
| `FLUTTER_DEV` | Cross-platform mobile |
| `GAME_DEV` | Game mechanics & engines |

### ⚙️ Engineering: Backend & Infrastructure
| Agent | Mission |
|:------|:--------|
| `BACKEND_PRINCIPAL` | Scalable backend architecture |
| `NODE_SPECIALIST` | Node/TypeScript backends |
| `PYTHON_BACKEND` | Django/FastAPI backends |
| `GOLANG_ENGINEER` | High-concurrency services |
| `RUST_SYSTEMS` | Memory-safe systems programming |
| `API_ARCHITECT` | API design (REST/GraphQL) |
| `DBA_POSTGRES` | Database optimization & migrations |
| `SEARCH_ENGINEER` | Search engines (Algolia, Elastic) |

### ☁️ Cloud & DevOps
| Agent | Mission |
|:------|:--------|
| `CLOUD_ARCHITECT` | Cloud infrastructure (AWS/GCP) |
| `KUBERNETES_PILOT` | Container orchestration |
| `DEVOPS_AUTOMATOR` | CI/CD pipelines & IaC |
| `SRE_WATCHER` | Site reliability & observability |
| `SERVERLESS_DEV` | Event-driven serverless architectures |

### 🔧 Specialized Tech
| Agent | Mission |
|:------|:--------|
| `BLOCKCHAIN_DEV` | DApps & smart contracts |
| `IOT_MAKER` | Hardware-to-digital (Arduino, MQTT, RPi) |
| `ELECTRON_DEV` | Cross-platform desktop apps |
| `BROWSER_EXTENSION_DEV` | Chrome/Firefox/Edge extensions |
| `SCIENTIFIC_COMPUTING` | Scientific calculations & simulations |

### 🧪 Quality Assurance
| Agent | Mission |
|:------|:--------|
| `QA_DIRECTOR` | Quality strategy & release criteria |
| `PERFORMANCE_TESTER` | Stress testing & bottleneck analysis |
| `TDD_MENTOR` | Test-Driven Development coaching |

### 🏢 Operations & Admin
| Agent | Mission |
|:------|:--------|
| `HR_DIRECTOR` | HR, culture, employee relations |
| `RECRUITER_BOT` | Sourcing candidates & hiring pipeline |
| `LEGAL_COUNSEL` | Contracts, TOS, IP protection |
| `FINANCE_CONTROLLER` | Budgeting, bookkeeping, forecasting |
| `AUTOMATION_ARCHITECT` | Business process automation (no-code) |
| `DOCS_LEAD` | Technical documentation & wikis |
| `EDUCATOR` | Training programs & courses |

### 🌐 Research & Intelligence
| Agent | Mission |
|:------|:--------|
| `DEEP_RESEARCHER` | Exhaustive topic research |
| `TREND_HUNT` | Industry trends & competitor monitoring |
| `ACADEMIC_SYNTHESIZER` | Academic paper summarization |
| `PATENT_ANALYST` | Patent landscape analysis |

> 📋 **Full roster with toolkits:** [`persona_menu.md`](.antigravity/docs/persona_menu.md)

---

## 709+ Agentic Skills

Skills are the **executable knowledge modules** that power each agent. Every skill is a folder inside [`.antigravity/skills/`](.antigravity/skills/) containing a `SKILL.md` with YAML frontmatter and step-by-step instructions.

**Categories include:**

| Category | Examples |
|:---------|:---------|
| **Architecture** | `architecture`, `c4-context`, `senior-architect`, `microservices-patterns` |
| **Business & Marketing** | `copywriting`, `pricing-strategy`, `seo-audit`, `email-sequence`, `paid-ads` |
| **Data & AI** | `rag-engineer`, `prompt-engineer`, `langgraph`, `langchain-architecture` |
| **Development** | `typescript-expert`, `python-patterns`, `react-best-practices`, `flutter-expert` |
| **Infrastructure** | `docker-expert`, `aws-serverless`, `vercel-deployment`, `terraform-specialist` |
| **Security** | `api-security-best-practices`, `sql-injection-testing`, `pentest-commands` |
| **Testing** | `test-driven-development`, `playwright-skill`, `testing-patterns` |
| **Workflow & Automation** | `workflow-automation`, `github-actions-templates`, `n8n-mcp-tools-expert` |
| **Integrations** | `hubspot-automation`, `stripe-integration`, `slack-automation`, `salesforce-automation` |
| **Documents** | `docx`, `xlsx`, `pptx`, `pdf` |

> 📦 **Browse all 709+ skills:** [`skills/`](.antigravity/skills/)

---

## Client Builder — Bespoke Teams in One Command

This is the **killer feature**. Instead of dumping 709+ skills on every project, you can create a **tailored, isolated environment** with only what each client needs.

### How It Works

```
┌────────────────────┐     ┌──────────────────────┐     ┌──────────────────────┐
│  1. RECEPTIONIST   │────▶│  2. CLIENT_BUILDER   │────▶│  3. ISOLATED BRANCH  │
│  (AI Interview)    │     │  (Python Script)     │     │  (Git Branch)        │
│                    │     │                      │     │                      │
│ • Asks about your  │     │ • Creates client dir │     │ client/acme_corp     │
│   business         │     │ • Copies only needed │     │ ├── .antigravity/    │
│ • Identifies tech  │     │   personas & skills  │     │ │   ├── personas/    │
│   stack            │     │ • Generates bespoke  │     │ │   │   ├── MASTER.md│
│ • Maps needs to    │     │   MASTER.md          │     │ │   │   ├── REACT_...│
│   agents           │     │ • Creates git branch │     │ │   │   └── SEO_...  │
│ • Recommends squad │     │ • Pushes to remote   │     │ │   └── skills/     │
└────────────────────┘     └──────────────────────┘     │ │       ├── react-...│
                                                        │ │       └── seo-...  │
                                                        │ └── (clean branch)   │
                                                        └──────────────────────┘
```

### Step 1: Talk to the Receptionist

The [`RECEPTIONIST`](.antigravity/personas/RECEPTIONIST.md) agent conducts a structured interview:

1. **Greeting** — Client name & industry
2. **Assessment** — Tech stack, team structure, marketing needs, pain points
3. **Formulation** — Maps answers to the right personas and skills
4. **Handoff** — Generates the exact build command

### Step 2: Run the Builder

```bash
python3 client_builder.py \
  --name "Acme Corp" \
  --personas PRODUCT_VISIONARY REACT_EXPERT SEO_TECHNICAL CISO_BOT BLUE_DEFENDER \
  --skills vercel-react-best-practices shadcn-ui-best-practices seo-audit
```

### Step 3: A Clean Branch Is Created

The [`client_builder.py`](client_builder.py) script:

1. ✅ Creates a `clients/acme_corp/` directory
2. ✅ Copies only the selected personas and skills
3. ✅ Always includes `SKILL_CREATOR` (so the client can generate missing skills)
4. ✅ Generates a bespoke `MASTER.md` from the [`CLIENT_MASTER_TEMPLATE.md`](.antigravity/CLIENT_MASTER_TEMPLATE.md)
5. ✅ Creates a `client/acme_corp` Git branch
6. ✅ Removes the global `.antigravity/` from the branch (isolation!)
7. ✅ Commits, pushes, and returns to `main`

**Result:** Each client gets their own branch with a **focused, relevant team** — no noise from the 700+ skills they don't need.

---

## Quick Start

### Option 1: Clone & Use the Full System

```bash
git clone https://github.com/alexreska/Antigravity.git
cd Antigravity
```

Start using the MASTER orchestrator with your AI assistant:

> *"Read `.antigravity/personas/MASTER.md` and act as the MASTER orchestrator. I need help building a React SaaS with SEO."*

### Option 2: Create a Client-Specific Branch

```bash
# 1. Clone the repo
git clone https://github.com/alexreska/Antigravity.git
cd Antigravity

# 2. Run the client builder
python3 client_builder.py \
  --name "My Project" \
  --personas REACT_EXPERT NEXTJS_GURU SEO_TECHNICAL UI_ARCHITECT \
  --skills react-best-practices nextjs-best-practices seo-audit tailwind-design-system

# 3. Switch to the client branch
git checkout client/my_project
```

### Option 3: Let the Receptionist Guide You

> *"Read `.antigravity/personas/RECEPTIONIST.md` and act as the Receptionist. I want to onboard a new client."*

The AI will interview you and generate the exact `client_builder.py` command for your needs.

---

## Project Structure

```
Antigravity/
├── .antigravity/                    # 🧠 The Brain (Multi-Agent System)
│   ├── personas/                    #    80+ Specialized Agent Personas
│   │   ├── MASTER.md                #    👑 The Orchestrator
│   │   ├── RECEPTIONIST.md          #    🤝 Client Onboarding Agent
│   │   ├── SKILL_CREATOR.md         #    🏭 On-Demand Skill Generator
│   │   ├── CHIEF_OF_STAFF.md        #    Executive & Strategy
│   │   ├── REACT_EXPERT.md          #    Frontend Specialist
│   │   ├── RED_TEAMER.md            #    Security Specialist
│   │   ├── CMO_BOT.md               #    Marketing Specialist
│   │   └── ... (80+ more)           #    Full roster
│   │
│   ├── skills/                      #    🛠️ 709+ Executable Skill Modules
│   │   ├── react-best-practices/    #    Each skill is a folder
│   │   │   └── SKILL.md             #    with a SKILL.md definition
│   │   ├── seo-audit/
│   │   ├── docker-expert/
│   │   └── ... (709+ more)
│   │
│   ├── docs/                        #    📚 System Documentation
│   │   ├── AGENT_PROTOCOL.md        #    Hierarchy & engagement rules
│   │   ├── persona_menu.md          #    Full agent roster with toolkits
│   │   └── PARANOIC_TEST.md         #    Audit checklist template
│   │
│   ├── CLIENT_MASTER_TEMPLATE.md    #    Template for client-specific MASTER
│   └── rules.md                     #    Global guardrails
│
├── client_builder.py                # 🤖 Creates isolated client branches
└── README.md                        # 📖 You are here
```

---

## Key System Files

| File | Purpose |
|:-----|:--------|
| [`MASTER.md`](.antigravity/personas/MASTER.md) | The orchestrator — analyzes requests and delegates to specialists |
| [`RECEPTIONIST.md`](.antigravity/personas/RECEPTIONIST.md) | Interviews users to identify the right personas and skills for their project |
| [`SKILL_CREATOR.md`](.antigravity/personas/SKILL_CREATOR.md) | Generates new skills on demand when a capability is missing |
| [`AGENT_PROTOCOL.md`](.antigravity/docs/AGENT_PROTOCOL.md) | The formal hierarchy and engagement rules for all agents |
| [`persona_menu.md`](.antigravity/docs/persona_menu.md) | Complete roster of 80+ agents with their missions and toolkits |
| [`CLIENT_MASTER_TEMPLATE.md`](.antigravity/CLIENT_MASTER_TEMPLATE.md) | Template used to generate client-specific MASTER files |
| [`client_builder.py`](client_builder.py) | Python script that creates isolated client branches |
| [`rules.md`](.antigravity/rules.md) | Global project guardrails and safety checks |
| [`PARANOIC_TEST.md`](.antigravity/docs/PARANOIC_TEST.md) | 30-check paranoia-level audit checklist |

---

## How It All Works Together

```
  YOU: "I need a React SaaS with SEO and security"
   │
   ▼
  RECEPTIONIST interviews you
   │
   ▼
  Identifies: REACT_EXPERT, NEXTJS_GURU, SEO_TECHNICAL,
              CISO_BOT, UI_ARCHITECT
   │
   ▼
  client_builder.py creates branch: client/your_project
   │
   ▼
  On the branch, MASTER orchestrates:
   │
   ├─▶ PRODUCT_VISIONARY writes the PRD
   ├─▶ UI_ARCHITECT designs the component library
   ├─▶ REACT_EXPERT builds the frontend
   ├─▶ SEO_TECHNICAL optimizes for search
   ├─▶ CISO_BOT audits security
   └─▶ QA_DIRECTOR validates the release
   │
   ▼
  If a skill is missing, SKILL_CREATOR generates it
   │
   ▼
  MASTER reviews everything before presenting to you
```

### Key Principles

1. **Specialization over Generalization** — Every agent has a focused mission and specific toolkit
2. **Delegation, Not Execution** — The MASTER never codes; it routes to specialists
3. **Isolation** — Client branches contain only relevant agents, reducing noise and context
4. **Self-Healing** — Missing skills are generated on-the-fly by `SKILL_CREATOR`
5. **Protocol-Driven** — Every interaction follows the [`AGENT_PROTOCOL.md`](.antigravity/docs/AGENT_PROTOCOL.md) workflow

---

## Compatibility

This system works with any AI coding assistant that can read markdown files as context:

| Tool | How to Use |
|:-----|:-----------|
| **Antigravity IDE** | Load persona files as agent context |
| **Claude Code** | Reference `.antigravity/personas/MASTER.md` in conversation |
| **Gemini CLI** | Point to persona files with `Use MASTER.md...` |
| **Cursor** | Add persona files to your context with `@` |
| **GitHub Copilot** | Paste persona content into chat |
| **Codex CLI** | Reference persona files in prompts |

---

## License

MIT License. See [LICENSE](LICENSE) for details.

---

## Support

If this project helps you, ⭐ **star the repo** — it helps others discover it.

Questions or ideas? [Open an issue](https://github.com/alexreska/Antigravity/issues).
