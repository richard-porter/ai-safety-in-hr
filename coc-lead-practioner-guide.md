# Chain of Custody Lead — Practitioner Guide

## AI Safety in HR · Future Roles Series · Practitioner Extension

*Operates under the Frozen Kernel. Never inside it.*

*Companion to: <jd-chain-of-custody-lead.md> · [HRBP-master-framework.md](../HRBP-master-framework.md)*

🧊

-----

## Profile Definition

**Role:** The named human accountable for the documentation, defensibility, and chain of custody of every AI-assisted HR decision in the organization.

**Primary Failure Mode:** Governance theater — documentation that exists but does not reflect genuine human review.

**Primary Risk:** The subpoena arrives and the record either doesn’t exist, or exists but cannot be defended because the “review” was a rubber stamp.

> **One-Line Profile Summary**
> The Chain of Custody Lead prioritizes defensible documentation, genuine human review, and evidentiary completeness over speed, convenience, or the appearance of oversight.

-----

## How This Profile Works

The JD describes the role. This guide tells you how to do it on Monday morning.

The Chain of Custody Lead operates in two modes:

**Operational mode** (daily/weekly): Monitoring AI tool use, reviewing outputs, maintaining documentation standards, catching gaps before they become liabilities.

**Adversarial mode** (when triggered): Producing complete, defensible records under legal, regulatory, or investigative pressure. This mode cannot be prepared for in the moment. Everything depends on what was done in operational mode.

*The goal of operational mode is to make adversarial mode boring.*

-----

## Inherited Tools

**From Core Sovereign Tools:**

**Scale Test** (Daily) — Most governance concerns are Pebbles that feel like Boulders under pressure. A single incomplete record is a Pebble. A pattern of incomplete records is a Boulder. Know which you’re dealing with before escalating.

**Capacity Gate** (When queue exceeds review capacity) — If the volume of AI-assisted decisions exceeds your genuine review capacity, the human review gate has failed. This is not a documentation problem — it is a structural problem requiring escalation, not acceleration.

**From HRBP Framework:**

**Wrongful Termination Test** (Per high-stakes decision) — If this AI output were entered as evidence in a wrongful termination proceeding, could you defend every step of the process that produced it? Apply before any AI-assisted output enters a personnel record.

**Quadrant Risk Check** (Per new AI tool deployment) — Which quadrant does this tool operate in? Employee Champion deployments require the highest documentation standard. No deployment proceeds without this check.

-----

## Quick Menu

*Select by what you’re experiencing, not by tool name.*

|What you’re experiencing                                                 |Use this tool                       |
|-------------------------------------------------------------------------|------------------------------------|
|“An AI tool was just deployed and I don’t know what documentation exists”|COC-1 Deployment Audit              |
|“I need to review an AI output before it enters a personnel record”      |COC-2 Output Review Gate            |
|“We got a subpoena / EEOC charge / DOL inquiry”                          |COC-3 Adversarial Response Protocol |
|“My reviewers are approving everything without reading it”               |COC-4 Rubber Stamp Detector         |
|“A vendor updated their model and didn’t tell us”                        |COC-5 Model Version Alert           |
|“We need to produce all AI-related records for an employee”              |COC-6 Employee Record Reconstruction|
|“I think this AI output is wrong but I’m not sure how to override it”    |COC-7 Human Override Protocol       |
|“Something about this deployment feels off but I can’t name it”          |COC-8 Governance Integrity Check    |

-----

## COC-1. Deployment Audit

*What AI tools are actually running in HR right now, and what documentation exists?*

**What it does:** Establishes the baseline. Before you can govern AI use, you need to know what is in use. Most organizations deploying AI in HR do not have a complete inventory. This is always the first tool.

**Protocol:**

**Inventory:** List every AI tool currently in use across all HR functions. Include: vendor name, tool name, version if known, deployment date if known, which HR function it supports.

**Quadrant map:** For each tool, assign the Ulrich quadrant(s) it operates in (Strategic Partner / Change Agent / Employee Champion / Administrative Expert).

**Documentation check:** For each tool, answer:

- Is there a deployment authorization document? (Y/N)
- Is there a record of what human review was designed into the workflow? (Y/N)
- Is the current model version documented? (Y/N)
- Is there a named human owner for governance of this tool? (Y/N)

**Gap log:** Any N is a gap. Log it with the tool name, the missing element, and a target resolution date.

**Priority:** Employee Champion quadrant gaps are blocking — resolve before the next time the tool runs. All other quadrant gaps are high priority — resolve within 30 days.

**Stop if:** The inventory is becoming a project rather than a scan. The goal is a working list, not a perfect database. Start with the tools most likely to touch a personnel decision.

-----

## COC-2. Output Review Gate

*Is this AI output defensible before it enters a personnel record?*

**What it does:** The operational checkpoint that makes chain of custody real rather than nominal. Every AI-assisted output that will influence a hiring decision, performance record, compensation recommendation, discipline action, or termination must pass through this gate before it is used.

**Protocol:**

**Identify:** What decision will this output influence? Name it specifically.

**Quadrant:** Which quadrant is this decision in? (Employee Champion decisions require the highest standard.)

**Source check:** Can you identify:

- Which AI tool produced this? (Y/N)
- Which version of that tool? (Y/N)
- What input data was used? (Y/N)
- When it was produced? (Y/N)

**Content check:**

- Does the output contain false precision — specific scores or rankings without uncertainty ranges? (Y/N — Y requires flagging)
- Does the output reference data that could be a proxy for protected class status? (Y/N — Y requires review)
- Is the output consistent with the human reviewer’s independent assessment? (Y/N — N requires documentation)

**Human review:** Document your review: your name, the date, your assessment, and whether you confirmed, modified, or overrode the AI output.

**Record:** File the output, your review documentation, and the decision taken. Retain per your jurisdiction’s requirements (minimum three years in most EEOC contexts).

**Stop if:** The volume of outputs exceeds your capacity for genuine review. This is not a documentation problem — trigger COC-4 (Rubber Stamp Detector) and escalate to leadership.

-----

## COC-3. Adversarial Response Protocol

*The subpoena arrived. The EEOC charge was filed. The DOL is asking.*

**What it does:** The structured response for when chain-of-custody records are demanded under legal or regulatory pressure. This protocol assumes you have been running COC-2 and COC-1. If you have not, the first step is an honest assessment of what you can actually produce.

**Protocol:**

**Scope:** What is being requested? Identify the specific decisions, time period, employees, and AI tools in scope.

**Litigation hold:** Stop normal records management immediately for anything in scope. Nothing is deleted, modified, or moved until the matter is resolved.

**Inventory what exists:** For each decision in scope, what documentation do you have?

- AI tool and version (Y/N)
- Input data used (Y/N)
- Output produced (Y/N)
- Human reviewer identity and date (Y/N)
- Decision taken and basis (Y/N)
- Employee notification (Y/N)

**Gap assessment:** For any N: can it be reconstructed from other sources (system logs, email, calendar)? If not, document the gap honestly. Do not attempt to reconstruct records that do not exist — that is obstruction.

**Legal coordination:** Brief employment counsel before producing anything. The attorney-client privilege on your gap assessment is important.

**Production timeline:** Confirm with counsel what can be produced, by when, and in what format.

**Stop if:** You are tempted to reconstruct records that do not exist or to characterize incomplete documentation as complete. Incomplete records are a problem. Falsified records are a crime.

-----

## COC-4. Rubber Stamp Detector

*Is “human review” actually happening, or is it a checkbox?*

**What it does:** The most dangerous failure mode in AI governance is not the absence of human review — it is human review that is nominal rather than real. A reviewer who approves 98% of AI outputs without documented reasoning is not reviewing. This tool detects the pattern.

**What it looks like:**

- Review queue sizes that make genuine individual review impossible
- Override rates that are statistically implausible (less than 2% in high-volume hiring tools is suspicious)
- Review timestamps that cluster (100 reviews in 45 minutes is not genuine review)
- Reviewers who cannot explain why they approved a specific output when asked
- Review steps that are UI checkboxes with no documentation field

**Protocol:**

**Volume check:** How many AI outputs is each reviewer approving per session? What is the realistic time for genuine review of one output? (Do the math — if it doesn’t fit, the review isn’t real.)

**Override rate:** What percentage of AI outputs are being modified or overridden by human reviewers? Pull this by reviewer. Zero overrides over a sustained period is a red flag, not a success metric.

**Timestamp analysis:** Are review timestamps clustered in patterns inconsistent with individual review? (Bulk approvals at end of day, all reviews within minutes of each other.)

**Sample audit:** Pull five recent reviews at random. Ask the reviewer to explain their assessment of each. If they cannot, the review was nominal.

**Escalation:** Rubber stamping is a structural failure, not a personnel failure. The fix is workflow redesign, queue management, or tool deployment reduction — not individual counseling.

**Stop if:** You’re using override rate as the primary metric. Some AI tools in low-risk quadrants may legitimately have low override rates. Context matters. The Employee Champion quadrant should have higher override rates than the Administrative Expert quadrant.

-----

## COC-5. Model Version Alert

*The AI vendor updated their model. What changed and what do we need to do?*

**What it does:** Vendor model updates are one of the highest-risk events in AI governance. A model that passed your adverse impact testing in January may behave differently in March. Most vendors do not proactively notify deploying organizations of model changes. This tool is the organizational response when you learn of a change.

**Protocol:**

**Detect:** How did you learn of the update? (Vendor notification, CHANGELOG, user report of different behavior, internal audit.) Document the source and date.

**Scope:** Which of your deployed tools are affected? Which HR decisions does each tool influence?

**Change assessment:** What changed in the model? (Request documentation from the vendor.) Specifically:

- Were training data, fine-tuning, or RLHF updated? (Y/N)
- Were safety filters or output constraints changed? (Y/N)
- Did the vendor conduct bias re-testing? Is documentation available? (Y/N)

**Adverse impact check:** For any Employee Champion or Strategic Partner quadrant tool: the model update triggers a new adverse impact assessment before continued use.

**Documentation update:** Update your deployment records to reflect the new model version and the date the update took effect.

**Contractual check:** Does your vendor contract require notification of model changes? If yes and they didn’t notify you, that is a contract issue. Flag for legal.

**Stop if:** Vendor documentation is so vague that you cannot assess what changed. In that case, treat it as a material change requiring re-evaluation of the deployment.

-----

## COC-6. Employee Record Reconstruction

*An employee (or their attorney) is asking for all AI-related records.*

**What it does:** When an employee requests their AI-related records — or when records are demanded in litigation — you need to be able to produce a complete account of every AI system that touched a decision about them. This tool structures that reconstruction.

**Protocol:**

**Scope:** Which decisions about this employee are in scope? (All? A specific time period? A specific decision type?)

**Tool inventory:** Which AI tools were in use during the relevant period that could have influenced any decision about this employee?

**For each tool:**

- Was this employee’s data processed by this tool? (Y/N — if unknown, that is itself a finding)
- What output was produced? Do you have the output? (Y/N)
- Who reviewed the output? Is that documented? (Y/N)
- What decision followed the output? Is the connection documented? (Y/N)

**Employee data:** Was this employee’s personal data used in model training? This requires vendor confirmation.

**Gap log:** Any N requires either reconstruction from other sources or honest documentation of the gap.

**Production:** Coordinate with legal before producing. Determine what is subject to privilege, what is producible, and what format is required.

**Stop if:** You cannot produce a complete record for a single employee. That finding tells you exactly what your governance gaps are. Document the gaps honestly — they will inform your remediation plan.

-----

## COC-7. Human Override Protocol

*The AI output feels wrong. How do I override it and document that I did?*

**What it does:** The human override is the most important function in AI governance. It is what makes chain of custody real rather than nominal. This tool structures the override decision and ensures it is documented in a way that is defensible.

**Protocol:**

**Name the concern:** What specifically is wrong with the AI output? Be concrete:

- The output contains factual errors about the employee (specify)
- The output reflects what appears to be bias or protected class proxy (specify)
- The output is inconsistent with evidence available to the human reviewer (specify)
- The output contains false precision that is not warranted (specify)

**Independent assessment:** Form your own judgment about the correct outcome, based on the evidence available to you, before modifying the output.

**Document the override:**

- Your name and title
- The date and time
- The AI output as originally produced (preserve this — do not overwrite)
- Your specific concern with the original output
- Your independent assessment
- The decision you made and why

**Escalation check:** Does this override indicate a systemic pattern — multiple similar overrides of the same tool? If yes, escalate to review the deployment, not just the individual case.

**Notification check:** Does the employee have any right to know that an AI output was involved in this decision and that it was overridden? Check your jurisdiction’s requirements and your organization’s disclosure commitments.

**Stop if:** You feel pressure not to override because it will “undermine” the AI tool’s adoption. The override is the governance system working. A human reviewer who feels unable to override is a rubber stamp. That is a structural failure requiring leadership escalation.

-----

## COC-8. Governance Integrity Check

*Something feels off about how we’re doing this. What is it?*

**What it does:** The diagnostic for when you have a sense that the AI governance system is failing in some way but cannot yet name the specific failure. Runs across the full governance architecture to identify where integrity has been compromised.

**Protocol:**

**Layer check — Design:**

- Is the Cognitive Sovereignty Architect (or equivalent function) involved in evaluating new AI tools before deployment? (Y/N)
- Is the quadrant risk assessment happening before deployment, not after? (Y/N)
- Are adverse impact assessments conducted before deployment for Strategic Partner and Employee Champion tools? (Y/N)

**Layer check — Operations:**

- Is COC-2 (Output Review Gate) running for every AI-assisted decision that influences a personnel record? (Y/N)
- Are override rates being tracked and reviewed? (Y/N)
- Is model version documentation current? (Y/N)

**Layer check — Culture:**

- Do reviewers understand that overriding AI output is expected and supported, not exceptional? (Y/N)
- Does leadership treat governance documentation as a protection, not a burden? (Y/N)
- Is there pressure — explicit or implicit — to approve AI outputs quickly? (Y/N — Y is a red flag)

**Layer check — Accountability:**

- Is there a named human owner for each AI tool in HR? (Y/N)
- Can you produce a complete chain-of-custody record for any AI-assisted decision in the past 90 days, on demand? (Y/N)
- Has employment counsel reviewed the governance architecture in the past 12 months? (Y/N)

**Flag:** Any N in the Operations or Accountability layer is an active gap. Any N in Design or Culture is a latent vulnerability. Document and escalate appropriately.

**Stop if:** Every answer is Y and you know that’s not honest. This tool requires you to be harder on your own governance than you would be in a normal review.

-----

## Tool Frequency Summary

|Tool                                |Frequency                         |Trigger                                                  |
|------------------------------------|----------------------------------|---------------------------------------------------------|
|COC-1 Deployment Audit              |Quarterly                         |Also: any new AI tool deployed                           |
|COC-2 Output Review Gate            |Per AI-assisted personnel decision|Non-negotiable in Employee Champion quadrant             |
|COC-3 Adversarial Response Protocol |When triggered                    |Legal hold, EEOC charge, DOL inquiry, litigation         |
|COC-4 Rubber Stamp Detector         |Quarterly                         |Also: when override rates seem implausibly low           |
|COC-5 Model Version Alert           |When triggered                    |Vendor update detected or reported                       |
|COC-6 Employee Record Reconstruction|When triggered                    |Employee request, litigation discovery, regulatory demand|
|COC-7 Human Override Protocol       |Per override                      |Every time a human reviewer modifies or rejects AI output|
|COC-8 Governance Integrity Check    |Quarterly                         |Also: when something feels off                           |
|Wrongful Termination Test           |Per high-stakes decision          |Every AI-assisted termination, discipline, or denial     |
|Quadrant Risk Check                 |Per new deployment                |Before any new AI tool goes live                         |
|Capacity Gate                       |When queue exceeds capacity       |When review volume exceeds genuine review capacity       |

-----

## What This Profile Explicitly Avoids

Rubber-stamp efficiency. Documentation for appearance rather than defensibility. Treating governance as a compliance checkbox. Allowing velocity pressure to override review standards. This profile is about building a record that can actually be defended — not one that looks like it can be.

-----

## Relationship to Other Practitioner Guides

|Related Document                                                                |Relationship                                                                                              |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
|<jd-chain-of-custody-lead.md>                                                   |The JD describes the role. This guide tells you how to do it.                                             |
|[HRBP-master-framework.md](../HRBP-master-framework.md)                         |Quadrant risk profiles underlying the governance standards in this guide                                  |
|[ai-vendor-scorecard.md](../for-hr-practitioners/ai-vendor-scorecard.md)        |Procurement tool — the Chain of Custody Lead is the primary user                                          |
|[ai-deployment-checklist.md](../for-hr-practitioners/ai-deployment-checklist.md)|Go-live governance — Chain of Custody Lead signs off                                                      |
|<jd-ai-decision-audit-analyst.md>                                               |The Audit Analyst supports COC-3 and COC-6 — this guide delegates the forensic reconstruction to that role|
|Food Pantry Manager Profile                                                     |Structural model this guide is built from — same derivation methodology                                   |

-----

## How to Use This Document

**This document is cold storage. It is not loaded into sessions.**

**For daily use:** Consult the Quick Menu. Deploy one tool. Use it. Shut it off. Return to work.

**For new deployments:** COC-1 first. Always.

**For legal events:** COC-3 immediately. Brief counsel before producing anything.

**For quarterly review:** COC-8. Be honest.

**For expansion:** New tools follow the same five principles as the Food Pantry Profile. All five or it doesn’t belong here.

-----

*The Frozen Kernel keeps you safe.*
*These tools help you think clearly inside the safe space.*

*Chain of Custody Lead Practitioner Guide · v1.0 · March 2026*
*AI Safety in HR Framework · Future Roles Series*
*Sovereign humans. Always.*
