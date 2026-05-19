# Awesome GitHub Agentic AI [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Deploying, operating, and governing AI agents in GitHub software development lifecycle workflows using Copilot.

[![GitHub Stars](https://img.shields.io/github/stars/sk3pp3r/awesome-github-agentic-ai?style=flat-square&logo=github&color=7c3aed)](https://github.com/sk3pp3r/awesome-github-agentic-ai/stargazers)
[![License: CC0](https://img.shields.io/badge/License-CC0-green.svg?style=flat-square)](LICENSE)
[![GH-600](https://img.shields.io/badge/Exam-GH--600-blueviolet?style=flat-square&logo=github)](https://learn.microsoft.com/credentials/certifications/github-copilot/)

<p align="center">
  <img src="https://learn.microsoft.com/media/learn/certification/badges/microsoft-certified-associate-badge.svg" alt="GitHub Certified: Agentic AI Developer" width="140"/>
</p>

---

## Contents

- [🧠 What Is GH-600](#-what-is-gh-600)
- [📋 Exam Blueprint](#-exam-blueprint)
- [📚 Official Study Resources](#-official-study-resources)
- [🎓 Microsoft Learn Modules (Self-Paced)](#-microsoft-learn-modules-self-paced)
- [📦 Domain Deep-Dives](#-domain-deep-dives)
- [🧰 Labs and Hands-On Practice](#-labs-and-hands-on-practice)
- [🌐 Community and Social](#-community-and-social)
- [📺 Video Resources](#-video-resources)
- [✅ Best Starting Points](#-best-starting-points)

---

## 🧠 What Is GH-600

The **GitHub Certified: Agentic AI Developer** (exam code **GH-600**) is the next-generation certification proving you can design, build, evaluate, and operate **autonomous AI agents** deeply embedded in the software development lifecycle.

This isn't your grandpa's chatbot cert. 😤 GH-600 covers the full agentic stack:

- 🏗️ Architecting agents with clear goals, boundaries, and tool access
- ⚡ Implementing tool use, API integrations, and environment interaction
- 🧩 Managing memory, state, context windows, and execution flow
- 📊 Evaluating agent quality, safety, latency, and cost — in CI/CD
- 🕸️ Orchestrating multi-agent systems with roles, contracts, and protocols
- 🛡️ Enforcing guardrails, human-in-the-loop, audit logs, and compliance

If you're serious about agentic AI engineering on GitHub — this list is your unfair advantage. 😎

---

## 📋 Exam Blueprint

| # | Domain                                       | Weight |
| - | -------------------------------------------- | ------ |
| 1 | Prepare Agent Architecture & SDLC Processes  | 15-20% |
| 2 | Implement Tool Use & Environment Interaction | 20-25% |
| 3 | Manage Memory, State & Execution             | 10-15% |
| 4 | Perform Evaluation, Error Analysis & Tuning  | 15-20% |
| 5 | Orchestrate Multi-Agent Coordination         | 15-20% |
| 6 | Implement Guardrails & Accountability        | 10-15% |

> 💡 **Tip:** Domain 2 (Tool Use) carries the most weight at 20-25%. Nail tool schemas, secrets management, and idempotency.

---

## 📚 Official Study Resources

> Start here. No shortcuts.

- 🎯 [Microsoft Learn — GitHub Certifications Hub](https://learn.microsoft.com/en-us/credentials/certifications/github-copilot/) - The mothership. All GitHub certs in one place.
- 📋 [Exam GH-600 Page](https://learn.microsoft.com/credentials/certifications/exams/gh-600/) - Register, review skills measured, download the study guide.
- 📖 [GH-600 Official Study Guide](https://learn.microsoft.com/credentials/certifications/resources/study-guides/gh-600) - The definitive objective-by-objective breakdown. Read it twice.
- 📣 [Microsoft Tech Community Announcement](https://techcommunity.microsoft.com/blog/skills-hub-blog/new-github-certified-agentic-ai-developer/4517571) - The official launch post with context on why this cert exists.
- 💬 [GitHub Community Discussions — GH-600](https://github.com/search?q=GH-600&type=discussions) - Real talk from folks prepping for the exam. Bookmark it.

---

## 🎓 Microsoft Learn Modules (Self-Paced)

> Free. Official. Exam-aligned. No excuses.

- 🤖 [Foundations of Agentic AI in GitHub](https://learn.microsoft.com/en-us/training/modules/foundations-agentic-ai/) - Core concepts: what agents are, how they reason, plan, and act within GitHub workflows.
- 🏗️ [Designing Agent Architecture and SDLC Integration](https://learn.microsoft.com/en-us/training/modules/design-agent-architecture-integration/) - Covers Domain 1 deeply. Agent goals, task decomposition, model selection, SDLC workflows.
- 🔧 [Tooling, MCP, and Agent Execution Environments](https://learn.microsoft.com/en-us/training/modules/agent-tooling-mcp-execution-environments/) - Tool schemas, MCP protocol, safe execution, secrets, side effects.

---

## 📦 Domain Deep-Dives

> Know your domains cold. Here's the full breakdown of what's actually tested.

---

### Domain 1

**What you need to know:**

- 🎯 Define agent goals, roles, and operational boundaries.
- 🔀 Decompose complex tasks into agent-executable sub-tasks.
- 🧩 Choose the right models, tools, and data sources for the job.
- 📐 Design SDLC workflows that integrate agents at the right points.
- 📌 Version prompts, tools, and configurations like any other code artifact.

**Key Artifacts:**

- 📐 Architecture diagrams — Visualize agent topology and data flow.
- 📋 Agent spec (YAML/JSON) — Define roles, goals, constraints, tool access.
- 🔄 Workflow and quality gates — Embed agents into CI/CD with approval steps.
- ⚠️ Risk assessment — Identify failure modes before they hit prod.

**GitHub Features to Know:**
`Projects` · `README / ADRs` · `CODEOWNERS` · `Milestones`

---

### Domain 2

**What you need to know:**

- 📝 Design and implement tool schemas (JSON Schema — be precise).
- 🔒 Enable safe tool execution (sandboxing, input validation, output sanitization).
- 🔗 Integrate agents with APIs, databases, CLIs, and file systems.
- 🤫 Manage secrets securely — never hardcode, always rotate.
- ♻️ Handle side effects and ensure idempotency for retryable operations.

**Key Artifacts:**

- 📄 Tool schemas (JSON) — Machine-readable tool contracts for agents.
- 🔌 Connector code — Actual integrations to external systems.
- ⚙️ Environment configs — Per-environment secrets, vars, and feature flags.
- 🔐 Secrets management — Vault strategies, GitHub Secrets, OIDC.

**GitHub Features to Know:**
`Actions` · `Secrets & Variables` · `Environments` · `Packages`

---

### Domain 3

**What you need to know:**

- 🗃️ Choose memory strategies: episodic, semantic, or hybrid — and when each applies.
- 💾 Persist and retrieve state reliably across agent runs.
- 📏 Manage context windows — trim, summarize, compress without losing signal.
- ⏸️ Enable checkpoints and resumption for long-running agentic tasks.
- 🎲 Ensure determinism where it matters (avoid flaky agent behavior).

**Key Artifacts:**

- 🧠 Memory design doc — Strategy for episodic vs. semantic vs. hybrid.
- 📋 State schemas — Typed definitions of what gets persisted.
- 💾 Storage configs — Database/vector store/cache configuration.
- ⏸️ Checkpoint strategy — How and when to snapshot agent state.

**GitHub Features to Know:**
`Artifacts` · `Cache` · `Releases` · `Discussions`

---

### Domain 4

**What you need to know:**

- 🧪 Build evaluation datasets and test harnesses for your agents.
- 📐 Define metrics across four axes: quality, safety, latency, cost.
- 🤖 Run automated evals in CI/CD — every PR, every deploy.
- 🔍 Analyze errors and failure modes systematically (not just vibes).
- 🔄 Tune prompts, tools, and models iteratively based on eval data.

**Key Artifacts:**

- 📊 Eval datasets — Ground truth pairs for automated scoring.
- 🧪 Test harnesses — Frameworks that run evals and assert thresholds.
- 📈 Metrics and reports — Dashboards showing quality/safety/latency/cost.
- 📝 Tuning logs — Experiment tracking for prompt/tool changes.

**GitHub Features to Know:**
`Actions (CI)` · `Code Scanning` · `Pages (Reports)` · `Pull Requests`

---

### Domain 5

**What you need to know:**

- 🎭 Design agent roles, contracts, and interaction protocols.
- 🔀 Coordinate via workflows and events (not spaghetti message passing).
- 📡 Master communication patterns: plan, debate, delegate, critique.
- ⚖️ Resolve conflicts and aggregate results from multiple agents.
- 🔭 Monitor and trace multi-agent behavior end-to-end.

**Key Artifacts:**

- 📄 Agent contracts — Formal definitions of agent capabilities/interfaces.
- 🗺️ Orchestration flows — Workflow diagrams showing agent coordination.
- 📡 Communication logs — Structured logs of inter-agent messages.
- 🔭 Trace visualizations — Spans and traces for debugging multi-agent flows.

**GitHub Features to Know:**
`Actions (Workflows)` · `Events (Webhooks)` · `Artifacts` · `Projects`

---

### Domain 6

**What you need to know:**

- 🚧 Implement content safety and policy guardrails (input and output).
- 🔐 Enforce least privilege — agents only get what they need.
- 👤 Add human-in-the-loop for high-risk or irreversible actions.
- 📝 Audit, log, and trace every decision an agent makes.
- ✅ Ensure compliance with data governance and regulatory requirements.

**Key Artifacts:**

- 🚧 Guardrail policies — Rules for what agents can/cannot do or say.
- ⚖️ Risk levels and rules — Tiered risk classification for actions.
- 📋 Audit logs — Immutable record of agent decisions and actions.
- 🗂️ Compliance mapping — Traceability to regulatory frameworks.

**GitHub Features to Know:**
`CODEOWNERS` · `Branch Protection` · `Audit Log` · `Dependabot`

---

## 🧰 Labs and Hands-On Practice

> Theory is nice. Building stuff is how you actually learn. 😤

- 🎮 [GitHub Skills](https://skills.github.com/) - Interactive, repo-based learning tracks. Build real workflows, get automated feedback.
- 📘 [GitHub Copilot Docs](https://docs.github.com/en/copilot) - Full documentation for GitHub Copilot, including agent mode, custom instructions, and workspace features.
- 🔌 [GitHub Copilot Extensions](https://docs.github.com/en/copilot/building-copilot-extensions) - Build your own Copilot extensions. Perfect for practicing tool schemas and agent integration patterns.
- ⚡ [GitHub Actions Docs](https://docs.github.com/en/actions) - Master the workflow engine that powers agent orchestration, CI/CD evals, and automated deployment.

### 🎯 Hands-On Build Checklist

Use the GH-600 study guide objective domains as your checklist. For each domain, build a small working artifact:

1. 🏗️ Domain 1 — Write an agent spec (YAML) for a code review agent with goals, tool access, and boundaries.
2. 🔧 Domain 2 — Implement a tool with a valid JSON Schema definition. Call it from a GitHub Action.
3. 🧠 Domain 3 — Build a simple state persistence mechanism using GitHub Artifacts and Cache.
4. 📊 Domain 4 — Create an eval harness for a Copilot extension. Define at least 3 metrics.
5. 🕸️ Domain 5 — Design a 2-agent orchestration flow using GitHub Actions workflows and webhooks.
6. 🛡️ Domain 6 — Add a content safety guardrail and a human approval gate to a GitHub Actions workflow.

---

## 🌐 Community and Social

> Don't study alone. The agentic AI community is loud, helpful, and building cool stuff. 🤝

- 🔴 [Reddit — r/AzureCertification GH-600 Thread](https://www.reddit.com/r/AzureCertification/comments/1td90hq/gh600_new_github_certified_agentic_ai_developer/) - Community discussion on the new cert. Exam experiences, prep tips, study group coordination.
- 💼 [LinkedIn — Microsoft Learn Announcement](https://www.linkedin.com/posts/microsoftlearn_were-introducing-a-new-github-certified-activity-7460713084647804928-_wqQ/) - Official launch post with context and industry reactions.
- 🐦 [X/Twitter — Microsoft Learn Announcement](https://x.com/MicrosoftLearn/status/2054969993410818299) - Short-form updates and community reactions.
- 📰 [GitHub Blog — Copilot Tag](https://github.blog/tag/github-copilot/) - Official GitHub engineering blog. Deep dives on Copilot features, agentic capabilities, and new integrations.
- 📋 [GitHub Copilot Changelog](https://github.blog/changelog/label/copilot/) - Every Copilot feature release, documented. Stay current.
- 💬 [GitHub Community Discussions](https://github.com/orgs/community/discussions) - The official GitHub community. Ask questions, share projects, find study partners.

---

## 📺 Video Resources

> Watch people build things. Then build things. 🎬

- ▶️ [YouTube — GitHub Copilot Agentic AI](https://www.youtube.com/results?search_query=GitHub+Copilot+agentic+AI+GH-600) - Search results for GH-600 and agentic AI content. New videos dropping regularly.
- 🎙️ [Microsoft Learn Shows — GitHub Copilot](https://learn.microsoft.com/en-us/shows/browse?terms=github+copilot) - Official Microsoft Learn video content. Structured, exam-relevant, free.

---

## ✅ Best Starting Points

> New here? Don't know where to begin? Here's your ordered attack plan. 😎

1. 📋 Read the Official Study Guide - Understand every objective before touching anything else.
2. 🎓 Complete the 3 Microsoft Learn Modules - Official, exam-aligned, free. Build the mental model.
3. 🏗️ Study the Domain Deep-Dives - Know the key topics, artifacts, and GitHub features cold for each domain.
4. 🛠️ Do the Hands-On Build Checklist - Build one artifact per domain. Learning by doing > passive reading.
5. 💬 Join the Community - Reddit thread, GitHub Discussions. Find others prepping. Share what you build.

---

## Contributing

See [contributing.md](contributing.md) for guidelines on how to contribute to this list.

---

<p align="center">
  Built with 😎 for the GitHub Agentic AI community<br/>
  <strong>Go build something that thinks for itself.</strong> 🤖
</p>
