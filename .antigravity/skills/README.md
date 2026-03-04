# 🛠️ Skills Directory — 709+ Agentic Skills

> The executable knowledge modules that power the [Antigravity Dream Team](../../README.md).

---

## What Are Skills?

Skills are **specialized instruction sets** that teach AI agents how to handle specific tasks. Each skill is a folder containing a `SKILL.md` file with YAML frontmatter and step-by-step procedures.

Think of them as **expert knowledge modules** your agents load on-demand. When the MASTER delegates a task to `REACT_EXPERT`, that agent reaches for skills like `react-best-practices` and `react-patterns` from its toolkit.

```
skills/
├── react-best-practices/     # Each skill lives in its own folder
│   ├── SKILL.md              # Core definition (required)
│   ├── scripts/              # Helper scripts (optional)
│   ├── examples/             # Usage examples (optional)
│   └── resources/            # Templates & resources (optional)
```

---

## How Skills Connect to Agents

Skills don't exist in isolation — they are the **toolkit** of each [persona](./../personas/). When the MASTER assigns work to an agent, that agent uses its assigned skills:

```
MASTER → assigns task to REACT_EXPERT
         REACT_EXPERT uses:
           ├── react-best-practices
           ├── react-patterns
           ├── react-state-management
           └── performance-profiling
```

> **Missing a skill?** The [`SKILL_CREATOR`](../personas/SKILL_CREATOR.md) agent can generate new skills on-the-fly following the Antigravity standard.

---

## Skill Categories

### 🎨 Creative & Design
`algorithmic-art` · `canvas-design` · `frontend-design` · `ui-ux-pro-max` · `web-artifacts-builder` · `theme-factory` · `brand-guidelines-anthropic` · `figma-to-code` · `stitch-ui-design` · `mobile-design`

### ⚡ Development & Engineering
`react-best-practices` · `nextjs-best-practices` · `typescript-expert` · `python-patterns` · `flutter-expert` · `golang-pro` · `rust-pro` · `java-pro` · `dotnet-architect` · `fastapi-pro` · `django-pro` · `nestjs-expert` · `angular-best-practices`

### 🧠 Data & AI
`rag-engineer` · `prompt-engineer` · `langgraph` · `langchain-architecture` · `llm-app-patterns` · `ai-agents-architect` · `autonomous-agents` · `embedding-strategies` · `vector-database-engineer` · `computer-vision-expert`

### 🛡️ Security
`api-security-best-practices` · `sql-injection-testing` · `pentest-commands` · `vulnerability-scanner` · `burp-suite-testing` · `metasploit-framework` · `red-team-tactics` · `ethical-hacking-methodology` · `cloud-penetration-testing`

### ☁️ Infrastructure & DevOps
`docker-expert` · `terraform-specialist` · `aws-serverless` · `kubernetes-architect` · `github-actions-templates` · `vercel-deployment` · `gcp-cloud-run` · `helm-chart-scaffolding` · `gitops-workflow`

### 📊 Business & Marketing
`copywriting` · `seo-audit` · `pricing-strategy` · `email-sequence` · `paid-ads` · `marketing-ideas` · `competitive-landscape` · `startup-financial-modeling` · `content-marketer`

### 🧪 Testing & QA
`test-driven-development` · `playwright-skill` · `testing-patterns` · `e2e-testing-patterns` · `python-testing-patterns` · `javascript-testing-patterns` · `performance-profiling`

### 🔗 Integrations (50+)
`hubspot-automation` · `stripe-integration` · `salesforce-automation` · `slack-automation` · `discord-automation` · `jira-automation` · `notion-automation` · `zapier-make-patterns` · `n8n-mcp-tools-expert` · `whatsapp-automation` · `telegram-automation` · and many more

### 📄 Documents
`docx` · `xlsx` · `pptx` · `pdf`

---

## Using Skills

### With the Multi-Agent System
When using the full Antigravity system, you don't invoke skills directly — the **MASTER delegates to agents**, and agents use their toolkit skills automatically.

### Standalone Usage
You can also use skills directly with any AI assistant:

```
> Use the @react-best-practices skill to review my component
> Apply @seo-audit to analyze my website
> Use @test-driven-development to help me write tests for this module
```

---

## Creating New Skills

Use the [`SKILL_CREATOR`](../personas/SKILL_CREATOR.md) agent, or create manually:

```markdown
---
name: my-new-skill
description: "One-line summary of what this skill does"
---

# Skill Name

## Prerequisites
- [Required tools or access]

## Step-by-Step Procedure
1. **[Action]:** [Instruction]
2. **[Action]:** [Instruction]

## Best Practices
- [Do X, not Y because of Z]

## Troubleshooting
- If [error], then [fix]
```

**Rules:**
- Use YAML frontmatter + Markdown body
- Action-oriented — use imperative verbs
- No fluff — no `README.md` or changelog, only `SKILL.md`
- Portable — no hardcoded paths

---

## Relevant Links

- [Main README](../../README.md) — Full system overview
- [Agent Protocol](../docs/AGENT_PROTOCOL.md) — How agents use skills
- [Persona Menu](../docs/persona_menu.md) — 80+ agents and their toolkits
- [Skill Creator](../personas/SKILL_CREATOR.md) — Generate new skills on demand
