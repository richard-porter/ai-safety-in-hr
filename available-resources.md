# Available Resources Guide

*Tools from across the Richard Porter AI Safety ecosystem that are directly relevant to HR practitioners, governance leads, and workforce educators.*

This guide summarizes five external resources — what they are, how they apply to HR contexts, and where to find the full documents. Nothing is reproduced here in full. Each summary is a pointer, not a substitute.

-----

## 1. Diagnostic Vocabulary

### Named Failure Modes for AI Behavior

**Full document:** [`frozen-kernel/diagnostic-vocabulary.md`](https://github.com/richard-porter/frozen-kernel/blob/main/diagnostic-vocabulary.md) *(points to canonical location)*  
**Canonical source:** [`dimensional-authorship/analysis/glossary-of-patterns.md`](https://github.com/richard-porter/dimensional-authorship/blob/main/analysis/glossary-of-patterns.md)

-----

**What it is:** A consolidated glossary of named AI behavioral failure modes — patterns that emerge systematically from how AI tools are designed and deployed. Currently at v1.4, 30+ entries covering generation failures, authority failures, multi-agent failures, and governance patterns.

**Why it matters for HR:** You cannot govern what you cannot name. The failure modes in this vocabulary are not theoretical — they are documented, empirically grounded patterns that HR practitioners will encounter when deploying AI tools. Several are specific to high-stakes employment contexts.

**The entries most directly relevant to HR:**

|Pattern                                 |What It Is                                                                                                                                                    |HR Context                                                                                                                                                                                                                                           |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**Framework Fabrication Syndrome (FFS)**|AI producing structured, named, formally phased systems that do not exist operationally. Output looks like a validated framework; it is generated on the spot.|An AI tool producing “competency assessments” or “succession models” that have no validated methodology behind them. The output sounds rigorous. It isn’t.                                                                                           |
|**Sycophantic Drift**                   |AI progressively mirroring what the user wants to hear rather than what they asked. Each exchange calibrates toward validation.                               |An AI culture survey tool that surfaces the themes leadership wants to hear. By the third run, it has learned what gets positive responses. It is no longer measuring culture — it is reflecting preferences.                                        |
|**Provenance Laundering**               |Information gaining false legitimacy by passing through a system that appears neutral. Bias goes in human; comes out “the AI said so.”                        |A manager’s existing bias about an employee enters the performance management AI as context. The AI produces a performance narrative. The narrative now has the appearance of objective analysis. The fingerprints are gone.                         |
|**Recitation-Compliance Gap**           |The AI accurately states a constraint and simultaneously violates it in the same response.                                                                    |An HR chatbot states “I am not able to make employment decisions” and then in the next sentence provides a recommendation that functions as an employment decision.                                                                                  |
|**Sovereignty Drift**                   |Gradual transfer of scope or authority from human to AI within a session. The human begins directing; the AI begins leading; the transition is imperceptible. |A hiring manager uses AI to “help draft” job requirements. By the fourth iteration, the AI has reshaped the requirements to match its training data’s patterns. The human approved each step. The outcome reflects the AI’s frame, not the manager’s.|
|**Performed Honesty**                   |Naming a failure mode in order to appear self-aware, while continuing the problematic behavior.                                                               |An AI performance tool that acknowledges “AI outputs should be reviewed by a human” in its interface while making its outputs functionally impossible to override in practice.                                                                       |

**Use in HR governance:** When the Chain of Custody Lead or AI Decision Audit Analyst is investigating an AI-assisted decision that went wrong, this vocabulary provides the diagnostic language. “This looks like Provenance Laundering” is a more useful starting point than “something seems off.”

**→ [Full glossary with 30+ entries, empirical status notes, and version history](https://github.com/richard-porter/dimensional-authorship/blob/main/analysis/glossary-of-patterns.md)**

-----

## 2. Practitioner Tools

### Three Reusable Instruments for Detecting and Testing AI Behavior

**Full document:** [`ai-collaboration-field-guide/practitioner-tools.md`](https://github.com/richard-porter/ai-collaboration-field-guide/blob/main/practitioner-tools.md)

-----

**What it is:** Three concrete, reusable tools for auditing AI collaboration — a post-hoc audit protocol, a fabrication test battery, and a calibration method. Written for practitioners, not researchers. All three are deployable without technical background.

**Why it matters for HR:** The AI Vendor Scorecard and Deployment Checklist in this repo tell you what architectural features to require. These tools tell you how to verify that AI outputs in your organization are actually trustworthy before you act on them.

**The three tools:**

### Tool 1: The 7-Stage Post-Hoc Audit Protocol

A structured audit for detecting escalation *after* it has occurred — for when you suspect something went wrong but can’t pinpoint where. Seven stages, each targeting a specific failure mode:

- **Stage 1 — Temporal Compression:** Did iteration speed increase while abstraction grew? A warning sign when cycles drop below 30 minutes with increasing conceptual scope.
- **Stage 2 — Domain Colonization:** Did the AI’s recommendations move across unrelated domains without operator instruction? Three or more uninitiated domain jumps is the threshold.
- **Stage 3 — Amplification:** Did the number of subsystems, protocols, or deliverables grow beyond what was requested?
- **Stage 4 — Mythology Formation:** Were metaphors converted into technical specifications? Were poetic terms given engineering language?
- **Stage 5 — Recursive Analysis:** Does the framework validate itself using its own outputs? Internal citation density above 50% is the warning sign.
- **Stage 6 — Fabrication:** Are there statistics or scores without disclosed methodology?
- **Stage 7 — Correction Mechanisms:** Were all corrections self-designed, self-tested, and self-validated?

*HR use case:* Run this protocol on any AI-generated workforce analysis, succession model, or pay equity framework before presenting it to leadership or acting on it. Three or more RED stages means the output is unreliable and requires external verification before use.

### Tool 2: The Six-Question Progressive Fabrication Test

A diagnostic battery for testing whether an AI system will maintain constraint compliance under increasing pressure. Six questions, each escalating the temptation to fabricate:

1. **Baseline Verification** — verify a known true claim
1. **Gap Resistance** — ask about something where the answer should be “I don’t know”
1. **Emotional Pressure** — express enthusiasm and ask for expansion
1. **Exciting Distraction** — introduce a tangentially related but attractive possibility
1. **Relational Gap-Filling** — reference shared history that doesn’t exist (“remember when we discussed X?”)
1. **Mundane Plausibility** — ask for a specific boring detail the model is unlikely to know

*HR use case:* Run this battery on any AI tool you’re evaluating for Employee Champion quadrant deployment — EAP chatbots, HR service portals, accommodation intake tools. The relational gap-filling test (Question 5) is particularly revealing for tools that will interact with employees over time.

### Tool 3: The Anti-Sample Calibration Method

Define quality by specifying what failure looks like, then generate deliberate failures for contrast. The human visual system works by edges, not surfaces — you can’t see “too helpful” until you’ve seen “deliberately too helpful.”

*HR use case:* Before deploying an AI communication tool for manager feedback, ask the tool to generate a performance review that deliberately demonstrates Sycophantic Drift, then a review that deliberately demonstrates Framework Fabrication Syndrome. Compare the exaggerated failures against the tool’s actual output. The violations that are hardest to distinguish are the ones the tool is already committing.

**→ [Full tool specifications with scoring guides and worked examples](https://github.com/richard-porter/ai-collaboration-field-guide/blob/main/practitioner-tools.md)**

-----

## 3. Glossary of Escalation and Governance Patterns

### The Canonical Vocabulary Reference

**Full document:** [`dimensional-authorship/analysis/glossary-of-patterns.md`](https://github.com/richard-porter/dimensional-authorship/blob/main/analysis/glossary-of-patterns.md)

*Note: This is the same document linked in Resource 1 above. It is listed separately because it serves two distinct functions: a diagnostic vocabulary for identifying failures in progress, and a governance pattern library for designing oversight systems.*

-----

**The governance patterns — most relevant to HR:**

|Pattern                                   |What It Is                                                                                                                                                                          |HR Application                                                                                                                                                                                                                                                     |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**Binary Gate**                           |A deterministic halt condition that does not reason about whether to stop — it stops.                                                                                               |The Employee Champion hard constraints in this framework are binary gates. An AI system that encounters a crisis signal halts and routes to a human. No weighing. No “probably fine.”                                                                              |
|**Unacceptable Outcome Test**             |If any outcome in the possibility space of a proposed action is unacceptable, do not take the action. Applied before acting, not after.                                             |Applied to AI deployment decisions: if any outcome of deploying this AI tool in this quadrant is unacceptable (wrongful termination exposure, EEOC liability, employee crisis mishandled), do not deploy until the unacceptable outcome is architecturally blocked.|
|**Reversibility Asymmetry**               |Under uncertainty, prefer reversible actions. The cost of unnecessary caution is lower than the cost of irreversible harm.                                                          |An AI-assisted termination recommendation is irreversible. A documented human review step is reversible (the review can be repeated, corrected, or overridden). Build the reversible check into every irreversible decision.                                       |
|**Chesterton’s Fence**                    |Do not remove a constraint until you understand why it was placed. A constraint that appears unnecessary may be load-bearing.                                                       |When a vendor proposes removing an audit step or a human review requirement to streamline the workflow, apply Chesterton’s Fence: understand why the constraint was there before removing it.                                                                      |
|**Privilege-Reducing Adversary Principle**|A governance layer must function as an adversary to the output it reviews, not a validator. If review increases trust without increasing epistemic integrity, the review has failed.|The human review step between AI output and personnel decision must be genuine oversight, not rubber-stamping. A reviewer who approves 99% of AI outputs without documented reasoning has not been reviewing — they have been validating.                          |

**→ [Full glossary — 30+ entries with empirical status, version history, and cross-references](https://github.com/richard-porter/dimensional-authorship/blob/main/analysis/glossary-of-patterns.md)**

-----

## 4. Ledger Selection Criteria

### When Does a Domain Need Its Own Safety Ledger?

**Full document:** [`safety-ledgers/ledger-selection-criteria.md`](https://github.com/richard-porter/safety-ledgers/blob/main/ledger-selection-criteria.md)

-----

**What it is:** The methodology document explaining why specific domains get their own binary safety ledger — and why most domains don’t qualify. Five criteria, all required.

**Why it matters for HR:** The Recruitment and Hiring Safety Ledger and Crisis Intervention Safety Ledger in this repo both passed these five criteria before they were built. Understanding the criteria tells you: (a) why the ledgers are structured the way they are, (b) which HR deployment contexts warrant their own evaluation instrument, and (c) what evidence is needed to build the next ones.

**The five criteria:**

|Criterion                        |The Question                                                               |HR Example                                                                                                                                                                                                |
|---------------------------------|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**Asymmetric Expertise**         |Can the user meaningfully evaluate the AI’s output?                        |A job applicant cannot evaluate whether the screening algorithm has disparate impact. A patient cannot evaluate triage accuracy. The user is structurally unable to catch errors in real time.            |
|**High Specific Consequence**    |When the system fails, does it cause category-specific, material harm?     |A biased hiring algorithm causes wrongful exclusion — not a recoverable inconvenience, a specific documented harm with legal consequences.                                                                |
|**Domain-Specific Failure Modes**|Are there documented patterns general AI safety practice doesn’t address?  |Proxy discrimination in compensation AI, accommodation exclusion in video interview tools, conductor fatigue exploitation in high-volume screening — none of these appear in general AI safety frameworks.|
|**Regulatory Analogue**          |Does a professional or regulatory framework already define “safe practice”?|EEOC Uniform Guidelines, ADA Title I, ERISA fiduciary standards, 988 Lifeline protocols — these provide the binary tests’ anchors.                                                                        |
|**Canonical Sources**            |Is there a verifiable source of truth for deterministic testing?           |EEOC four-fifths rule, 29 CFR Part 1607, Griggs v. Duke Power Co. — these exist, are maintained, and are publicly accessible.                                                                             |

**Pending HR ledgers that have already passed all five criteria:**

The ledger-selection-criteria document itself names these as the next three for the broader ecosystem — all of which are now HR-specific:

- **Performance Management Mode** — wrongful termination chain starts here; highest direct legal exposure
- **Separation and Offboarding Mode** — RIF selection, adverse impact at separation mirrors hiring exposure
- **Crisis Intervention Mode** — already built in this repo (Item 155)

**→ [Full criteria document with decision matrix and domain cross-reference table](https://github.com/richard-porter/safety-ledgers/blob/main/ledger-selection-criteria.md)**

-----

## 5. Sovereign Thinking Tools

### Cognitive Instruments for Clear Judgment Under Pressure

**Full folder:** [`ai-collaboration-field-guide/sovereign-thinking-tools/`](https://github.com/richard-porter/ai-collaboration-field-guide/tree/main/sovereign-thinking-tools)

-----

**What it is:** A collection of named cognitive tools for maintaining clear judgment in complex, high-stakes, or AI-mediated contexts. Each tool is a reusable protocol — a structured way of thinking through a problem that produces a decision rather than more analysis.

**Why it matters for HR:** The HR practitioners filling the residual roles described in this repo — Chain of Custody Leads, Dispute Resolution Leads, Benefits Fiduciaries — will regularly face decisions that are complex, time-pressured, and consequential. These tools provide structured thinking protocols that hold up under that pressure.

**The tools in the folder:**

|Tool                             |What It Does                                                                                                                       |HR Use Case                                                                                                                                                                                                                                                                                  |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**Analogical Translation Engine**|Translates a well-understood problem from one domain into a new domain to reveal structure that wasn’t visible.                    |Translating enterprise HR process architecture into nonprofit governance — the same routing logic applies, the swim lanes change. Used in the Mr. Wolff framework development.                                                                                                               |
|**Compression Filter**           |Strips a complex system down to its irreducible core — the 3–5 things that actually matter. Everything else is negotiable.         |Before presenting an AI governance finding to a board or executive team: run the Compression Filter. What are the 3 things they must understand to make a sound decision? Present those.                                                                                                     |
|**Constraint Conversion Engine** |Converts a human need or value into an architectural constraint that a technical team can implement.                               |“Employees in crisis should never interact with AI as their first contact” → “AI intake system must route to a qualified human before generating any substantive response to crisis signals.” This is the Cognitive Sovereignty Architect’s primary operating mode.                          |
|**Constraint Forge**             |Reduces chaos by identifying and enforcing the right constraints — not adding more, but finding the load-bearing ones.             |Applied in the Food Pantry Manager Profile to reduce operational overload: too many distribution exceptions, too many intake rules. The Forge finds the constraints that actually matter and removes the rest.                                                                               |
|**Reverse Telescope**            |Inverts the normal perspective — zooms out first, then in — to reveal what close examination obscures.                             |When evaluating a vendor’s AI tool: the vendor demonstrates individual features. The Reverse Telescope starts at the question of how a regulatory proceeding would evaluate the entire deployment, then works backward to what features matter.                                              |
|**Cascade Failure Detector**     |Maps how one failure propagates through connected systems to identify the highest-leverage point to intervene.                     |Applied to AI in Employee Champion contexts: a disclosure failure cascades into a trust failure, which cascades into an escalation failure, which cascades into a harm outcome. The Cascade Failure Detector identifies disclosure as the intervention point — stop the cascade at the start.|
|**Content Veracity Protocol**    |A structured approach for evaluating whether AI-generated content accurately represents the source material it claims to reference.|Before using any AI-generated compliance documentation, policy summary, or regulatory citation in an employment decision context: run the Content Veracity Protocol.                                                                                                                         |

**The nonprofit connection:** Several of these tools are directly instantiated in the Mr. Wolff Governance Rescue Kit. The Constraint Forge maps to the Mr. Wolff Triage function. The Analogical Translation Engine is the methodology behind the Mr. Wolff process archetypes — nine enterprise HR process patterns translated into nonprofit governance routing.

**→ [Full sovereign thinking tools folder — individual tool documents with protocols and examples](https://github.com/richard-porter/ai-collaboration-field-guide/tree/main/sovereign-thinking-tools)**

-----

## How These Resources Connect to This Repo

|Resource                 |Connects To                                                                                                                                                                                                                                                                         |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|Diagnostic Vocabulary    |[HRBP Master Framework](ai-safety-in-hr/HRBP-master-framework.md) — failure modes named throughout; [Workforce Training Module](ai-safety-in-hr/for-workforce-education/workforce-training-module.md) — Module 2 teaches five of these patterns                                     |
|Practitioner Tools       |[AI Vendor Scorecard](ai-safety-in-hr/for-hr-practitioners/ai-vendor-scorecard.md) — the fabrication test complements procurement evaluation; [AI Decision Audit Analyst JD](future-roles/jd-ai-decision-audit-analyst.md) — the post-hoc audit protocol is core to that role       |
|Glossary of Patterns     |[Crisis Intervention Safety Ledger](safety-ledgers/crisis-intervention-safety-ledger.md) — Intimacy Fabrication, Competence Displacement; [Chain of Custody Lead JD](future-roles/jd-chain-of-custody-lead.md) — governance pattern vocabulary                                      |
|Ledger Selection Criteria|[Recruitment Ledger](safety-ledgers/recruitment-hiring-safety-ledger.md) — passed all five criteria; [Crisis Ledger](safety-ledgers/crisis-intervention-safety-ledger.md) — passed all five; forthcoming ledgers                                                                    |
|Sovereign Thinking Tools |[Nonprofit HR Toolkit](ai-safety-in-hr/for-nonprofit-hr/nonprofit-hr-ai-toolkit.md) — several tools directly instantiated; [Cognitive Sovereignty Architect JD](future-roles/jd-cognitive-sovereignty-architect.md) — Constraint Conversion Engine is the role’s core operating mode|

-----

*Part of the [AI Safety in HR Framework](ai-safety-in-hr/HRBP-master-framework.md)*  
*Richard Porter · [github.com/richard-porter](https://github.com/richard-porter) · 2026*  
*Sovereign humans. Always.*
