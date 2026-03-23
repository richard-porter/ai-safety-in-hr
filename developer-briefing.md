# What You Need to Know Before Building for HR

*A briefing for AI developers and product teams building tools for HR workflows.*

**Audience:** AI developers, product managers, and engineers building tools that will be used in HR contexts

*Richard Porter · Part of the AI Safety in HR Framework · 2026*

-----

> **The Core Fact**
> HR is not a typical software domain. A single AI failure in an HR context can produce a wrongful termination claim, an EEOC complaint, a wage and hour violation, or a hostile work environment finding. The organization cannot redirect liability to your product. This briefing tells you what that means for how you build.

-----

## The Four Quadrants You Are Building Into

Every HR AI tool operates in one or more of these quadrants. Know which one before you ship.

|Quadrant                 |What Happens Here                                 |AI Risk      |Your Responsibility                                                           |
|-------------------------|--------------------------------------------------|-------------|------------------------------------------------------------------------------|
|**Strategic Partner**    |Succession, workforce planning, talent calibration|HIGH         |Bias compounds over years. Demographic parity testing required pre-deployment.|
|**Change Agent**         |Culture, sentiment, DEI, change management        |MODERATE–HIGH|Failure modes that look like success. Dissenting signals must surface.        |
|**Employee Champion**    |ER, grievance, EAP, accommodation, crisis         |HIGHEST      |People in acute distress. Hard constraints required. Not optional.            |
|**Administrative Expert**|Benefits, HRIS, onboarding, job descriptions      |MODERATE     |Automates broken processes faster. Human audit cycle mandatory.               |

-----

## The Employee Champion Hard Stops

If your tool operates in the Employee Champion quadrant — or could be used there — these are non-negotiable:

**Explicit AI disclosure at conversation start.** Not in terms of service. Not in a help page. At the start of the interaction, in plain language. “You are speaking with an AI assistant.”

**Human escalation path.** Any employee who requests human contact must be able to reach a human within one business day. Your tool must not block, obscure, or discourage this path.

**No autonomous case decisions.** Your tool must not generate output that enters a disciplinary or personnel record without documented human review. The human review must be genuine — not a rubber stamp enabled by queue volume.

**No training on same-org ER data.** The privacy violation is structural. An employee who filed a harassment complaint did not consent to that complaint training a tool that will respond to future harassment complaints in the same organization.

**Crisis signal routing.** If your tool can receive any text input from employees, it will receive crisis signals — disclosures of self-harm, suicidal ideation, domestic violence, acute mental health episodes. Your tool must have a documented protocol for routing these to a qualified human before any AI response is generated. “We didn’t build it for that” is not a defense.

-----

## The Wrongful Termination Test

> *If this AI output were entered as evidence in a wrongful termination proceeding, could a lawyer defend every step of the process that produced it?*

Apply this to every output your tool produces that could influence a personnel decision.

**What this means in practice:**

- Uncertainty ranges are not optional. “Sarah is a 7.2/10 successor candidate” is false precision that will not survive cross-examination.
- Audit trails must be complete: model version, prompt or configuration, output, timestamp, human authorization identity and date.
- Proxy variables must be blocked at the input layer: zip code, graduation year, employment gap, part-time history, and name patterns are protected class proxies.
- Human override must be architectural, not aspirational. A “review” button that no one uses because the queue is 400 items long is not a human review gate.

-----

## Chain of Custody Architecture

Your tool must be able to answer these questions for any output that influenced a personnel decision:

|What must be logged        |Model version · prompt/configuration · output · timestamp · authorizing human identity · whether output was used in a personnel decision|
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
|**What must be blocked**   |Protected class data and known proxies at the input layer                                                                               |
|**What must be disclosed** |That AI was involved in generating any output used in a personnel decision                                                              |
|**What must be reversible**|Human override must supersede any AI recommendation with a single documented action                                                     |
|**What must be retained**  |Minimum three years in most EEOC jurisdictions                                                                                          |

-----

## Documented Cases You Should Know

|Case                                |What Happened                                                                                                                                                                   |What It Means for You                                                                                                            |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
|**EEOC v. iTutorGroup (2023)**      |$365K settlement. AI hiring tool rejected women 55+, men 60+.                                                                                                                   |Age discrimination through AI is legally equivalent to intentional discrimination. Your screening tool is not exempt.            |
|**Mobley v. Workday (2023–ongoing)**|Class action certified May 2025. Potentially millions of applicants alleging AI screening discrimination. Court: AI-assisted rejection is legally equivalent to human rejection.|Vendor delegation does not transfer liability. The deploying organization is exposed. So is the vendor — Workday itself is named.|
|**D.K. v. Intuit / HireVue (2025)** |Deaf employee denied ADA accommodation for AI video interview. AI feedback told her to “practice active listening.”                                                             |Your tool’s assessment criteria must be accommodation-neutral. The accommodation pathway must bypass the AI entirely.            |

-----

## What You May Not Know About HR

**HR professionals cannot defer compliance.** A product manager can ship a feature and address accessibility in the next sprint. An HRBP who uses a non-compliant AI tool cannot defer the EEOC charge.

**The organizations deploying your tool may not have legal review of AI.** Especially in nonprofits and mid-market companies. They are trusting your product to be safe. If you know your tool has proxy variable exposure and you haven’t disclosed it, you know something the deploying organization needs to know.

**Employee relations professionals are trained intermediaries for people in acute distress.** Your tool is not. Warmth in UX copy is a risk multiplier in ER contexts, not a feature.

**“The AI handled it” ends careers.** The HR director who approved deployment of a biased screening tool will be asked in a deposition who reviewed the system for adverse impact. If the answer is “we relied on the vendor,” that is not a satisfactory answer.

-----

> **Build the chain of custody first. The productivity features come after.**

*Part of the [AI Safety in HR Framework](../HRBP-master-framework.md)*  
*Full quadrant analysis: [HRBP-master-framework.md](../HRBP-master-framework.md)*  
*Vendor evaluation criteria: [for-hr-practitioners/ai-vendor-scorecard.md](../for-hr-practitioners/ai-vendor-scorecard.md)*  
*Sovereign humans. Always.*
