# Recruitment and Hiring Mode Safety Ledger

*A binary safety scorecard for AI systems operating in talent acquisition*

*Part of the AI Safety in HR Framework · Safety Ledger Series · v1.0 · Richard Porter · 2026*

*[← Back to Safety Ledgers](README.md)*

-----

**
**Recruitment and Hiring Mode Safety Ledger**

*A binary safety scorecard for AI systems operating in talent
acquisition.*

v1.0 · March 2026 · Richard Porter · Part of the AI Safety in HR
Framework

| **Design Principle**                                                  |
|                                                                       |
| Hiring decisions require documented, human-authorized, legally        |
| defensible chains of custody. Safety must be built into the system    |
| architecture, not added as post-hoc disclaimers or policy statements. |
| This ledger evaluates whether specific architectural features exist   |
| — not whether vendor intentions are good, not whether features are  |
| on the roadmap.                                                       |

**What This Is**

AI systems are now sourcing candidates, screening resumes, scheduling
interviews, assessing fit, generating offers, and processing onboarding.
When these systems fail in employment contexts, the consequences are not
product defects — they are wrongful exclusion claims, EEOC complaints,
disparate impact findings, and ADA violations. The organization cannot
point to the AI vendor. The organization is liable.

This ledger defines the surviving HR role in a future-state talent
acquisition COE where AI has absorbed most of the transactional work.
That role is not coordination. It is governance — the chain-of-custody
owner who ensures every AI output that influences a hiring decision can
be defended in a legal proceeding.

**Who This Is For**

HR professionals evaluating AI solutions for talent acquisition
deployment. Specifically: the practitioner who will be named in the EEOC
charge if the system fails. Not for vendors. Not for procurement teams
unfamiliar with employment law. For the HR professional who has to sign
off on this and who carries the legal and ethical weight of that
signature.

**Empirical Basis**

These criteria are grounded in documented failures and regulatory
findings:

-----

**Case**          **What Happened**            **Ledger Application**

EEOC v.           The EEOC's first AI hiring  Anchors Section 1
iTutorGroup       discrimination settlement:   (Adverse Impact Gate) and
(2023)            $365,000. Hiring software   Section 3 (Protected
programmed to automatically  Class Boundary).
reject female applicants     Demonstrates that
aged 55+ and male applicants automated age
aged 60+. Discovered when a  discrimination is legally
rejected applicant           equivalent to intentional
resubmitted with a different discrimination.
birth date — identical
application, offered an
interview.

Mobley v. Workday Class action alleging        Anchors Section 4 (Chain
(2023–ongoing)   Workday's AI-powered        of Custody) and Section
applicant screening tools    11 (Vendor
discriminate on the basis of Accountability).
race, age, and disability.   Establishes that vendor
In May 2025 a federal judge  delegation does not
certified a nationwide       transfer liability from
collective action under the  the deploying
ADEA covering potentially    organization.
millions of applicants over
40. The court explicitly
held that "Workday's role
in the hiring process is no
less significant because it
allegedly happens through
artificial intelligence."

D.K. v. Intuit /  An Indigenous and deaf       Anchors Section 7
HireVue (ACLU     Intuit employee requested    (Accommodation and ADA
complaint, March  human-generated captioning   Compliance). Demonstrates
2025)             as an ADA accommodation for  the accommodation pathway
an AI video interview.       failure mode: an AI
Request denied. She was      system with no structural
rejected for the promotion.  accommodation path cannot
AI-generated feedback told   meet the ADA interactive
her to "practice active     dialogue requirement.
listening."

Amazon Hiring     Amazon discontinued an       Anchors Section 3
Algorithm (2018)  internal AI hiring tool      (Protected Class
after discovering it         Boundary) and Section 10
systematically downgraded    (Audit and
resumes from women's        Explainability).
colleges, having been        Demonstrates that proxy
trained predominantly on     discrimination compounds
male candidate data and      silently without ongoing
learning to prefer resume    demographic parity
language more common among   testing.
men.

-----

**The EEOC was explicit in the iTutorGroup settlement: "Even when
technology automates the discrimination, the employer is still
responsible." This is the governing legal principle for every section
of this ledger.**

**Five Ledger Selection Criteria — Verified**

-----

**Criterion**       **Status**

Asymmetric          ✅ Candidates cannot evaluate screening algorithm
Expertise           logic, adverse impact calculations, or model
validation. The power asymmetry is maximized at the
precise moment candidates are most dependent on the
process.

High Specific       ✅ Wrongful exclusion, disparate impact liability,
Consequence         individual EEOC charges, class action exposure. The
Workday collective — potentially hundreds of
millions of applicants — represents the upper
bound of scale.

Domain-Specific     ✅ Proxy discrimination, adverse impact at scale,
Failure Modes       accommodation exclusion, compensation disparities,
framing bypass (iTutorGroup's birth date bypass
demonstrates this precisely).

Regulatory Analogue ✅ EEOC Uniform Guidelines on Employee Selection
Procedures (1978, still in force). EEOC Strategic
Enforcement Plan 2024–2028 naming AI in hiring as
a priority. NYC Local Law 144. Colorado SB 21-169.
Illinois AI Video Interview Act.

Canonical Sources   ✅ EEOC Uniform Guidelines, 29 CFR Part 1607. EEOC
technical assistance documents. Griggs v. Duke
Power Co., 401 U.S. 424 (1971) — job-relatedness
requirement still governs.

-----

**The Eleven Criteria Sections**

**Section 1 — Adverse Impact Gate**

Disparate impact — when a facially neutral selection criterion
disproportionately excludes a protected class — is the central legal
risk in AI-assisted hiring. The EEOC Uniform Guidelines on Employee
Selection Procedures (1978) establish the four-fifths rule as the
primary adverse impact test. This has not changed. AI does not exempt an
organization from it.

Binary tests:

- Does the system conduct automated adverse impact analysis against
  all protected classes at each selection stage before candidates are
  advanced or rejected? (Y/N)
- When adverse impact is detected at any stage, does the system
  automatically halt the selection process and require human review
  before continuation? (Y/N)
- Is the adverse impact analysis documented and retained for each
  selection event, with timestamps and decision records? (Y/N)
- Does the system apply the four-fifths rule (EEOC Uniform Guidelines)
  as a deterministic threshold, not a configurable setting that can be
  turned off? (Y/N)
- Does the system test for intersectional disparate impact (e.g.,
  Black women, not just race and gender separately)? (Y/N)

| **Failure Mode: Proxy Discrimination**                                |
|                                                                       |
| The system excludes protected class members through correlated        |
| variables (zip code for race, employment gap for pregnancy, name      |
| patterns for national origin) while technically operating on neutral  |
| criteria. The iTutorGroup case demonstrates that the mechanism of     |
| discrimination — automated or human — does not change the         |
| employer's liability.                                                |

Regulatory anchor: EEOC Uniform Guidelines on Employee Selection
Procedures, 29 CFR Part 1607. Executive Order 11246 (OFCCP). ADA Title
I.

**Section 2 — Candidate Disclosure Architecture**

Candidates have a right to know they are being evaluated by an AI
system. This is not aspirational — it is increasingly codified in law
(New York City Local Law 144, Colorado SB 21-169, Illinois AI Video
Interview Act). Disclosure must be structural, not behavioral.

Binary tests:

- Is candidate disclosure of AI involvement structurally generated at
  the system level, not dependent on recruiter remembering to
  disclose? (Y/N)
- Does disclosure occur before any AI assessment begins — not after,
  not in terms of service, not in fine print? (Y/N)
- Does the disclosure specify what the AI is evaluating — not just
  that AI is being used, but what dimensions, criteria, or data points
  are being assessed? (Y/N)
- Is there a documented, accessible opt-out path for candidates who
  request human-only evaluation? (Y/N)
- Is the opt-out path functionally equivalent — opting out does not
  disadvantage the candidate or remove them from consideration? (Y/N)
- Does the disclosure architecture comply with all jurisdictions in
  which the organization operates, not only the most permissive? (Y/N)

Regulatory anchor: NYC Local Law 144 (2023). Illinois AI Video Interview
Act (820 ILCS 42). Colorado SB 21-169. EU AI Act Article 50.

**Section 3 — Protected Class Boundary**

Some data points must never be assessed, regardless of what the AI
system is technically capable of detecting. Systems that can infer
protected class status from voice, video, name, or behavioral patterns
must have hard architectural exclusions — not policy statements.

Binary tests:

- Does the system have hard architectural exclusions preventing the
  use of the following in any hiring assessment? (Y/N for each): Race
  or ethnicity including name pattern and zip code proxies; Sex,
  gender identity, or pregnancy status; Age including graduation year
  and employment gap proxies; Disability status including movement and
  speech pattern proxies; Religion including name and affiliation
  proxies; National origin including accent analysis; Genetic
  information
- Are these exclusions enforced at the input layer before model
  processing, not filtered at the output layer after assessment? (Y/N)
- Is there a documented audit process that verifies proxy exclusions
  are functioning, run on a defined cycle? (Y/N)
- Can the exclusions be overridden by any user, administrator, or
  configuration setting? (Y/N — answer must be NO to pass)

| **Note on Employment Gap as Pregnancy Proxy**                         |
|                                                                       |
| Employment gaps are among the most common proxy variables for         |
| pregnancy status in AI hiring tools — and among the least flagged.  |
| An AI trained on historical hiring data will learn that gaps in       |
| employment correlate with subsequent lower performance ratings        |
| (themselves a product of return-from-leave bias), and use gaps as a   |
| negative signal. This is protected class discrimination. The          |
| exclusion must be explicit and tested.                                |

Regulatory anchor: Title VII. ADA Title I. Age Discrimination in
Employment Act (ADEA). Genetic Information Nondiscrimination Act (GINA).
Pregnancy Discrimination Act.

**Section 4 — Chain of Custody**

Every AI output that influences a hiring decision must be attributable
specific human who reviewed and authorized it. This is the evidentiary
requirement for defending a hiring decision in litigation. The Workday
case established that when an employer delegates its screening function
to an AI platform, the platform's role is no less significant because
it happened through software.

Binary tests:

- Does the system generate an immutable chain-of-custody record for
  every candidate at every selection stage? (Y/N)
- Does the record include: model version, assessment timestamp, input
  data used, output produced, human reviewer identity, and review
  timestamp? (Y/N)
- Is the chain-of-custody record tamper-evident — modifications are
  logged, not overwritten? (Y/N)
- Is the record retained for the legally required period in each
  applicable jurisdiction (minimum three years under most EEOC
  record-keeping requirements)? (Y/N)
- Can a complete chain-of-custody record be produced within 72 hours
  in response to a regulatory inquiry or litigation hold? (Y/N)
- Does the system flag and log any instance where a human overrides an
  AI recommendation, including the reason given? (Y/N)

Regulatory anchor: EEOC Record-Keeping Requirements, 29 CFR Part 1602.
OFCCP record-keeping obligations. Federal Rules of Civil Procedure
(litigation hold requirements).

**Section 5 — Human Override Requirements**

AI in talent acquisition is a recommendation engine. The human HR
professional is the decision-maker. This distinction must be
architectural, not aspirational. Systems designed to make human override
difficult, inconvenient, or statistically invisible have inverted the
governance relationship.

Binary tests:

- Is human review required before any rejection at any stage of the
  hiring process? (Y/N)
- Can a human reviewer override any AI recommendation with a single
  documented action, without re-litigating with the system? (Y/N)
- Does the override create a logged record that the human decision
  differed from the AI recommendation? (Y/N)
- Does the system surface the AI's reasoning to the human reviewer in
  plain language before the reviewer confirms or overrides? (Y/N)
- Is there a maximum queue size that prevents human reviewers from
  being overloaded to the point where review becomes rubber-stamping?
  (Y/N)
- Does the system track override rates by reviewer and flag reviewers
  whose override rate drops below a defined threshold as a Conductor
  Fatigue Exploitation signal? (Y/N)

| **Failure Mode: Conductor Fatigue Exploitation**                      |
|                                                                       |
| The AI's output rate exceeds the human reviewer's genuine review    |
| capacity, converting the human from a decision-maker into a rubber    |
| stamp. The human signature is present. The human judgment is not.     |
| This is the failure mode that makes chain-of-custody documentation    |
| meaningless — the review is documented but not real.                |

**Section 6 — Offer and Compensation Constraint**

AI-generated compensation recommendations carry specific legal exposure.
Pay equity laws apply to how compensation is determined, not just what
is paid. An AI that generates offers based on salary history,
negotiation patterns, or market data without demographic parity analysis
creates immediate legal exposure.

Binary tests:

- Does the system conduct pay equity analysis before generating any
  compensation recommendation, testing for gender, race, and other
  protected class disparities? (Y/N)
- Is salary history excluded from the compensation model in
  jurisdictions where salary history inquiry is prohibited? (Y/N)
- Does the system apply pay band enforcement as a hard constraint —
  offers outside the approved band require documented human
  escalation? (Y/N)
- Does the system disclose the basis for a compensation recommendation
  to the reviewing HR professional in terms that can be defended under
  pay transparency requirements? (Y/N)
- Are compensation recommendations flagged for human review whenever
  the recommended offer falls below the midpoint of the band for the
  role? (Y/N)
- Does the system log all offer negotiations and analyze them for
  protected class patterns on a defined audit cycle? (Y/N)

Regulatory anchor: Equal Pay Act. Title VII compensation provisions.
State-level pay transparency laws (California, Colorado, New York,
Washington, Illinois). Salary history prohibition statutes.

**Section 7 — Accommodation and ADA Compliance**

The Americans with Disabilities Act requires reasonable accommodation in
the hiring process itself — not just in employment. The Intuit/HireVue
case illustrates the architectural failure precisely: an accommodation
request was denied, the AI could not assess the candidate accurately,
and the AI-generated feedback criticized the disability itself. An
AI-mediated hiring process without a structurally accessible
accommodation pathway is not ADA-compliant, regardless of intent.

Binary tests:

- Is there a human-accessible accommodation request pathway that
  bypasses the AI assessment process entirely? (Y/N)
- Is the accommodation pathway disclosed to all candidates at the
  beginning of the application process — not only when a candidate
  self-identifies as having a disability? (Y/N)
- Does the system route accommodation requests directly to a qualified
  human without requiring the candidate to first interact with the AI?
  (Y/N)
- Is the accommodation pathway functionally equivalent — a candidate
  who requests accommodation is evaluated for the same role on the
  same criteria, through a human-led process? (Y/N)
- Does the system log all accommodation requests and track
  accommodation outcomes to ensure accommodated candidates are not
  disproportionately excluded? (Y/N)
- Is there a documented process for interactive dialogue (as required
  by ADA) when the appropriate accommodation is not immediately clear?
  (Y/N)

Regulatory anchor: Americans with Disabilities Act, Title I. EEOC
Technical Assistance Document on AI and Disability Discrimination (2023,
removed from EEOC website January 2025 — available on Internet
Archive). EEOC Enforcement Guidance on Reasonable Accommodation (2002).

**Section 8 — Data Minimization and Retention**

AI hiring systems collect more candidate data than any previous hiring
process. The candidate who doesn't get the job has no ongoing
relationship with the organization — but the organization may retain
their behavioral data, video recordings, voice patterns, and assessment
scores indefinitely. This is both a privacy risk and a legal exposure.

Binary tests:

- Does the system collect only the data required for the specific
  assessment being conducted — no additional behavioral, biometric,
  or inferred data? (Y/N)
- Is there a documented data retention schedule for rejected candidate
  data, with automatic deletion at the end of the retention period?
  (Y/N)
- Is candidate data excluded from model training without explicit,
  informed, separate consent from the candidate? (Y/N)
- Does the system comply with biometric data laws in all jurisdictions
  where candidates are located (Illinois BIPA, Texas, Washington)?
  (Y/N)
- Is there a candidate data access pathway — a process by which a
  candidate can request what data was collected and how it was used?
  (Y/N)
- Does the system have a documented process for responding to data
  deletion requests from candidates in jurisdictions with deletion
  rights (CCPA, GDPR)? (Y/N)

Regulatory anchor: Illinois Biometric Information Privacy Act (BIPA).
California Consumer Privacy Act (CCPA). GDPR Article 17 (right to
erasure). EEOC record-keeping minimums.

**Section 9 — The Wrongful Termination Test Gate**

| **The Governing Heuristic for This Entire Ledger**                    |
|                                                                       |
| If this AI output were entered as evidence in a wrongful exclusion    |
| proceeding, could you defend every step of the process that produced  |
| it? What criteria were applied? What data was assessed? What was the  |
| AI output? Who reviewed it? When? Was the candidate informed? If the  |
| answer to any of these is "the AI handled it" — the organization  |
| is exposed.                                                           |

Binary tests:

- Can the system produce, for any rejected candidate, a complete
  decision record that includes: what criteria were applied, what data
  was assessed, what the AI output was, who reviewed it, and when?
  (Y/N)
- Is the decision record produced automatically at the point of
  rejection, not reconstructed retroactively? (Y/N)
- Does the decision record use job-related criteria only — criteria
  that have been validated against job performance for the specific
  role? (Y/N)
- Is there a documented validation study for each AI assessment tool,
  conducted for the specific role family in which it is deployed?
  (Y/N)
- Does the system flag when it is being applied to a role for which it
  has not been validated? (Y/N)
- Is the system documented as a recommendation tool, not a
  decision-making tool, in all materials provided to hiring managers?
  (Y/N)

Regulatory anchor: EEOC Uniform Guidelines, Section 15 (record-keeping
for validation studies). Griggs v. Duke Power Co., 401 U.S. 424 (1971).
NYC Local Law 144 (bias audit requirements).

**Section 10 — Audit and Explainability**

An AI system that cannot explain its outputs to the humans responsible
for them has inverted the governance relationship. The HR professional
is accountable for decisions the system made. They must be able to
understand what the system did.

Binary tests:

- Does the system provide plain-language explanations of assessment
  outputs to HR reviewers — not scores alone, but the factors that
  produced the score? (Y/N)
- Are explanations role-specific — the system explains what it
  assessed for this role, not generic model behavior? (Y/N)
- Is there an independent bias audit conducted by a third party on a
  defined cycle (minimum annual)? (Y/N)
- Are bias audit results publicly available or available to the
  organization's HR team on request? (Y/N)
- Does the system have a documented escalation path for HR
  professionals who believe a specific output is wrong or
  discriminatory? (Y/N)
- Is there a pattern detection mechanism that identifies when similar
  candidates are being scored differently in ways that correlate with
  protected class membership? (Y/N)

Regulatory anchor: NYC Local Law 144 (annual bias audit requirement). EU
AI Act Article 13 (transparency for high-risk AI). EEOC technical
assistance on AI explainability.

**Section 11 — Vendor Accountability**

The organization is liable for what the vendor's system does. Vendor
indemnification clauses do not protect against EEOC complaints or class
action litigation. The Workday case established that a vendor whose AI
participates in the decision-making process may itself be liable as an
"agent" of the employer — but this does not reduce the employer's
own exposure.

Binary tests:

- Does the vendor provide contractual SLAs for bias audit completion
  — not best-effort, but enforceable timelines? (Y/N)
- Does the vendor provide model version documentation sufficient to
  reconstruct what version processed a specific candidate at a
  specific date? (Y/N)
- Does the vendor have a documented incident response process for
  discriminatory output findings, including notification timelines?
  (Y/N)
- Does the vendor provide validation study data for each assessment
  tool, specific to the role families for which deployment is
  recommended? (Y/N)
- Is there a contractual data deletion provision requiring the vendor
  to delete candidate data on the organization's instruction within a
  defined period? (Y/N)
- Does the vendor indemnify the organization for regulatory penalties
  arising from undisclosed model changes that affect adverse impact
  rates? (Y/N)

| **Failure Mode: Vendor Liability Transfer**                           |
|                                                                       |
| The organization deploys a vendor's AI system, the system produces   |
| discriminatory outcomes, and the organization discovers the vendor    |
| contract provides no meaningful protection. The EEOC's explicit      |
| position: the employer cannot point to the vendor. The organization   |
| is liable. Contract review before deployment is not optional.         |

**Scoring**

-----

**Score**        **Definition**

PASS             All binary tests return affirmative. Evidence is
publicly documented or contractually confirmed.

PARTIAL          Some binary tests pass. Others cannot be confirmed.
"Cannot be confirmed" defaults to FAIL, not PARTIAL.
The burden of evidence is on the vendor, not the
evaluator.

FAIL             Structural absence of the tested feature. A single
FAIL in Section 4 (Chain of Custody), Section 7
(Accommodation), or Section 9 (Wrongful Termination
Test Gate) is a deployment-blocking finding.

-----

*Total Score = Talent Acquisition AI Confidence Index (TAACI). TAACI
does not measure candidate matching quality. It measures deterministic
safety completeness for AI-assisted hiring.*

**Vendors Pending Evaluation**

The following platforms are candidates for evaluation against this
ledger. Evaluation is vendor-agnostic — the same criteria apply
regardless of market position or reputation. Evaluations open to
community contribution. Independent replication explicitly encouraged.

-----

**Platform**                 **Category / Status**

Workday Recruiting           ATS / AI screening — active litigation
(Mobley v. Workday, N.D. Cal. 23-cv-00770)

Greenhouse                   ATS

Lever                        ATS

HireVue                      Video assessment — active EEOC complaint
(D.K. v. Intuit/HireVue, March 2025)

Pymetrics / Harver           Behavioral assessment

LinkedIn Recruiter AI        Sourcing / matching

Eightfold AI                 Talent intelligence — active litigation
pending

SeekOut                      Sourcing

Paradox (Olivia)             Conversational AI / scheduling

Beamery                      Talent CRM

-----

**The Surviving HR Role**

In a future-state talent acquisition COE where AI has absorbed sourcing,
screening, scheduling, assessment, offer generation, and onboarding
processing, the human HR professional's role is not coordination. It is
governance.

**The questions this ledger asks are the questions that role requires:**

- Can I defend this?
- Do I understand what the system did?
- Is there a human signature on every decision that matters?
- Can I produce the record when asked?
- Did the candidate know what was happening to them?

If the answer to any of these is "the system handles it" — the HR
professional has abdicated the role this ledger exists to define. The AI
does the work. The human governs. That is the surviving function.

**What This Ledger Does Not Cover**

- Internal mobility and promotion decisions — a separate ledger is
  warranted
- Collective bargaining environments where AI deployment triggers
  negotiated obligations
- Cross-border hiring in jurisdictions with works council requirements
- Legal advice — an employment attorney should review any AI
  deployment in hiring before launch
- AI vendor security posture or data breach risk

**Relationship to Other Framework Documents**

-----

**Document**           **Relationship**

HRBP AI Safety         Parent document — quadrant-by-quadrant risk
Framework              mapping this ledger operationalizes. The
Administrative Expert quadrant is the primary
quadrant this ledger covers.

AI Vendor Scorecard    Companion procurement tool — covers all four
quadrants. This ledger provides the talent
acquisition-specific depth.

AI Deployment          Go-live governance — what must be in place
Checklist              before any AI hiring tool is deployed.

Crisis Intervention    Companion ledger for the Employee Champion
Safety Ledger          quadrant — different failure modes, same
binary evaluation methodology.

Chain of Custody Lead  The role this ledger is written for. Section 4
(JD)                   and Section 9 define the documentation standard
that role owns.

Employee Rights in     The candidate-facing rights document — covers
AI-Assisted Decisions  the disclosure and appeal rights defined in
Sections 2 and 4.

-----

*Recruitment and Hiring Mode Safety Ledger · v1.0 · March 2026*


