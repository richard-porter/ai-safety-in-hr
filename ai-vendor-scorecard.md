# AI Vendor Scorecard for HR Procurement

*The questions to ask before you deploy — organized by where the tool lands.*

**Audience:** HR practitioners, HRBPs, and procurement evaluators

-----

> **Who This Is For:** You are the person in HR who has been asked to evaluate, recommend, or sign off on an AI tool. This scorecard gives you the questions you need — organized by the Ulrich quadrant the tool operates in — so you are not making this decision without a framework.

-----

## Step 1: Identify the Quadrant

Before running any checklist, determine which quadrant(s) this tool operates in.

|Quadrant                 |If the tool does any of these things…                                                                            |
|-------------------------|-----------------------------------------------------------------------------------------------------------------|
|**Strategic Partner**    |Succession planning, workforce modeling, talent calibration, org design, headcount forecasting                   |
|**Change Agent**         |Culture surveys, sentiment analysis, change communications, DEI program support, learning personalization        |
|**Employee Champion**    |Employee relations intake, accommodation requests, grievance support, EAP routing, conflict resolution           |
|**Administrative Expert**|Benefits administration, HRIS workflows, onboarding/offboarding, job description generation, compliance reporting|

A tool may operate in more than one quadrant. Run the checklist for each applicable quadrant.

-----

## The Wrongful Termination Test — Run First

> *Ask yourself: If this AI output were entered as evidence in a wrongful termination proceeding, could I defend every step of the process that produced it? If you cannot answer yes with confidence — run the full scorecard below before proceeding.*

-----

## Strategic Partner Checklist

|Question                                                                                                         |Answer                |
|-----------------------------------------------------------------------------------------------------------------|----------------------|
|Does the tool output confidence intervals or uncertainty ranges alongside its predictions?                       |☐ Yes  ☐ No  ☐ Unknown|
|Has demographic parity testing been conducted? Is documentation available?                                       |☐ Yes  ☐ No  ☐ Unknown|
|Does the tool have access to zip code, graduation year, part-time work history, or other protected-class proxies?|☐ Yes  ☐ No  ☐ Unknown|
|Does every output that influences a personnel decision require documented human sign-off?                        |☐ Yes  ☐ No  ☐ Unknown|
|Can the tool produce an audit log showing which human authorized which decision and when?                        |☐ Yes  ☐ No  ☐ Unknown|
|Can you identify the specific model version that produced any given output?                                      |☐ Yes  ☐ No  ☐ Unknown|


> ⚠️ Any “No” or “Unknown” requires a vendor response in writing before procurement. Do not accept verbal assurances.

-----

## Change Agent Checklist

|Question                                                                                          |Answer                                        |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
|Does sentiment analysis output include dissenting signals, or only majority themes?               |☐ Includes dissent  ☐ Majority only  ☐ Unknown|
|Can outputs be filtered or adjusted by the vendor to reflect sponsor preferences?                 |☐ Yes  ☐ No  ☐ Unknown                        |
|Are AI-generated communication drafts clearly labeled as AI-generated before the human sends them?|☐ Yes  ☐ No  ☐ Unknown                        |
|Is DEI program design human-led with AI data support, or does AI generate the program?            |☐ Human-led  ☐ AI-generated  ☐ Unclear        |
|Are there separate metrics for engagement with the AI tool vs. actual change adoption?            |☐ Yes  ☐ No  ☐ Unknown                        |

-----

## Employee Champion Checklist

> ⛔ **Highest Risk Quadrant.** If any answer here is “No” or “Unknown,” do not deploy until resolved.

|Question                                                                                           |Answer                          |
|---------------------------------------------------------------------------------------------------|--------------------------------|
|Is the employee told — explicitly, at the start of interaction — that they are speaking with an AI?|☐ Yes  ☐ No  ☐ Unknown          |
|Is there a guaranteed path to reach a human? Is the SLA defined and enforced?                      |☐ Yes  ☐ No  ☐ Unknown          |
|Can AI outputs from this tool be used in disciplinary proceedings without documented human review? |☐ Blocked  ☐ Possible  ☐ Unknown|
|Is the tool trained on employee relations case data from the deploying organization?               |☐ No  ☐ Yes  ☐ Unknown          |
|Has an employment attorney reviewed the deployment configuration?                                  |☐ Yes  ☐ No  ☐ Planned          |
|Who has access to the log of employee interactions?                                                |Answer: ___________________     |
|What happens if an employee discloses a safety concern to the AI?                                  |Answer: ___________________     |

-----

## Administrative Expert Checklist

|Question                                                                           |Answer                             |
|-----------------------------------------------------------------------------------|-----------------------------------|
|Have the processes this tool automates been audited for accuracy before automation?|☐ Yes  ☐ No  ☐ Unknown             |
|Is there a documented human audit cycle for automated compliance workflows?        |☐ Yes  ☐ No  ☐ Unknown             |
|Do benefits eligibility determinations have a human appeal path?                   |☐ Yes  ☐ No  ☐ Unknown             |
|Are job descriptions reviewed for FLSA classification accuracy before posting?     |☐ Yes  ☐ No  ☐ Unknown             |
|Does the tool collect only the personal data it needs?                             |☐ Minimized  ☐ Expansive  ☐ Unknown|

-----

## Final Decision Gate

|Decision                     |Criteria                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------|
|🟩 **Proceed**                |All checklists complete. No unresolved “No” or “Unknown.” Employment attorney reviewed Employee Champion deployments.|
|🟨 **Proceed with conditions**|Minor gaps with written vendor commitments and remediation plan with owner and date.                                 |
|🟥 **Do not deploy**          |Any unresolved “No” in the Employee Champion checklist. Any unknown on audit trail or proxy variable access.         |


> **Remember:** The vendor is not liable for how their tool is used in your employment decisions. You are. This scorecard documents your due diligence. Keep it on file.

*See also: <ai-deployment-checklist.md> for go-live governance.*
