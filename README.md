# AI Safety in HR

**A governance framework for responsible AI deployment across the employment lifecycle.**

Binary safety ledgers. Vendor scorecards. Chain-of-custody tools. Position descriptions for the HR roles AI makes necessary.

*Part of the [Richard Porter AI Safety ecosystem](https://github.com/richard-porter)*

-----

## The Central Argument

> AI in HR is not a productivity problem. It is a chain-of-custody problem. Every output that influences a personnel decision must be attributable to a specific AI version, authorized by a specific human, reviewable by the employee it concerns, and defensible in a legal proceeding.

AI tools are now making — or materially influencing — hiring decisions, performance evaluations, compensation recommendations, termination actions, benefits determinations, and workforce reductions. When these systems fail in employment contexts, the consequences are not product defects. They are wrongful exclusion claims, EEOC complaints, disparate impact findings, and ADA violations.

The organization cannot point to the AI vendor. The organization is liable.

-----

## The Wrongful Termination Test

The single most useful heuristic in this framework, applicable to any AI tool in any HR context:

> *If this AI output were entered as evidence in a wrongful termination proceeding, could you defend every step of the process that produced it? Which model version? Which human reviewed it? When? Was the employee informed? Is the documentation complete?*
> 
> *If the answer to any of these is “the AI handled it” — the organization is exposed.*

-----

## Navigate by Audience

|If you are…                                                                          |Start here                                                                                                            |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
|**An AI developer or product team** building tools for HR workflows                  |[`for-developers/developer-briefing.md`](ai-safety-in-hr/for-developers/developer-briefing.md)                        |
|**An HR practitioner or procurement lead** evaluating or deploying AI                |[`for-hr-practitioners/`](ai-safety-in-hr/for-hr-practitioners/)                                                      |
|**An early-career HR professional** entering the field                               |[`for-early-career/hr-ai-framework-early-career.md`](ai-safety-in-hr/for-early-career/hr-ai-framework-early-career.md)|
|**A nonprofit HR leader or small HR shop** without a dedicated AI governance function|[`for-nonprofit-hr/nonprofit-hr-ai-toolkit.md`](ai-safety-in-hr/for-nonprofit-hr/nonprofit-hr-ai-toolkit.md)          |
|**A workforce educator** building AI literacy programs                               |[`for-workforce-education/`](ai-safety-in-hr/for-workforce-education/)                                                |
|**Evaluating a specific AI vendor** against safety criteria                          |[`safety-ledgers/`](safety-ledgers/)                                                                                  |
|**An HR leader** thinking about the future of the function                           |[`future-roles/`](future-roles/)                                                                                      |

-----

## Repository Structure

```
hr-ai-safety/
│
├── README.md                              ← You are here
├── RELATED-WORK.md                        Ecosystem lineage and connected repositories
│
├── ai-safety-in-hr/
│   ├── HRBP-master-framework.md           The full framework — all four quadrants,
│   │                                      Wrongful Termination Test, technical mapping
│   │
│   ├── for-developers/
│   │   └── developer-briefing.md          Quadrant risk profiles, hard stops,
│   │                                      chain-of-custody requirements
│   │
│   ├── for-hr-practitioners/
│   │   ├── ai-vendor-scorecard.md         Procurement evaluation by quadrant
│   │   └── ai-deployment-checklist.md     Go-live governance checklist
│   │
│   ├── for-early-career/
│   │   └── hr-ai-framework-early-career.md  Quadrant model as risk map,
│   │                                         differentiating questions, portfolio path
│   │
│   ├── for-nonprofit-hr/
│   │   └── nonprofit-hr-ai-toolkit.md     Nonprofit-specific risk, Mr. Wolff
│   │                                      integration, minimum viable governance
│   │
│   └── for-workforce-education/
│       ├── workforce-training-module.md   5-module 90-minute training program
│       └── employee-rights-ai-decisions.md  Plain-language employee rights
│
├── safety-ledgers/
│   ├── README.md                          Ledger methodology and series status
│   ├── recruitment-hiring-safety-ledger.md   11 sections, talent acquisition
│   └── crisis-intervention-safety-ledger.md  9 sections, Employee Champion quadrant
│
├── future-roles/
│   ├── README.md                          The residual human layer explained
│   ├── evolution-residual-human-layer.md  Full 3-phase transformation narrative
│   ├── jd-cognitive-sovereignty-architect.md
│   ├── jd-chain-of-custody-lead.md
│   ├── jd-dispute-resolution-labor-relations.md
│   ├── jd-decision-audit-analyst.md
│   ├── jd-workforce-education-wellness-lead.md
│   ├── jd-pay-equity-compensation-integrity.md
│   └── jd-benefits-fiduciary-plan-integrity.md
│
└── publications/
    └── ai-isnt-replacing-hr-its-inventing-it.md   Medium article
```

-----

## The Safety Ledger Series

The ledgers in this repository apply a binary evaluation methodology: either the architectural safeguard exists or it does not. No partial credit. No roadmap exceptions. No “the vendor is working on it.”

Each ledger is warranted by five criteria:

- **Asymmetric expertise** — users cannot evaluate what they cannot see
- **High specific consequence** — the harm class is significant and often irreversible
- **Domain-specific failure modes** — patterns unique to the context
- **Regulatory analogue** — existing legal framework
- **Canonical sources** — authoritative reference standards

|Ledger                                             |Status       |Quadrant                                 |
|---------------------------------------------------|-------------|-----------------------------------------|
|Recruitment and Hiring Mode Safety Ledger          |✅ v1.0       |Administrative Expert + Strategic Partner|
|Crisis Intervention Mode Safety Ledger             |✅ v1.0       |Employee Champion                        |
|Performance Management Mode Safety Ledger          |🔜 Forthcoming|Strategic Partner + Employee Champion    |
|Separation and Offboarding Mode Safety Ledger      |🔜 Forthcoming|All quadrants                            |
|Employee Relations Investigation Mode Safety Ledger|🔜 Forthcoming|Employee Champion                        |

-----

## The Residual Human Layer

The framework’s thesis on the future of HR roles:

> *AI takes the volume, compresses the expertise, and leaves behind the accountability. The residual human layer in HR is the layer that accepts the consequence.*

These are not the roles that survived AI. They are the roles AI made necessary.

|Role                                        |What It Owns                                                   |Why It Cannot Be Automated                                   |
|--------------------------------------------|---------------------------------------------------------------|-------------------------------------------------------------|
|Cognitive Sovereignty Architect             |Design layer — preserves human agency before systems ship      |An AI cannot reliably identify what AI erases                |
|AI Governance & Chain of Custody Lead       |Enforcement layer — defends every AI-assisted decision         |Accountability requires a person who can accept a subpoena   |
|AI Dispute Resolution & Labor Relations Lead|Dispute layer — human process for AI-affected decisions        |A dispute proceeding is a form of recognition, not a task    |
|AI Decision Audit Analyst                   |Forensic layer — reconstructs what the AI actually did         |Automating the audit of AI with AI is a conflict of interest |
|AI Workforce Education & Wellness Lead      |Education layer — honest account of what AI does to people     |An AI cannot tell a workforce what AI tools are doing to them|
|Pay Equity & Compensation Integrity Lead    |Methodology layer — designs what the auditor signs             |Legal accountability for the framework requires a human      |
|Benefits Fiduciary & Plan Integrity Lead    |Fiduciary layer — ERISA oversight of AI-assisted administration|Fiduciary duty cannot be delegated to a model                |

-----

## Documented Cases

This framework is grounded in documented failures, not theoretical risk:

- **EEOC v. iTutorGroup (2023)** — $365,000 settlement. AI hiring software automatically rejecting women 55+ and men 60+. EEOC: *“Even when technology automates the discrimination, the employer is still responsible.”*
- **Mobley v. Workday (2023–ongoing)** — Nationwide collective action certified May 2025 (N.D. Cal. 23-cv-00770-RFL). Potentially millions of applicants 40+ alleging age discrimination through AI screening. Court: AI-assisted rejection is legally equivalent to human-made rejection.
- **D.K. v. Intuit / HireVue (March 2025)** — ACLU complaint to Colorado CRD and EEOC. Deaf and Indigenous employee denied ADA accommodation for AI video interview. Rejected for promotion. AI feedback: *“practice active listening.”*
- **Amazon Hiring Algorithm (2018)** — Internal tool discontinued after discovery of systematic downgrading of resumes from women’s colleges.

-----

## Relationship to the Broader Ecosystem

|Repository                                                                                      |What It Does                            |Relationship to This Repo                                                         |
|------------------------------------------------------------------------------------------------|----------------------------------------|----------------------------------------------------------------------------------|
|[`frozen-kernel`](https://github.com/richard-porter/frozen-kernel)                              |Session-level AI governance architecture|Theoretical foundation — the Carver/IGL governance model underlying this framework|
|[`trust-chain-protocol`](https://github.com/richard-porter/trust-chain-protocol)                |Multi-agent chain of custody            |The technical architecture the Chain of Custody Lead role enforces                |
|[`adult-mode-safety-ledger`](https://github.com/richard-porter/adult-mode-safety-ledger)        |High-gain AI domain safety criteria     |HR qualifies on all three high-gain criteria                                      |
|[`ai-collaboration-field-guide`](https://github.com/richard-porter/ai-collaboration-field-guide)|Parent collection                       |This repository is a domain-specific extension                                    |
|[`sovereign-thinking-tools`](https://github.com/richard-porter/sovereign-thinking-tools)        |Cognitive tools                         |The Mr. Wolff Governance Rescue Kit (nonprofit HR) lives here                     |

-----

## What This Repository Does Not Constitute

- Legal advice. An employment attorney should review any AI deployment in HR contexts before launch.
- Clinical guidance. The Crisis Intervention Ledger addresses architectural requirements; clinical crisis intervention requires qualified professionals.
- Vendor endorsement or condemnation. Ledger evaluations are independently replicable and community-contributed.

-----

## Contributing

Vendor evaluations against the safety ledgers are explicitly invited. Independent replication of any evaluation is encouraged. Corrections welcome — with documentation.

The goal is not to block AI in HR. The goal is a defensible record that the human who signed off on the deployment can stand behind.

-----

## Author

Richard Porter (pen name) · SPHR · Master’s in HR, Loyola University · Six Sigma Green Belt · 25+ years enterprise HR including Rolls-Royce North America and Navient · Four nonprofit boards

*Sovereign humans. Always.*

-----

**Topics:** `ai-safety` `hr-tech` `employment-law` `ai-governance` `eeoc` `responsible-ai` `hr-compliance` `disparate-impact` `chain-of-custody` `workforce-ai` `talent-acquisition` `hrbp` `ulrich-model` `ai-discrimination`
