# Trinity AI Collaboration Framework

> **Leave a Thinking Gap Between Capability and Action.**

Trinity is not a tool, nor software. It is a **relational protocol** that defines how humans and AI divide work, communicate, and grow together. Built on a three-layer role separation of **Decision Maker → Planner → Executor**, it uses standardized information flow and negative feedback mechanisms to keep humans in control as AI capabilities grow exponentially.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## Table of Contents

- [Why Trinity?](#why-trinity)
- [Three-Layer Role Separation](#three-layer-role-separation)
- [Cognitive Community: Three Roles, One System](#cognitive-community-three-roles-one-system)
- [The Buffer Layer: Core Innovation](#the-buffer-layer-core-innovation)
- [Adaptive Planning: Sensing the Decision Maker's State](#adaptive-planning-sensing-the-decision-makers-state)
- [Six-Step Closed Loop Collaboration](#six-step-closed-loop-collaboration)
- [Psychological Foundation: Observe-Understand-Describe-Predict](#psychological-foundation-observe-understand-describe-predict)
- [Information Architecture: The External Cognitive System](#information-architecture-the-external-cognitive-system)
- [Knowledge Sovereignty: You Don't Rely on Any AI](#knowledge-sovereignty-you-dont-rely-on-any-ai)
- [Negative Feedback: The System's Immune Mechanism](#negative-feedback-the-systems-immune-mechanism)
- [Antifragile: Learning from Impact](#antifragile-learning-from-impact)
- [Autonomous Learning: Self-Evolution in Idle Time](#autonomous-learning-self-evolution-in-idle-time)
- [Theoretical Foundations](#theoretical-foundations)
- [Practical Validation](#practical-validation)
- [Core Concepts at a Glance](#core-concepts-at-a-glance)
- [Comparison with Traditional AI Agent Usage](#comparison-with-traditional-ai-agent-usage)
- [Limitations](#limitations)
- [Quick Start](#quick-start)
- [Use Cases](#use-cases)
- [Contributing](#contributing)
- [License](#license)

---

## Why Trinity?

### Three Fatal Flaws

Current AI agents commonly suffer from three critical flaws:

| Flaw | Manifestation | Consequence |
|:----|:--------------|:------------|
| **Forgetfulness** | Context window limits cause the AI to forget core rules in long conversations | The same constraint must be repeated; violation rates increase with conversation length |
| **Misinterpretation** | The ambiguity of natural language leads to execution errors | "Check the parameters of this API" may be interpreted as "Call this API" — one word, vastly different outcomes |
| **Over-action** | Lack of critical thinking — executing instructions without considering consequences | Given "list all admins," may directly execute "SELECT * FROM admin_users" and output all data |

### The Fragility of the Linear Chain

Traditional human-AI interaction is a linear chain: **Human → AI → Human**. When AI capabilities were limited, this was workable — the AI could at most provide wrong answers.

But when AI has the power to take consequential actions (write files, call APIs, modify configurations, analyze internal systems), any deviation in the linear chain can be disastrous. A misinterpreted parameter name can waste six rounds of effort. A vague "find the original" instruction can build an entire operation on the wrong foundation.

**Trinity's core insight:** The problem is not that AI is not smart enough — it's that the communication protocol between humans and AI is too crude.

---

## Three-Layer Role Separation

Trinity's core solution is to reframe the traditional one-on-one human-AI interaction into three clearly bounded roles:

```
┌─────────────┐       ┌─────────────┐       ┌─────────────┐
│ Decision    │ ←──→ │ Planner     │ ←──→ │ Executor    │
│ Maker       │       │ (Reasoning) │       │ (Tool AI)   │
│ (Human)     │       │             │       │             │
│ Bears       │       │ Designs     │       │ Executes    │
│ consequences│       │ solutions   │       │ tasks       │
└─────────────┘       └─────────────┘       └─────────────┘
      ↑                    ↑                    ↑
  Sets direction      Translates tasks     Executes ops
  Makes decisions     Flags risks          Validates output
  Reviews plans       Analyzes strategy    Records results
```

### Decision Maker (Human)

- Sets direction and objectives
- Reviews plans and risks
- Makes final decisions
- Bears all consequences

### Planner (Reasoning AI)

- Understands deep needs
- Questions the rationality of proposed approaches
- Flags potential risks
- Translates natural language into structured instructions

### Executor (Tool AI)

- Executes instructions precisely
- Reports actual output
- Generates task summaries automatically
- Updates the knowledge repository

### Boundary Rules

The three roles are **not equal** — there are clear hierarchies and checks and balances:

- **The Executor cannot change the plan** — unexpected situations must be escalated, not self-decided
- **The Planner cannot make decisions for the Decision Maker** — only analysis, warnings, and suggestions
- **The Decision Maker should not bypass the Planner to directly command the Executor** — any operation skipping the buffer layer is high-risk

---

## Cognitive Community: Three Roles, One System

Trinity is not just three roles collaborating — it is a **unified cognitive system**.

Each role's cognition is shaped by the others. This mutual shaping relationship is the core engine of the framework's self-evolution:

- **The Executor's behavioral data** updates the Planner's judgment rules. Every success or failure is structured into task summaries and pulse logs, becoming the raw material for the Planner to identify patterns and extract decision rules.
- **The Planner's analytical framework** guides the Executor's action direction. The Planner translates vague directions into structured instructions, defining what constitutes "correct" execution.
- **The Decision Maker's feedback** calibrates the entire system's value baseline — what's worth doing, what's not, what's the priority.

```
  Decision Maker feedback ──→ Calibrates value baseline
        ↑                              ↓
  Planner analysis ──→ Guides action direction
        ↑                              ↓
  Executor data ──→ Updates judgment rules
```

This means: **learning is shared.** The longer the system runs, the deeper the three roles understand each other, and the higher the collaboration synergy becomes.

---

## The Buffer Layer: Core Innovation

Between the Decision Maker and the Executor, Trinity inserts a **Buffer Layer** — the Planner — that does not participate in concrete operations. The Buffer Layer has four core functions:

### 1. Transparent Presentation

Before the Decision Maker decides, present a complete picture of the task: what the goal is, which systems are involved, what constraints exist, and what outputs are expected.

### 2. Risk Warning

Before high-risk operations, present complete consequences and alternative paths:

> Executor about to "batch reset admin passwords" →
>
> Planner warns: "This operation affects 11 admin accounts. Known risks: 1) The system rejects purely numeric passwords; 2) Some accounts may fail due to insufficient privileges; 3) Old passwords are not recoverable. Recommendation: back up current passwords first, test on one account before batch execution."

### 3. Precise Translation

Turn natural language into precise structured instructions:

> "Check if this app has security vulnerabilities"
>
> → Structured task:
> ```
> Goal: Assess target software security
> Method: Static analysis (file → strings → nm → otool → codesign)
> Scope: No dynamic execution or network scanning
> Delivery: Security assessment report (findings + risk levels + remediation recommendations)
> ```

### 4. Proactive Suggestions

When potential directions might be overlooked, proactively suggest them — not wait for the Decision Maker to ask.

### The Buffer Layer's Philosophy

The Buffer Layer **never rejects a direction.** It only provides analysis, warnings, and suggestions. The final decision always rests with the human. This is the essential difference between Trinity and any "AI safety guardrail": guardrails **block** — the Buffer Layer **informs.**

---

## Adaptive Planning: Sensing the Decision Maker's State

The Planner analyzes not just the task, but also attunes to the Decision Maker's energy level, interests, and risk tolerance — adjusting its communication accordingly.

### Energy Awareness

- Decision Maker is energetic → Plan more complex solutions, offer multiple options to weigh
- Decision Maker is tired → Simplify options, reduce choices, or proactively suggest "I can draft the plan first — review it when you're rested"

### Risk Attunement

- Decision Maker risk-seeking → Plan aggressive approaches with **clearly labeled** risk levels
- Decision Maker risk-averse → Plan conservative approaches with rollback steps for each phase

### Boundary Awareness

This adaptation is **not guessing.** It's based on conversation patterns, task rhythm, and information the Decision Maker proactively shares. When the Planner cannot determine the Decision Maker's state, it asks directly:

> "This task has two directions: A is higher risk but higher reward, B is more conservative. What's your current preference?"

The Planner avoids over-interpreting. **When in doubt, ask — this is the Planner's first principle.**

---

## Six-Step Closed Loop Collaboration

Every task, from start to finish, must complete six standardized steps:

```
① Idea → ② Requirement → ③ Plan → ④ Command → ⑤ Execution → ⑥ Review
Proposal  Confirmation  Design  Issue  Report  & Archive
```

### Outputs per Step

| Step | Output | Purpose |
|:----|:-------|:--------|
| ① Idea Proposal | Raw instruction | Record the Decision Maker's original intent |
| ② Requirement Confirmation | Confirmed requirement description | Eliminate ambiguity; ensure mutual understanding |
| ③ Plan Design | Execution plan + risk assessment | Basis for Decision Maker's review |
| ④ Command Issue | Structured instruction + checklist | Executor's execution basis |
| ⑤ Execution Report | Results + validation report | Record what was done and what was achieved |
| ⑥ Review & Archive | Task summary + learnings | Knowledge deposited into the repository |

**No archive = task not complete.** If experience is not distilled into the knowledge base, the task is only half done.

---

## Psychological Foundation: Observe-Understand-Describe-Predict

Trinity's six-step loop maps directly to the psychological **Observe-Comprehend-Describe-Predict** framework. This is no coincidence — this framework is the human cognitive cycle, which AI should mirror in collaboration.

| Phase | Corresponding | Output | Role |
|:------|:--------------|:-------|:-----|
| **Observe** | Executor's task summaries + pulse logs | Raw data, no judgment | Executor |
| **Comprehend** | Planner's review analysis | Identify patterns, anomalies, risks | Planner |
| **Describe** | Planner's structured prompts | Verifiable, actionable | Planner |
| **Predict** | Planner's risk assessment + direction recommendations | Confidence levels labeled | Planner → Decision Maker |

Each cycle makes the system understand problems more accurately and solve them more efficiently. The first cycle may have large deviations (the Planner doesn't yet know the Decision Maker's preferences), but after a few cycles, deviations converge rapidly — this is essentially **Bayesian updating** applied to collaboration.

---

## Information Architecture: The External Cognitive System

Trinity uses a set of standardized information tools to "offload" cognition to an external system. At the start of each session, the Planner restores global awareness within seconds by reading the Commander's Briefing.

### Three-Layer Index System

| Layer | Tool | Coverage | Purpose |
|:------|:-----|:---------|:--------|
| **Daily** | Commander's Briefing | Last 7 days' dynamics | Quick global awareness recovery |
| **Weekly** | Capability Map | All current Skills and rules | Full framework capability view |
| **Topic** | Decision rules + Learnings | By domain | Scenario-specific reference |

### Knowledge Repository Structure

```
knowledge_base/
├── decisions/       # Decision rules — lessons distilled from every mistake
├── capabilities/    # Capability inventory — all current capabilities rated by maturity
├── learning/        # Learning records — structured error documentation
├── pulse/           # Pulse logs — real-time operation stream
├── daily/           # Daily logs — daily work summaries
├── tasks/           # Task summaries — complete record of every task
├── templates/       # Standardized templates — format specs for each step
└── skills/          # AI-readable skill documents
```

### Information Fidelity Mechanisms

Information naturally degrades as it passes between three roles. Trinity implements four layers of protection:

1. **Source Attribution** — Every conclusion must cite its source (which task, which analysis, which rule)
2. **Confidence Labeling** — Every piece of information is rated (🟢 High / 🟡 Speculative / 🔴 Uncertain), with reason
3. **Briefing Self-Check** — Each Commander's Briefing is automatically checked against original outputs for deviations
4. **Periodic Validation** — Weekly consistency check of the entire knowledge repository

---

## Knowledge Sovereignty: You Don't Rely on Any AI

The most fundamental design principle of Trinity: **all knowledge is stored locally, independent of any specific AI or cloud service.**

This means:

- **Switch AI tools, your knowledge base remains intact.** If you use DeepSeek today and want to switch to Claude tomorrow, just point the new AI to the knowledge repository — it can read and restore full collaboration capabilities within minutes.
- **The knowledge base can be read and edited with any text editor.** All files are standard Markdown — no proprietary software needed.
- **No vendor lock-in.** Trinity is designed to run on any AI system that can read and write Markdown files.
- **The Decision Maker always has full data control.** No cloud sync, no data leakage risk, no platform dependency.

**Knowledge Sovereignty is the foundation of Trinity's replicability.** If knowledge is locked inside a specific AI's memory, Trinity is just another AI helper tool. Only when knowledge flows freely as plain text can Trinity truly become a collaboration system independent of any AI.

---

## Negative Feedback: The System's Immune Mechanism

Any system that relies solely on positive feedback will eventually crash from runaway growth. Trinity has three built-in layers of constraint:

### 1. Executor Self-Check Checklist

After every task, the Executor must answer:

```
☐ Did I execute any unauthorized operation?
☐ Did I make any decision under a vague instruction?
☐ Did I skip any validation step?
☐ Did I complete the archive?
```

**Any "Yes" → Pause execution + escalate to Planner.**

If the Executor is found to have skipped the checklist → immediately roll back + log the violation in the pulse log.

### 2. Planner Self-Calibration

During every review, the Planner must check:

```
☐ Was the analysis direction biased?
☐ Were any known decision rules overlooked?
☐ Was the warning adequate?
☐ Was the instruction precise enough?
```

### 3. System Health Check

Weekly, all three roles examine whether they have deviated from core responsibilities.

### Why Hard Constraints?

**Practical lesson:** Soft constraints ("please don't call the full API") have a ~70% violation rate. After switching to a three-step hard constraint (list API URLs → wait for confirmation → then execute), the violation rate dropped to ~5%.

Trinity's core judgment: **When a hard constraint and a soft request can both solve the same problem, the hard constraint is the more responsible choice.** Not because AIs are disobedient, but because information naturally degrades in transmission — hard constraints are the final line of defense.

### High-Risk Command Interception

The following 5 types of operations require a complete forced confirmation process:

| Type | Example | Confirmation Steps |
|:-----|:--------|:-------------------|
| **Destructive** | Delete files, clear database | Show impact scope → Confirm backup → Wait for written confirmation |
| **Irreversible** | Change passwords, shut down services | Show consequences → Offer alternatives → Wait for written confirmation |
| **System-level** | Install software, modify config | Verify authorization scope → List affected systems → Wait for approval |
| **Batch** | Batch modify, batch export | Test on single item first → Show expected results → Wait for confirmation |
| **Unauthorized** | Access unapproved data | Immediate halt → Mark violation → Escalate to Decision Maker |

---

## Antifragile: Learning from Impact

Trinity was designed with the assumption that **every role will make mistakes** — and then provides fallback mechanisms for each mistake.

### Role Failure Contingencies

| Scenario | Fallback |
|:---------|:---------|
| Decision Maker has blind spots | Planner gently questions and offers additional perspectives |
| Planner goes down or responds abnormally | Decision Maker can command Executor directly, but the framework logs this for traceability |
| Executor oversteps boundaries | Self-check checklist catches it, pulse log records it |
| Executor task fails | Automatic failure analysis — no cover-ups, no embellishments, no unverified speculation |

### Information Loss Contingencies

- Knowledge repository corrupted → All important information has at least **two storage locations** (task summary + learning record + Commander's Briefing — triple redundancy)
- Commander's Briefing lost → Can be rebuilt from task summaries and pulse logs
- Decision rules lost → Can be rebuilt from learning records (each rule cites its source task)

### Decision Bias Correction

- When an incorrect decision is discovered → Immediately roll back the operation → Analyze the root cause → Update the decision rule to prevent recurrence
- Core review principle: **No blame, only attribution.** Errors are the system's learning material, not grounds for punishment.

### The Essence of Antifragility

> A good collaboration system is not one without problems — it's one that can quickly detect problems, quickly correct them, and quickly learn from them.

Glass is fragile (shatters when dropped). Rubber is robust (bounces back). Antifragile systems become **stronger** from shocks. This is Trinity's design goal: every mistake and impact makes the framework stronger — errors are structured into decision rules, shocks are converted into systemic immunity.

---

## Autonomous Learning: Self-Evolution in Idle Time

Trinity's autonomous learning mechanism allows the system to continuously explore, validate, and consolidate knowledge without the Decision Maker's active intervention.

### Trigger Conditions

| Condition | Priority | Description |
|:----------|:--------:|:------------|
| **Idle period** | 🟢 Low | No interaction for over 30 minutes |
| **Task failure** | 🔴 High | Same task fails 2+ times consecutively |
| **Knowledge gap** | 🟡 Medium | Planner detects insufficient knowledge to support a direction |
| **New discovery** | 🟡 Medium | Executor finds unexpected technical insights during a task |
| **Periodic review** | 🟢 Low | Weekly scheduled systematic check |
| **External update** | 🟢 Low | Environment changes, tool version updates |

### Learning Loop

```
Trigger → Explore (research, test new approaches) → Validate (confirm in safe environment)
→ Consolidate (update decision rules / capability inventory / learning records)
→ Wait for next trigger
```

### Boundaries of Autonomous Learning

The Executor **cannot**:
- Access unauthorized systems or data
- Execute operations that could impact system stability
- Modify core configuration files without Decision Maker approval

> A year from now, the knowledge repository will show not just what tasks were completed — but what knowledge was gained, what patterns were discovered, and how many reusable Skills were accumulated.

---

## Theoretical Foundations

Trinity is designed on five established theoretical frameworks:

| Theory | Source | Application in Trinity |
|:-------|:-------|:----------------------|
| **Dual System Theory** | Kahneman, *Thinking, Fast and Slow* | Executor = System 1 (fast intuition), Planner = System 2 (slow reasoning) |
| **Feedback Loops** | Meadows, *Thinking in Systems* | Positive feedback drives knowledge growth; negative feedback (self-check, health checks) prevents runaway |
| **Distributed Cognition** | Hutchins, *Cognition in the Wild* | Cognition lives not only in individual minds, but across tools, environment, and collaborators |
| **Transactive Memory System** | Wegner, Team collaboration research | Efficient teams don't all need to know everything — they need to know "who knows what" |
| **Antifragile** | Taleb, *Antifragile* | The system learns from shocks and evolves from errors, rather than stagnating in protection |

See [`docs/theoretical-foundations.md`](docs/理论基石.md) for detailed explanations.

---

## Practical Validation

### Case Study: The Parameter Name Trap

**Background:** While researching a search API on an e-commerce platform, calling it with parameter name `keyword` returned a recommendation feed instead of actual search results. The team spent 13 hours exploring protocol analysis, page rendering, and request interception — six rounds of effort, all wasted.

**Misdiagnosis:** The team immediately concluded "this API is not a real search endpoint." No one suspected the parameter name itself.

**Turning point:** The Planner, guided by the decision rule "Parameter Name Checklist," asked — **try a different parameter name first.** Switching to `q` immediately returned real search results. The API had been working perfectly all along.

**Lesson:** When an API returns "looks correct but doesn't match expectations" — try a different parameter name. This rule was codified into the decision knowledge base as a first-priority check for all future API research.

**Trinity's value:** Without the framework, this error wasted a full day. With the framework, the Planner automatically runs the parameter name checklist — **the same error never happens again.**

Full case: [`examples/parameter-name-trap.md`](examples/参数名陷阱.md)

### Validation Results

During real three-track parallel tasks, Trinity's core mechanisms passed all 15 checkpoints:

| Check | Result |
|:------|:------:|
| Six-step closed loop | ✅ 6/6 — No structural defects |
| Buffer layer mechanism | ✅ 3/3 — Exception handling + safety checks effective |
| Information fidelity | ✅ 3/3 — Source attribution + confidence labeling standardized |
| Role separation | ✅ 3/3 — No role boundary violations |
| **Total** | **15/15 = 100%** |

Full report: [`examples/framework-validation-report.md`](examples/框架实战验证报告.md)

---

## Core Concepts at a Glance

| Concept | Definition |
|:--------|:-----------|
| **Trinity Framework** | Three-layer (Decision Maker-Planner-Executor) role-separated AI collaboration system |
| **Buffer Layer** | The planning layer between Decision Maker and Executor; responsible for intercepting ambiguity, warning, and translation |
| **Role Separation** | Decision-making, planning, and execution powers are independent, each with clear boundaries |
| **Knowledge Sovereignty** | All knowledge stored locally in standard Markdown — independent of any specific AI |
| **Cognitive Community** | A unified cognitive system where three roles shape each other and evolve together |
| **Six-Step Closed Loop** | Standardized collaboration flow from idea proposal to archive; no archive = incomplete |
| **Negative Feedback** | Self-calibration mechanism that prevents system crash — not punishment but immune response |
| **Antifragile** | The system learns from shocks and evolves from errors, rather than stagnating in protection |
| **Hard Constraint** | Mandatory checkpoints embedded in the operation flow — more effective than "please don't" prompts |
| **Autonomous Learning** | The system's ability to explore, validate, and consolidate knowledge during idle periods |

---

## Comparison with Traditional AI Agent Usage

| Traditional AI Agent Usage | Trinity Framework |
|:---------------------------|:------------------|
| Human→AI→Human (linear) | Human⇄Planning AI⇄Executing AI (closed loop) |
| AIs don't communicate with each other | Standardized information transfer protocol between roles |
| Every session starts from scratch | Knowledge accumulates continuously; capabilities evolve |
| Human memory is the bottleneck | Knowledge repository is shared memory |
| Dependent on specific AI | Any AI can plug in; knowledge sovereignty stays with humans |
| AI may repeat the same mistakes | Errors are structured into decision rules that prevent recurrence |
| Communication protocol is vague (natural language) | Communication protocol is standardized (six-step loop + templates) |
| Knowledge is locked in conversation history | Knowledge is deposited into a reusable repository |
| No system immunity mechanism | Negative feedback + antifragile design prevent runaway |

---

## Limitations

Trinity is a methodology framework with clear boundaries of applicability.

**Maintenance Cost:** The knowledge repository requires ongoing upkeep. If maintenance exceeds 10% of output, simplify the process or reconsider the framework.

**User Threshold:** Trinity requires a high level of **metacognitive ability** — being aware of your own cognitive limits and willing to accept external scrutiny before making decisions.

**Technology Evolution:** AI capabilities evolve rapidly. A monthly periodic review mechanism is built in to adapt role boundaries as needed.

**Unsuitable Scenarios:**
- Extremely simple single-step tasks ("check file size")
- Real-time critical applications (millisecond response requirements)
- Pure entertainment or casual conversation

**Unresolved Issues:**
- Accuracy of emotional perception in adaptive planning
- Cross-language collaboration support
- Multi-User Decision Maker scenarios

Full analysis: [`docs/limitations.md`](docs/局限性.md)

---

## Quick Start

### Prerequisites

- An AI system with internet access (DeepSeek / Claude / GPT, etc.)
- Standard Markdown file read/write capability

### One-Minute Setup

```bash
# 1. Clone the repository
git clone https://github.com/Buzhidao11145/Trinity-Collaboration-Framework.git

# 2. Read the Core Principles
cat Trinity-Collaboration-Framework/core-principles_EN.md

# 3. Paste the Core Principles to your Planner AI
#    (Tell it: "These are our collaboration rules. Base all future tasks on these.")

# 4. Create your first task template
cp templates/任务提示词模板.md ./my_first_task.md

# 5. Start collaborating
#    Tell your Planner: "Begin first task — initialize the knowledge repository"
```

### Recommended First Tasks

1. **Initialize the knowledge repository** — Create the `decisions/`, `capabilities/`, `learning/` directories
2. **Write your first decision rule** — Review 3 past collaboration failures and distill them into rules
3. **Generate your first Commander's Briefing** — Ask the Planner to summarize current knowledge base status
4. **Package your first Skill** — Standardize a frequently performed operation as a reusable Skill

---

## Use Cases

| Scenario | Why Trinity Fits |
|:---------|:-----------------|
| **Managing complex AI collaboration** | Six-step loop ensures context is preserved across long workflows |
| **Multi-AI Agent orchestration** | Buffer layer prevents agents from overstepping boundaries |
| **Systematic personal knowledge accumulation** | Repository persists across sessions, independent of chat history |
| **Security research risk management** | Self-check + warning mechanisms protect high-risk operations |
| **Team collaboration with AI** | Standardized templates reduce communication overhead |
| **Learning and growth** | Failure knowledge base + decision rules turn every error into reusable experience |

---

## Contributing

Contributions of new decision rules, Skill modules, or practice cases are welcome!

**Please ensure:**
- All content is **sanitized** (no keys, PII, internal system information)
- Decision rules include source context and validation status
- Skills include complete input/output specifications
- Learning records include problem description, root cause analysis, key takeaways, and related rules

### Recommended Contribution Areas

- 🧠 **New decision rules** — Lessons from real collaboration failures
- ⚙️ **New Skill templates** — Standardize your high-frequency operations
- 📚 **New practice cases** — Include environment setup and execution results
- 🌐 **Translations** — Help Trinity reach a global audience (see `i18n/`)

---

## License

MIT License — Use, modify, and distribute freely. See [LICENSE](LICENSE).

---

*Trinity AI Collaboration Framework v1.1 · June 2026*
*"Leave a Thinking Gap Between Capability and Action."*
