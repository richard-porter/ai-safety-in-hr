# AI Decision Audit Analyst — Practitioner Guide

## AI Safety in HR · Future Roles Series · Practitioner Extension

*Operates under the Frozen Kernel. Never inside it.*

*Companion to: <jd-ai-decision-audit-analyst.md> · <coc-lead-practitioner-guide.md>*

🧊

-----

## Profile Definition

**Role:** The forensic reconstruction layer. When a dispute arises, a proceeding begins, or a regulator asks what happened, the AI Decision Audit Analyst does the work that makes a defensible answer possible: read the logs, trace the decision chain, identify what documentation exists and what doesn’t, translate all of it into plain language for non-technical reviewers.

**Primary Failure Mode:** Reconstruction theater — producing a record that looks complete but contains gaps the analyst didn’t name.

**Primary Risk:** A gap you didn’t document is a gap that looks like concealment. A gap you named is a gap that looks like honesty. Always name the gap.

> **One-Line Profile Summary**
> The AI Decision Audit Analyst prioritizes forensic accuracy, gap identification, and plain-language translation over speed, completeness, or making the record look better than it is.

-----

## How This Role Supports the Chain of Custody Lead

The Chain of Custody Lead owns the governance system and the accountability. The AI Decision Audit Analyst does the technical reconstruction work that makes that accountability possible. The relationship is specific:

|Chain of Custody Lead          |AI Decision Audit Analyst                   |
|-------------------------------|--------------------------------------------|
|Owns the governance obligation |Executes the forensic work                  |
|Signs off on the record        |Produces the record                         |
|Appears in legal proceedings   |Prepares the materials for those proceedings|
|Sets the documentation standard|Audits compliance with that standard        |
|Escalates systemic findings    |Identifies the patterns that need escalating|

The Analyst does not make governance decisions. The Analyst makes governance decisions possible by producing accurate, honest, plain-language records.

-----

## Inherited Tools

**From Core:**

**Scale Test** (Per request) — Not every gap in a record is a crisis. A single missing timestamp is a Pebble. A missing human reviewer identity on a termination decision is a Boulder. Calibrate before escalating.

**From Chain of Custody Lead Guide:**

**COC-2 Output Review Gate** — The Analyst supports this gate in volume situations: when the Chain of Custody Lead cannot individually review every AI output, the Analyst audits samples and reports patterns.

**COC-3 Adversarial Response Protocol** — The Analyst executes the reconstruction work within COC-3. When the subpoena arrives, the Chain of Custody Lead runs the protocol; the Analyst does the document work.

-----

## Quick Menu

*Select by what you’re experiencing, not by tool name.*

|What you’re experiencing                                       |Use this tool                      |
|---------------------------------------------------------------|-----------------------------------|
|“I need to reconstruct what the AI did in a specific decision” |ADA-1 Decision Chain Reconstruction|
|“I have logs but I don’t know what they mean”                  |ADA-2 Log Interpretation Protocol  |
|“I need to produce a summary a non-technical person can use”   |ADA-3 Plain-Language Translation   |
|“I need to find all the gaps in this record”                   |ADA-4 Gap Identification Audit     |
|“I’m seeing the same problem showing up in multiple records”   |ADA-5 Pattern Detection            |
|“I need to check whether documentation standards are being met”|ADA-6 Documentation Standards Audit|
|“Something in this record doesn’t add up”                      |ADA-7 Consistency Check            |
|“I need to prepare materials for a proceeding or inquiry”      |ADA-8 Proceeding Preparation       |

-----

## ADA-1. Decision Chain Reconstruction

*What did the AI actually do in this specific decision?*

**What it does:** The foundational tool. Every other tool in this guide depends on this one working correctly. Reconstructs the complete sequence of events for a single AI-assisted HR decision: what the AI received as input, what it produced as output, what the human did with that output, and what decision followed.

**Protocol:**

**Anchor:** Name the specific decision you are reconstructing. Date, employee, decision type (hiring, performance, discipline, termination, compensation, benefits). This is your anchor. Everything you reconstruct must connect back to this specific decision.

**Identify the tool:** Which AI system was involved? Get the specific name and version if possible. If version is unknown, document what you do know and flag the gap.

**Input:** What data did the AI receive? Sources may include: HRIS data, applicant tracking system data, performance management data, prior AI outputs, manager-provided context. List what you can confirm; flag what you cannot.

**Output:** What did the AI produce? Retrieve the actual output if it exists. If it was modified before use, retrieve both the original and the modified version. Document the difference.

**Human review:** Who reviewed the output? When? What did they do with it — confirm, modify, or override? Is this documented? If the review is documented only as a UI checkbox, flag that.

**Decision:** What decision was made? When? By whom? Is the connection between the AI output and the decision explicit in the record, or inferred?

**Timeline:** Assemble the chain in sequence: input received → AI output produced → human review → decision taken. Gaps in the timeline are findings.

**Output of this tool:** A Decision Chain Reconstruction memo — one page if possible, plain language, organized in chronological sequence, with all gaps explicitly named.

**Stop if:** You are inferring steps that are not documented. An inference is not a reconstruction. Document what you know, name what you are inferring, and flag what you cannot determine.

-----

## ADA-2. Log Interpretation Protocol

*The logs exist. What do they mean?*

**What it does:** AI system logs are not written for HR practitioners. They are written for engineers. This tool provides a structured approach for extracting the information that matters for governance purposes from logs that were not designed to provide it.

**Protocol:**

**Scope:** What logs do you have access to? (API logs, audit logs, system event logs, access logs, output logs.) List what exists and what you cannot access.

**Anchor to decision:** Before reading any log: what specific question are you trying to answer? “What model version was running on March 15?” is a question you can answer from a log. “Was this decision fair?” is not. Anchor every log review to a specific question.

**Timestamp alignment:** Identify the timestamps in the logs that correspond to the decision you are reconstructing. Work outward from there. Do not read the entire log — read the relevant window.

**Key data points to extract:**

- Model version or model identifier (what was running?)
- Input identifiers (what data was submitted?)
- Output identifiers (what was produced?)
- User or session identifiers (who initiated the request?)
- Timestamps (when did each step occur?)
- Error or exception flags (did anything fail or behave unexpectedly?)

**What logs cannot tell you:** Whether the human reviewer genuinely read the output. Whether the decision was fair. Whether the AI’s behavior was appropriate. Logs tell you what happened technically — not whether what happened was right.

**Translation:** Convert what you found into plain language before reporting. “The API log shows a request submitted at 14:32:07 with model identifier GPT-4-HR-v2.1, returning a response at 14:32:19” is accurate but not useful. “The AI tool received the candidate’s application at 2:32pm and produced an assessment within 12 seconds, using model version 2.1” is what the Chain of Custody Lead needs.

**Stop if:** The logs are so technical that you cannot extract meaningful information without engineering support. Name that gap, request support, and do not produce a reconstruction that implies more certainty than you have.

-----

## ADA-3. Plain-Language Translation

*The technical record exists. Now make it usable.*

**What it does:** Converts technical documentation — logs, AI outputs, system records, vendor documentation — into language that a non-technical reviewer (employment attorney, HR director, arbitrator, EEOC investigator) can understand and rely on. This is not simplification. It is translation. The accuracy must survive.

**Protocol:**

**Audience:** Who will read this? An employment attorney needs different language than an EEOC investigator, who needs different language than an employee in a dispute proceeding. Name the audience before you write.

**One fact per sentence:** Technical records often compress multiple facts into single statements. Unpack them. “The model v2.3 processed 847 applicant records between January 3 and March 15, flagging 23% for manual review” contains four facts: model version, record count, date range, and flag rate. Treat them as four sentences if your audience needs to understand each independently.

**Define every term on first use:** Model version, API, adverse impact, chain of custody, RLHF — none of these should appear undefined in a document going to a non-technical audience.

**What happened, then what it means:** Lead with the factual description, then explain the governance significance. “The system log shows no record of a human reviewer accessing this output before the rejection was issued. This means the chain of custody documentation does not include evidence of the required human review step.”

**Preserve gaps:** If you don’t know something, say so plainly. “The vendor has not provided model version documentation for this period. We cannot confirm which version of the tool was running.” Do not write around a gap. Name it.

**Test:** Read your translation aloud. If you would need to explain a sentence to someone who reads it, rewrite the sentence.

**Stop if:** You are producing a translation that makes the record look better or more complete than it is. Translation serves accuracy. If the accurate translation reveals a significant gap, that is what it should reveal.

-----

## ADA-4. Gap Identification Audit

*What is missing from this record?*

**What it does:** The systematic search for absence. The most dangerous documentation gaps are the ones nobody noticed. This tool makes absence visible by checking every element that should be present in a complete chain-of-custody record.

**The complete record checklist — every AI-assisted HR decision should have:**

|Element                                                      |Present?|If No: Can It Be Reconstructed?|
|-------------------------------------------------------------|--------|-------------------------------|
|AI tool name                                                 |Y / N   |                               |
|AI tool version                                              |Y / N   |                               |
|Date and time of AI processing                               |Y / N   |                               |
|Input data description                                       |Y / N   |                               |
|AI output (original, unmodified)                             |Y / N   |                               |
|Human reviewer name                                          |Y / N   |                               |
|Human reviewer date and time                                 |Y / N   |                               |
|Human reviewer assessment (confirmed / modified / overridden)|Y / N   |                               |
|If modified or overridden: what changed and why              |Y / N   |                               |
|Decision taken                                               |Y / N   |                               |
|Decision maker name                                          |Y / N   |                               |
|Decision date                                                |Y / N   |                               |
|Employee notification (if required)                          |Y / N   |                               |
|Retention period compliance                                  |Y / N   |                               |

**Protocol:**

**Run the checklist** for the specific decision under review.

**For each N:** Can this element be reconstructed from other sources (email, calendar, system logs)? If yes, attempt reconstruction and document the source. If no, document the gap explicitly.

**Gap classification:**

- **Blocking gap:** Missing element that cannot be reconstructed and is essential to demonstrating human review occurred. (Example: no human reviewer identity on an Employee Champion decision.) This finding must be escalated immediately.
- **Significant gap:** Missing element that weakens the record but does not eliminate the ability to demonstrate process. (Example: AI output version unknown but model vendor can confirm the version running on a specific date.)
- **Documentation gap:** Missing element that is recoverable with additional effort. (Example: decision date not in the AI record but in the HRIS system.)

**Output:** A Gap Identification memo listing each gap, its classification, and whether reconstruction is possible. Plain language. One page if possible.

**Stop if:** You are classifying blocking gaps as significant to make the record look better. The classification serves the Chain of Custody Lead’s ability to prioritize remediation — inflating it helps no one.

-----

## ADA-5. Pattern Detection

*Is this gap in one record, or is it in all of them?*

**What it does:** A single documentation gap in a single record is a Pebble. The same gap across fifty records is a systemic failure. Pattern detection is how individual audit findings become organizational intelligence. This is the tool that turns the Analyst’s work into something more than case-by-case reconstruction.

**Protocol:**

**Sample:** Pull a sample of recent AI-assisted decisions of the same type. (Minimum: 10 records. More is better, but 10 reveals most patterns.)

**Checklist:** Run ADA-4 (Gap Identification Audit) on each record in the sample.

**Aggregate:** For each checklist element, what percentage of records have the element present?

**Threshold:**

- 95%+ present: standard is being met
- 80–94% present: compliance is inconsistent — identify the circumstances where it fails
- Below 80%: standard is not being met — this is a systemic finding

**Identify the pattern:** When the gap occurs, what else is true? Same AI tool? Same reviewer? Same time period? Same decision type? The pattern is the finding, not the individual gaps.

**Report:** A Pattern Detection memo to the Chain of Custody Lead. Lead with the finding: “Human reviewer identity is missing from 34% of AI-assisted performance review records in Q1 2026.” Then the pattern: “Missing records cluster in the period before the new review workflow was implemented.” Then the implication: “Records from February and earlier may not meet evidentiary standards for documentation of human oversight.”

**Stop if:** You are identifying patterns to assign blame rather than to diagnose the system. Pattern detection serves remediation, not punishment.

-----

## ADA-6. Documentation Standards Audit

*Are our documentation standards actually being followed?*

**What it does:** A periodic check that the governance standards the Chain of Custody Lead has established are being met in practice. The gap between designed governance and actual governance is where liability accumulates. This tool measures that gap.

**Protocol:**

**Identify the standard:** What documentation is required for each AI tool in use? Pull the deployment records, the workflow design, and the documented review requirements.

**Sample:** Pull 10–20 recent records across the AI tools in scope.

**Compliance check:** For each record: does it meet the documented standard? (Y/N — no partial credit)

**Discrepancy log:** Any record that does not meet the documented standard is a discrepancy. Log it: which tool, which element missing, which decision, which date.

**Systemic discrepancy:** If the same element is missing across multiple tools or multiple reviewers, the standard itself may need to be redesigned — it may not be achievable in the current workflow.

**Findings memo:** Report to the Chain of Custody Lead. Lead with the compliance rate. Follow with the specific discrepancies. Distinguish between one-off failures and systemic patterns (ADA-5).

**Stop if:** The audit is being used to evaluate individual reviewer performance rather than system design. A reviewer who consistently cannot meet the documentation standard may need support — but the first diagnostic is whether the standard is achievable in the designed workflow.

-----

## ADA-7. Consistency Check

*Something in this record doesn’t add up.*

**What it does:** The targeted diagnostic when something in a specific record feels internally inconsistent. Timestamps that don’t make sense. A decision that doesn’t match the AI output. A review that is documented but implausible. This tool provides structure for investigating the inconsistency.

**Protocol:**

**Name the inconsistency:** Be specific. “The human review is timestamped 14:32 but the AI output wasn’t produced until 14:47” is a specific inconsistency. “Something feels off” is not. Name it before you investigate it.

**Collect the relevant elements:** Pull every element of the record that touches the inconsistency. Do not pull the whole record — pull the specific elements in question.

**Check each element independently:** Can each element be confirmed from an independent source? (The timestamp from system logs, the reviewer identity from access logs, the decision from the HRIS system.) Independent confirmation is the standard.

**Possible explanations:** For the inconsistency you’ve identified, what are the possible explanations?

- Data entry error (most common, least concerning)
- System clock misalignment (technical, fixable)
- Retroactive documentation (concerning)
- Record modification (very concerning)
- Genuine workflow irregularity (case-by-case assessment)

**Escalation threshold:** If the most likely explanation is retroactive documentation or record modification, escalate to the Chain of Custody Lead and legal immediately. Do not investigate further without guidance.

**Document your work:** Even if the inconsistency resolves into a benign explanation, document what you found and how you resolved it. An unexplained inconsistency that was never investigated is worse than an inconsistency that was investigated and explained.

**Stop if:** You are investigating an inconsistency that the Chain of Custody Lead or legal should be aware of before you proceed. When in doubt about scope, ask before digging.

-----

## ADA-8. Proceeding Preparation

*We have a dispute, investigation, or regulatory inquiry. What do I produce?*

**What it does:** Structures the Analyst’s contribution to formal proceedings. The Chain of Custody Lead runs COC-3 (Adversarial Response Protocol). The Analyst executes the document work within it. This tool defines that work.

**Protocol:**

**Scope from counsel:** Before producing anything, confirm with employment counsel what is in scope, what is privileged, and what format is required. Do not produce documents without this guidance.

**What the Analyst produces:**

- Decision Chain Reconstruction memos (ADA-1) for each decision in scope
- Gap Identification Audits (ADA-4) for each record in scope
- Plain-Language Translations (ADA-3) of any technical records being produced
- A summary index: all decisions in scope, all documents produced, all gaps identified

**What the Analyst does not produce:**

- Legal conclusions or assessments of liability
- Characterizations of whether decisions were fair or unfair
- Opinions on whether the organization’s AI use was appropriate
- Anything that has not been reviewed by counsel before production

**Quality standard for proceedings:** The plain-language standard (ADA-3) is more important here than anywhere else. A document that requires explanation during a deposition is a liability. Every document produced must stand alone.

**Gap handling in proceedings:** Gaps identified in ADA-4 must be disclosed honestly. Attempting to hide or minimize gaps in produced records is obstruction. Name every gap clearly.

**Index everything:** Maintain a complete index of what you produced, when you produced it, and to whom. This is itself a chain-of-custody record.

**Stop if:** You are being asked to produce documents without legal guidance, to characterize records in ways that exceed your role, or to omit identified gaps from produced materials. All three require immediate escalation to the Chain of Custody Lead and counsel.

-----

## Tool Frequency Summary

|Tool                               |Frequency                                      |Trigger                                                              |
|-----------------------------------|-----------------------------------------------|---------------------------------------------------------------------|
|ADA-1 Decision Chain Reconstruction|Per dispute, inquiry, or audit request         |Any time a specific AI-assisted decision is under review             |
|ADA-2 Log Interpretation Protocol  |Per reconstruction request requiring log access|When ADA-1 requires technical log review                             |
|ADA-3 Plain-Language Translation   |Per document going to non-technical audience   |Any time reconstructed records will be used in a proceeding or review|
|ADA-4 Gap Identification Audit     |Per record reviewed                            |Runs inside ADA-1 and ADA-8                                          |
|ADA-5 Pattern Detection            |Quarterly                                      |Also: when ADA-4 reveals a gap that may be systemic                  |
|ADA-6 Documentation Standards Audit|Quarterly                                      |Feeds Chain of Custody Lead’s COC-8 (Governance Integrity Check)     |
|ADA-7 Consistency Check            |When triggered                                 |Any record that contains an apparent internal inconsistency          |
|ADA-8 Proceeding Preparation       |When triggered                                 |Dispute, regulatory inquiry, litigation                              |

-----

## The Three Capabilities That Predict Effectiveness

The JD names these. This guide is built around them.

**Reading logs without getting lost.** You will spend significant time in system logs that were not designed for you. The discipline is anchoring every log review to a specific question before you start, and stopping when you’ve answered it. The log will always offer more than you need. Take only what answers the question.

**Writing plainly about technical findings.** A technically accurate summary that a non-technical person cannot use is not useful. Every document you produce will be read by someone who does not know what an API log is. Write for them.

**Recognizing absence as data.** The most important skill in this role. A gap you didn’t name is a gap that looks like concealment. A gap you named is a gap that looks like honesty. When you cannot find something, that finding is as important as what you do find — sometimes more important.

-----

## What This Profile Explicitly Avoids

Legal conclusions. Assessments of fairness. Governance decisions. Blame assignment. Producing documents without counsel guidance in adversarial contexts. This profile is about producing accurate, honest, plain-language records — not about deciding what those records mean.

-----

## Relationship to Other Practitioner Guides

|Related Document                          |Relationship                                                                                                                            |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
|<coc-lead-practitioner-guide.md>          |The COC Lead runs the governance system; the Audit Analyst executes the forensic work within it. COC-3 and COC-6 delegate to this guide.|
|<jd-ai-decision-audit-analyst.md>         |The JD describes the role. This guide tells you how to do it.                                                                           |
|<dispute-resolution-practitioner-guide.md>|The Dispute Resolution Lead uses ADA-1, ADA-3, and ADA-4 outputs to run proceedings.                                                    |
|Food Pantry Manager Profile               |Structural model this guide is built from.                                                                                              |

-----

## How to Use This Document

**This document is cold storage. It is not loaded into sessions.**

**For daily use:** Consult the Quick Menu. Deploy one tool. Use it. Document your work. Return to work.

**For reconstructions:** ADA-1 first. Always. Everything else follows from the chain.

**For proceedings:** Brief counsel before running ADA-8. No exceptions.

**For quarterly work:** ADA-5 and ADA-6. These feed the Chain of Custody Lead’s governance review.

-----

*The Frozen Kernel keeps you safe.*
*These tools help you think clearly inside the safe space.*

*AI Decision Audit Analyst Practitioner Guide · v1.0 · March 2026*
*AI Safety in HR Framework · Future Roles Series*
*Sovereign humans. Always.*
