# Service Standard Maturity Model (Draft)

*Draft v0.2 for team discussion, November 2026. A CMMI-style maturity model built on the GOV.UK Service Standard, plus three local extension points. Companion to [cmmi_adaptation_approach.md](cmmi_adaptation_approach.md) and [research.md](research.md) (sections 3.1 and 3.23)*

## 1. Purpose

The **GOV.UK Service Standard** tells us *what* a good public service looks like (14 points). A **service assessment** checks, at set points (alpha, beta, live), whether each point is **met or not met**.

This model adds the **CMMI** view of *how mature* a team is against each point, so we can:

- See where a team stands **between** formal assessments, not only at phase gates
- Show **progress** over time (Level 2 to Level 3), rather than a pass/fail result
- Prepare teams for service assessments, and check readiness before a phase gate
- Go **beyond** the minimum the standard expects, with Levels 4–5

It **complements** GDS service assessments and does not replace them.

## 2. Design Principles

- **Content from the Service Standard, structure from CMMI.** Each of the 14 points is treated as a CMMI-style *practice area*, with an intent, links to CMMI practice areas, and level descriptors.
- **Local extension points.** The NHS adds 3 points to the GOV.UK standard; we add 3 of our own in the same way (points 15–17) to cover gaps that matter to us: running cost, the team's experience, and supply chain security. They're clearly marked so they're never confused with official GOV.UK points. GDS service assessments won't check them.
- **The team is the unit assessed.** It assesses the team running a service, in line with our CMMI adaptation approach.
- **Evidence from real work.** Ratings are based on what the team does and on data from its tools, not on documents written for the assessment.
- **Our own words.** Service Standard point titles are reproduced from the GOV.UK Service Manual (© Crown copyright, Open Government Licence v3.0). CMMI is used for its concepts and structure only; no CMMI text is reproduced.
- **UK first.** Where a point touches security, accessibility, or technology choices, it points to UK frameworks: NCSC CAF, UK Government Secure by Design, the Technology Code of Practice, and the accessibility regulations.

## 3. Maturity Levels

The same scale as [cmmi_adaptation_approach.md](cmmi_adaptation_approach.md), with a rough link to service assessment outcomes:

| Level | CMMI name | What it looks like for a team | Rough link to a service assessment |
|---|---|---|---|
| 0 | Incomplete | Not done at all, or only partly done, so the point's intent isn't achieved | **Not met**; expected only in discovery or very early alpha |
| 1 | Initial | Done inconsistently; depends on individuals | Likely **not met** |
| 2 | Managed | Agreed team practice, done consistently and tracked | Likely **met at alpha**; borderline at beta |
| 3 | Defined | Uses shared organizational standards and patterns, adapted on purpose | Likely **met at beta and live** |
| 4 | Quantitatively Managed | Managed using measures and targets; outcomes are predictable | **Beyond** what the assessment requires |
| 5 | Optimizing | Continuous, evidence-based improvement that spreads to other teams | **Exemplar**; others learn from the team |

**Rating rule (CMMI-style):** A team reaches a level for a point only when it meets the descriptor for that level **and all lower levels**.

**Level 0 and N/A:**

- **Level 0** means the point *applies* but the practice isn't being done, or only in fragments. It's a valid rating, not a failure, and it's normal for some points in discovery (e.g., point 14 before anything is running).
- **N/A** means the point genuinely doesn't apply, e.g., point 12 for a service with no new code. Record the reason. N/A points are left out of ratings and roll-ups.
- Level 0 is the same for every point, so the tables below start at Level 1. Rate a point **Level 0** when the team doesn't yet meet its Level 1 descriptor in a consistent way.

## 4. Structure of the Model

The 14 GOV.UK points and our 3 extension points (17 in total) are grouped into six **capability groups**, similar to CMMI's capability areas:

| Group | Service Standard points | Focus |
|---|---|---|
| **A. Users and needs** | 1–5 | Understanding users and designing services that work for everyone |
| **B. Team and ways of working** | 6–8 | How the team is built and how it delivers and improves |
| **C. Security and performance** | 9–10 | Protecting users and measuring success |
| **D. Technology** | 11–13 | Technology choices, openness, and reuse |
| **E. Operations** | 14 | Running a reliable service |
| **F. Local extensions** *(ours, not GOV.UK)* | 15–17 | Running cost, the team's experience, supply chain security |

Each point below has:

- **Intent:** what the point is for, in our words
- **CMMI v3.0 practice areas:** links to CMMI. *Check names against the licensed model.*
- **Our topic areas:** links to the team's 7 topic areas in [proposal.md](proposal.md) (section 4)
- **Related frameworks:** where to go for more detailed practice
- **Level descriptors and signals:** the evidence that supports each level

---

## 5. The Model

### Group A: Users and Needs

#### Point 1. Understand users and their needs

- **Intent:** The team bases decisions on direct, continuing research with real users, including people with access needs, not on assumptions.
- **CMMI:** Requirements Development & Management (RDM)
- **Our topic areas:** 6. Product & Requirements Management
- **Related frameworks:** GOV.UK Service Manual (user research), NHS Service Standard point 1

| Level | Descriptor | Signals |
|---|---|---|
| 1 | User needs are assumed by the team or stakeholders; little direct research | No research plan; needs not written down |
| 2 | The team researches regularly with real users, including people with access needs, and findings shape the backlog | Research plan and cadence; user needs recorded; backlog items trace to needs |
| 3 | Follows organizational research standards (ethics, consent, research repository); a user researcher is embedded | Findings in a shared repository; research ops standards followed |
| 4 | Research coverage and impact are measured; user needs are checked against outcome data | Share of features validated with users; needs linked to KPIs |
| 5 | Continuous discovery; insights are shared across services and research methods improve based on evidence | Cross-service insight sharing; changes to research methods |

#### Point 2. Solve a whole problem for users

- **Intent:** The team understands the user's whole journey, including other services, organizations, and channels, and works to solve the whole problem, not just its own part.
- **CMMI:** Requirements Development & Management (RDM), Strategic Service Management (STSM)
- **Our topic areas:** 6. Product & Requirements Management; 1. Engineering Strategy & Governance
- **Related frameworks:** GOV.UK Service Manual (whole problem, service design)

| Level | Descriptor | Signals |
|---|---|---|
| 1 | Scope is set by organizational boundaries; the wider journey isn't understood | No journey map; scope limited to one system |
| 2 | The end-to-end journey is mapped, and the team knows its scope and its dependencies on others | Journey map; dependency list; scope rationale recorded |
| 3 | Works with other teams and organizations to a shared service design approach; journey ownership is clear | Joint service design sessions; named owners along the journey |
| 4 | Journey-level measures (e.g., end-to-end completion, drop-off between services) are tracked | Journey dashboards spanning service boundaries |
| 5 | Shapes policy and the services of other organizations to remove friction for users | Changes upstream or in policy, influenced by the team |

#### Point 3. Provide a joined up experience across all channels

- **Intent:** Online, phone, paper, and face-to-face channels work together, and the team improves all of them, not only the digital one.
- **CMMI:** Service Delivery Management (SDM), Product Integration (PI)
- **Our topic areas:** 6. Product & Requirements Management; 4. Reliability, Observability & Incident Management (for operational channels)
- **Related frameworks:** GOV.UK Service Manual (channels); ITIL 4 (service desk, relationship management)

| Level | Descriptor | Signals |
|---|---|---|
| 1 | The digital channel is designed alone; offline channels are an afterthought | No contact with frontline or contact centre staff |
| 2 | Offline channels and assisted digital support are understood and designed for | Assisted digital plan; frontline staff involved in research |
| 3 | Consistent experience across channels, using shared organizational patterns; support and frontline feedback flows back to the team | Shared content and patterns; regular feedback loop from support teams |
| 4 | Channel use, channel shift, and failure demand are measured | Channel mix data; failure demand tracked |
| 5 | Channel design is optimized from evidence, and the lessons are shared across services | Channel improvements adopted by other services |

#### Point 4. Make the service simple to use

- **Intent:** Users can succeed first time, with no unnecessary steps. The team tests usability throughout and fixes problems.
- **CMMI:** Verification & Validation (VV), Requirements Development & Management (RDM)
- **Our topic areas:** 6. Product & Requirements Management; 2. Software Delivery & CI/CD (testing)
- **Related frameworks:** GOV.UK Design System; ISO/IEC 25010 (interaction capability)

| Level | Descriptor | Signals |
|---|---|---|
| 1 | Usability is judged by the team; little testing with users | No usability testing |
| 2 | Regular usability testing; problems are prioritized and fixed | Usability findings logged and fixed in sprints |
| 3 | Uses the GOV.UK (or NHS) Design System and organizational content standards; departs from them only with evidence | Design system components in use; content design reviews |
| 4 | Completion rate, time to complete, and error rate are tracked against targets | Analytics dashboards showing task success |
| 5 | Continuous experiments (e.g., A/B tests); improvements contributed back to the design system | Contributions to the design system; experiment log |

#### Point 5. Make sure everyone can use the service

- **Intent:** The service is accessible and inclusive, meeting **WCAG 2.2 AA** and the **Public Sector Bodies Accessibility Regulations 2018**, and works for people with low digital skills or confidence.
- **CMMI:** Verification & Validation (VV), Requirements Development & Management (RDM)
- **Our topic areas:** 6. Product & Requirements Management; 2. Software Delivery & CI/CD (automated checks)
- **Related frameworks:** WCAG 2.2; UK accessibility regulations; GOV.UK Service Manual (accessibility, assisted digital)

| Level | Descriptor | Signals |
|---|---|---|
| 1 | Accessibility checked late or not at all | No audit; no accessibility statement |
| 2 | Accessibility built into the definition of done; manual testing including assistive technology; accessibility statement published | Assistive technology test records; accessibility statement |
| 3 | Automated accessibility checks in CI; regular independent audits; follows organizational accessibility standards | CI accessibility checks; audit reports; issues fixed |
| 4 | Accessibility defects and fix times tracked; research includes disabled users with set targets | Accessibility defect trend; research participation data |
| 5 | Recognized for inclusive practice; patterns and tools shared with others | Accessibility patterns contributed and reused |

### Group B: Team and Ways of Working

#### Point 6. Have a multidisciplinary team

- **Intent:** A stable team with the right mix of skills (product, delivery, user research, design, engineering, and others), including decision-makers, for the life of the service.
- **CMMI:** Workforce Empowerment (WE), Organizational Training (OT), Planning (PLAN)
- **Our topic areas:** 5. Platform & Developer Experience (people); 1. Engineering Strategy & Governance (recruitment)
- **Related frameworks:** UK Government DDaT Capability Framework; SPACE / DevEx; DORA (culture)

| Level | Descriptor | Signals |
|---|---|---|
| 1 | Missing key roles; heavy reliance on individuals; high turnover | Role gaps; single points of knowledge |
| 2 | All key roles filled; clear responsibilities; knowledge is shared within the team | Team chart with roles; handover and knowledge-sharing practice |
| 3 | Roles follow the DDaT Capability Framework; skills plans and career paths in place; a balanced mix of permanent staff and contractors | DDaT role profiles; skills matrix; training plans |
| 4 | Team health and capability are measured (e.g., developer experience or team health surveys) and acted on | Survey trends; actions taken |
| 5 | The team develops people for the wider organization; its practices are a model for others | Rotation and mentoring programmes; practices adopted elsewhere |

#### Point 7. Use agile ways of working

- **Intent:** Work is delivered in small, iterative steps with frequent feedback. Governance adapts to agile delivery.
- **CMMI:** Planning (PLAN), Monitor & Control (MC), Estimating (EST), Process Management (PCM)
- **Our topic areas:** 2. Software Delivery & CI/CD; 1. Engineering Strategy & Governance (governance burden)
- **Related frameworks:** GOV.UK Service Manual (agile delivery); DORA (small batches, visibility of work)

| Level | Descriptor | Signals |
|---|---|---|
| 1 | Large, infrequent releases; plans fixed up front; governance designed for waterfall | Phase-gate plans; big-bang releases |
| 2 | The team follows an agreed agile cadence (planning, show and tells, retrospectives) and visible backlog | Regular ceremonies; visible board; show and tell notes |
| 3 | Organizational agile governance in place: proportionate, light assurance and delegated decisions | Governance by show and tell or outcome reviews; few separate approval boards |
| 4 | Flow is measured (lead time, work in progress, predictability) and used for planning | Flow metrics; forecasts based on data |
| 5 | The team experiments with its ways of working and shares what works | Experiments recorded; practices adopted by others |

#### Point 8. Iterate and improve frequently

- **Intent:** The team can change the service often and safely, in response to user feedback and data, throughout its life, not only before launch.
- **CMMI:** Causal Analysis & Resolution (CAR), Managing Performance & Measurement (MPM), Configuration Management (CM)
- **Our topic areas:** 2. Software Delivery & CI/CD
- **Related frameworks:** DORA metrics and capabilities; GOV.UK Service Manual (iteration in live)

| Level | Descriptor | Signals |
|---|---|---|
| 1 | Changes are slow and risky; improvements stop once the service is live | Infrequent releases; no funding for live iteration |
| 2 | Automated build and deployment; feedback drives a regular stream of improvements | CI/CD pipeline; changes linked to user feedback |
| 3 | Organizational pipeline standards and golden paths; continuous improvement funded throughout the service's life | Standard pipeline in use; funding model for live service |
| 4 | DORA metrics tracked with targets; improvement impact measured | DORA dashboard; before and after measures |
| 5 | Continuous delivery with progressive release (feature flags, canary releases); lessons shared | Progressive delivery in use; patterns shared with others |

### Group C: Security and Performance

#### Point 9. Create a secure service which protects users' privacy

- **Intent:** Security and privacy risks are understood and managed throughout delivery, in line with UK guidance and law.
- **CMMI:** Enabling Security (ESEC), Managing Security Threats & Vulnerabilities (MST), Risk & Opportunity Management (RSK)
- **Our topic areas:** 3. Security & Secure SDLC
- **Related frameworks:** **NCSC CAF** (research.md 3.20); **UK Government Secure by Design**; UK GDPR and data protection impact assessments (DPIAs); NIST SSDF and OWASP SAMM (secure development practice)

| Level | Descriptor | Signals |
|---|---|---|
| 1 | Security considered late (e.g., a penetration test before launch only); privacy handled ad hoc | No threat model; no DPIA |
| 2 | Threat modelling and a DPIA done; security requirements in the backlog; dependency and code scanning in CI | Threat model; DPIA; scan results acted on |
| 3 | Follows organizational secure development and Secure by Design standards; contributing outcomes for the relevant CAF profile are met | Secure by Design self-assessment; CAF outcomes evidenced; regular penetration testing |
| 4 | Vulnerability fix times, scan coverage, and security incidents tracked against targets | Security metrics dashboard; fix times within policy |
| 5 | Security improves proactively (e.g., threat hunting, removing whole classes of vulnerability); learning shared | Classes of vulnerability eliminated; contributions to security patterns |

#### Point 10. Define what success looks like and publish performance data

- **Intent:** The team defines measurable outcomes, tracks them, publishes performance data where required, and uses it to make decisions.
- **CMMI:** Managing Performance & Measurement (MPM), Monitor & Control (MC)
- **Our topic areas:** 2. Software Delivery & CI/CD (metrics and measurement); 6. Product & Requirements Management
- **Related frameworks:** GOV.UK Service Manual (measuring success, e.g., cost per transaction, user satisfaction, completion rate, digital take-up); DORA; SPACE

| Level | Descriptor | Signals |
|---|---|---|
| 1 | Success not defined; little data collected | No KPIs; analytics missing or unused |
| 2 | KPIs defined and tracked, including the GOV.UK mandatory or recommended measures where they apply | KPI list; performance dashboard |
| 3 | Organizational measurement standards and tooling; performance data published where required | Shared analytics setup; published data |
| 4 | Targets set and reviewed; decisions demonstrably driven by data | Targets in roadmaps; decision records cite data |
| 5 | Measures themselves are refined; benchmarks and insights shared across services | Measurement improvements; benchmarking across services |

### Group D: Technology

#### Point 11. Choose the right tools and technology

- **Intent:** Technology choices are made on evidence, avoid lock-in, give value for money, and are reviewed as needs change.
- **CMMI:** Decision Analysis & Resolution (DAR), Technical Solution (TS), Supplier Agreement Management (SAM)
- **Our topic areas:** 1. Engineering Strategy & Governance; 7. FinOps
- **Related frameworks:** **Technology Code of Practice**; Well-Architected Frameworks; FinOps (research.md 3.11, 3.17)

| Level | Descriptor | Signals |
|---|---|---|
| 1 | Technology chosen by habit or by a supplier; no recorded rationale | No decision records |
| 2 | Choices recorded with their rationale (e.g., architecture decision records), options compared, and exit strategy considered | Decision records; options appraisal |
| 3 | Follows organizational technology standards and the Technology Code of Practice; regular architecture reviews | Technology radar or standards used; Well-Architected reviews |
| 4 | Total cost of ownership, unit cost, and technical health (e.g., tech debt, run cost) tracked | Cost per transaction; tech debt register with trends |
| 5 | Technology choices continually re-evaluated; findings shape organizational standards | Contributions to the tech radar or standards |

#### Point 12. Make new source code open

- **Intent:** New source code is developed in the open and reusable by others by default, with clear and justified exceptions.
- **CMMI:** Configuration Management (CM), Governance (GOV)
- **Our topic areas:** 3. Security & Secure SDLC (safe publishing, supply chain); 2. Software Delivery & CI/CD
- **Related frameworks:** Technology Code of Practice (open source); GOV.UK Service Manual (making source code open); SLSA and SBOMs (research.md 3.9, 3.10)

| Level | Descriptor | Signals |
|---|---|---|
| 1 | Code is closed by default; reasons not recorded | Private repositories with no recorded justification |
| 2 | Code is open by default, with a licence and README; exceptions (e.g., fraud rules) recorded | Public repositories; licence; exception log |
| 3 | Follows organizational open source policy: secret scanning, safe publishing, contribution guidance | Secret scanning; CONTRIBUTING files; policy compliance |
| 4 | Openness and reuse measured (e.g., share of repositories open, external reuse, contributions) | Openness and reuse metrics |
| 5 | Actively maintained shared code that other organizations reuse and contribute to | External contributors; reuse by other organizations |

#### Point 13. Use and contribute to open standards, common components and patterns

- **Intent:** The team reuses common platforms, components, patterns, and open standards rather than building its own, and contributes improvements back.
- **CMMI:** Process Asset Development (PAD), Technical Solution (TS), Product Integration (PI)
- **Our topic areas:** 5. Platform & Developer Experience
- **Related frameworks:** GOV.UK Design System; common platforms such as GOV.UK Notify, GOV.UK Pay, and GOV.UK One Login; open standards (Open Standards Board); CNCF Platform Maturity Model (research.md 3.15)

| Level | Descriptor | Signals |
|---|---|---|
| 1 | Components built from scratch; open standards not considered | Custom components that duplicate common platforms |
| 2 | Uses common components and open standards where available; choices to build bespoke are justified | Common platforms in use; build-vs-reuse decisions recorded |
| 3 | Organizational golden paths and shared components adopted by default | Reuse of platform templates and shared libraries |
| 4 | Level of reuse and the cost of bespoke components measured | Reuse metrics; bespoke maintenance cost tracked |
| 5 | The team contributes components and patterns that others adopt | Contributions merged into shared platforms or design systems |

### Group E: Operations

#### Point 14. Operate a reliable service

- **Intent:** The service is available, monitored, resilient, and recoverable. Incidents are handled well and learned from.
- **CMMI:** Incident Resolution & Prevention (IRP), Continuity (CONT), Service Delivery Management (SDM), Causal Analysis & Resolution (CAR)
- **Our topic areas:** 4. Reliability, Observability & Incident Management
- **Related frameworks:** Site Reliability Engineering (3.12); ITIL 4 (3.24); NCSC CAF objectives C and D (3.20); Well-Architected Reliability pillar

| Level | Descriptor | Signals |
|---|---|---|
| 1 | Outages found by users; recovery ad hoc; on-call unclear | No monitoring or alerting; no runbooks |
| 2 | Monitoring and alerting, on-call rota, runbooks, and incident process in place; backups tested | Alerts; on-call rota; incident log; restore test record |
| 3 | Organizational incident and problem management in use; blameless post-incident reviews; continuity and disaster recovery plans tested | Post-incident reviews with completed actions; DR test reports |
| 4 | SLOs and error budgets set and used to balance reliability against change; recovery time and availability tracked | SLO dashboards; error budget policy |
| 5 | Proactive resilience (e.g., chaos testing, game days); reliability lessons shared across services | Game day reports; shared reliability patterns |

### Group F: Local Extensions *(our points, not part of the GOV.UK Service Standard)*

#### Point 15. Manage the cost of running the service

- **Intent:** The team understands and takes ownership of the cost of running its service (cloud, licences, third-party services), relates it to the value delivered, and keeps improving it.
- **Why we added it:** Point 11 mentions value for money, but no GOV.UK point covers ongoing running cost. This fills the FinOps gap.
- **CMMI:** Managing Performance & Measurement (MPM), Planning (PLAN), Estimating (EST)
- **Our topic areas:** 7. FinOps; 1. Engineering Strategy & Governance
- **Related frameworks:** FinOps Framework and Maturity Model (research.md 3.17); Well-Architected Cost and Sustainability pillars (3.11); Technology Code of Practice (value for money); GOV.UK cost per transaction

| Level | Descriptor | Signals |
|---|---|---|
| 1 | The team doesn't know its running costs; bills are handled centrally and arrive as a surprise | No cost visibility at team level |
| 2 | The team can see its own costs; resources are tagged; budgets and alerts are set (FinOps *Crawl*) | Tagging policy applied; budget alerts; monthly cost review |
| 3 | Follows organizational FinOps standards; cost is part of design and planning decisions; a unit cost (e.g., cost per transaction) is defined (FinOps *Walk*) | Unit cost metric; cost noted in decision records |
| 4 | Unit cost targets set and tracked; costs forecast; optimizations (rightsizing, scheduling, commitments) measured (FinOps *Run*) | Cost per transaction trend; forecast accuracy; savings log |
| 5 | Optimization is automated; architecture is cost- and carbon-aware; savings and patterns shared across services | Automated rightsizing; carbon metrics; patterns adopted by others |

#### Point 16. Look after the team and its ways of working

- **Intent:** The team works at a sustainable pace with psychological safety, has a good developer experience (fast feedback, manageable cognitive load, time for focused work), and keeps learning.
- **Why we added it:** Point 6 covers the team's *make-up* (roles and skills) but not its *health and experience*, which DORA and SPACE research show drive delivery performance.
- **CMMI:** Workforce Empowerment (WE), Organizational Training (OT), Process Management (PCM), Causal Analysis & Resolution (CAR)
- **Our topic areas:** 5. Platform & Developer Experience (people)
- **Related frameworks:** SPACE and DevEx (research.md 3.3); DORA (Westrum culture, wellbeing) (3.2); CNCF Platform Engineering Maturity Model (3.15)

| Level | Descriptor | Signals |
|---|---|---|
| 1 | Friction and overload are tolerated; signs of burnout; retrospectives rarely lead to change | Long hours; retrospective actions not completed |
| 2 | Regular retrospectives with actions completed; sustainable on-call and working patterns; an onboarding guide | Retro action completion; on-call load reviewed; onboarding time |
| 3 | Uses organizational developer experience standards, golden paths, and protected learning time; psychological safety discussed openly | Org DevEx survey taken part in; golden paths in use; learning time in plans |
| 4 | Developer experience measured (e.g., build and review wait times, flow, survey scores) with targets | DevEx dashboard; trends acted on |
| 5 | The team experiments to improve its own experience and shares what works; feeds back into platform improvements | Experiments recorded; practices adopted by other teams |

#### Point 17. Secure the software supply chain

- **Intent:** The team knows and can trust everything that goes into the service (open source dependencies, build tools, third-party components, and suppliers) and can quickly tell whether a new vulnerability affects it.
- **Why we added it:** Point 9 covers security broadly. Supply chain attacks deserve a point of their own, in line with NCSC CAF principle A4 (Supply Chain).
- **CMMI:** Supplier Agreement Management (SAM), Configuration Management (CM), Managing Security Threats & Vulnerabilities (MST)
- **Our topic areas:** 3. Security & Secure SDLC
- **Related frameworks:** SLSA (research.md 3.9); SP 800-161r1 and SBOM guidance (3.10); NCSC CAF A4 (3.20); NIST SSDF Protect the Software group (3.4)

| Level | Descriptor | Signals |
|---|---|---|
| 1 | Dependencies aren't tracked; there's no inventory; builds may run on developers' machines | No dependency scanning; artifacts can't be traced to source |
| 2 | Dependency scanning and automated updates; lockfiles; all builds in CI; an SBOM generated for each release (about SLSA L1) | Dependency scanning alerts handled; SBOM stored with each release |
| 3 | Follows organizational supply chain standards: approved registries or mirrors, signed provenance from a hosted build platform (SLSA L2), suppliers' security assessed (CAF A4) | Provenance attestations; approved registry use; supplier assessments |
| 4 | Fix times for critical dependency vulnerabilities, SBOM coverage, and the share of artifacts with verified provenance are tracked against targets; "are we affected?" answered within hours | Supply chain metrics dashboard; incident response times for new vulnerabilities |
| 5 | Hardened builds (SLSA L3); provenance checked before deploy; the team contributes fixes upstream to open source it depends on | Deploy-time policy checks; upstream contributions |

---

## 6. Expected Levels by Delivery Phase

A suggested **minimum** level for each point at each phase, to help teams prepare for service assessments. Discovery isn't formally assessed by GDS, but we include it as a guide, because this is where Level 0 is expected for points that don't apply yet.

| Point | Discovery | Alpha | Beta | Live |
|---|---|---|---|---|
| 1. Understand users and their needs | 2 | 2 | 3 | 3 |
| 2. Solve a whole problem for users | 2 | 2 | 2 | 3 |
| 3. Joined up experience across all channels | 1 | 2 | 2 | 3 |
| 4. Make the service simple to use | 0 | 2 | 3 | 3 |
| 5. Make sure everyone can use the service | 1 | 2 | 3 | 3 |
| 6. Have a multidisciplinary team | 2 | 2 | 3 | 3 |
| 7. Use agile ways of working | 1 | 2 | 3 | 3 |
| 8. Iterate and improve frequently | 0 | 2 | 3 | 3 |
| 9. Secure service which protects privacy | 1 | 2 | 3 | 3 |
| 10. Define success and publish performance data | 1 | 2 | 2 | 3 |
| 11. Choose the right tools and technology | 0 | 2 | 3 | 3 |
| 12. Make new source code open | 0 | 2 | 2 | 3 |
| 13. Use and contribute to common components | 1 | 2 | 3 | 3 |
| 14. Operate a reliable service | 0 | 1 | 2 | 3 |
| *15. Manage the cost of running the service (ext.)* | 1 | 1 | 2 | 3 |
| *16. Look after the team (ext.)* | 1 | 2 | 2 | 3 |
| *17. Secure the software supply chain (ext.)* | 0 | 2 | 3 | 3 |

**Reading the table:**

- **0 in discovery** means the point isn't expected yet; it isn't a gap. Discovery should still consider points 3, 5, 9, 10, 13, and 15 lightly (Level 1), e.g., channels, access needs, privacy, success measures, existing components, and the rough cost of options.
- Level 3 at live is the baseline. Levels 4–5 are where we want to go beyond what the standard requires, especially for **points 8, 10, and 14**, where measurement (DORA, SLOs) gives the biggest benefit.

## 7. Organizational Enablers

As in our CMMI adaptation, **Level 3 needs organizational support**. Teams can't reach it alone. The organization needs to provide:

| Enabler | Supports points |
|---|---|
| User research operations: ethics, consent, recruitment, research repository | 1, 2, 4, 5 |
| Use of the GOV.UK or NHS Design System, plus content standards | 3, 4, 5, 13 |
| Accessibility testing tools and audit capability | 5 |
| DDaT-aligned roles, career paths, and training | 6 |
| Agile governance and assurance that is proportionate to risk (no unnecessary approval boards) | 7, 8 |
| Standard CI/CD pipeline and golden paths | 8, 12, 13 |
| Secure by Design standards, security tooling, CAF profile and assurance | 9 |
| Analytics tooling and measurement standards | 10 |
| Technology standards, tech radar, architecture review | 11 |
| Open source policy and safe publishing tools (secret scanning) | 12 |
| Shared platforms and components | 13 |
| Observability platform, incident and problem management process, DR capability | 14 |
| FinOps tooling, cost allocation and tagging standards, cost data available to teams | 15 |
| Organizational developer experience survey, platform team, protected learning time | 16 |
| Approved package registries, SBOM tooling, hosted CI with signed provenance, supplier assessment process | 17 |

## 8. Assessment Method

It follows the **GDS service assessment** model, with the peer validation used by the **NHS Digital Maturity Assessment**:

1. **Self-assessment:** the team rates each point using the descriptors and gathers signals, ideally pulled from tools (around 2 hours).
2. **Peer panel:** a small multidisciplinary panel (e.g., delivery, user research or design, engineering, and security or operations), drawn from outside the team, reviews the evidence with the team in a 90-minute session.
3. **Agreed rating:** a level for each point, plus a **profile by capability group**.
4. **Outcome:** 2–3 improvement goals, and readiness against the phase table (section 6) if a service assessment is coming up.

**Reporting:**

- Report a **profile** (a level for each point), not a single overall number.
- If a single rating is needed, use the CMMI staged rule: **the lowest level achieved across all applicable points**, leaving out N/A points.
- Report the 14 GOV.UK points and the 3 extension points **separately**, so readiness for a service assessment is clear.
- As with the wider model, results are for **improvement, not ranking teams**.

## 9. Mapping to Our Topic Areas

How well the Service Standard covers the team's 7 topic areas (from [proposal.md](proposal.md), section 4):

| Our topic area | GOV.UK points | Extension points | Coverage |
|---|---|---|---|
| 1. Engineering Strategy & Governance | 2, 7, 11 | 15 | **Partial.** Agile governance, technology choices, and cost ownership are covered; engineering strategy and recruitment only through point 6 |
| 2. Software Delivery & CI/CD | 7, 8, 10, 12 | — | **Good.** Add DORA metrics for depth |
| 3. Security & Secure SDLC | 9, 12 | 17 | **Good** with point 17. Detailed secure development practice comes from NCSC CAF, Secure by Design, and SSDF |
| 4. Reliability, Observability & Incident Management | 14 | — | **Good** at outcome level. Add SRE and ITIL for practice |
| 5. Platform & Developer Experience | 6, 13 | 16 | **Good** with point 16 |
| 6. Product & Requirements Management | 1–5, 10 | — | **Strong.** The core of the Service Standard |
| 7. FinOps | 11 (value for money) | 15 | **Good** with point 15 |

**Remaining gap:** engineering strategy and recruitment (topic area 1) is still only partly covered. It could become a fourth extension point later, or be assessed separately at organizational level.

### NHS work

For NHS services, also include the **three NHS Service Standard points**: support a culture of care, make your service clinically safe (DCB0129/DCB0160), and make your service interoperable. They would form a further group alongside our extensions, giving 20 points in total.

## 10. Open Questions

1. For NHS work, do we add the **three NHS points** to our 17 (20 in total), or use the NHS Service Standard on its own?
2. Are the **phase expectations** (section 6) right, including discovery, or too demanding for alpha?
3. Who sits on **peer panels**? Could we reuse people already trained as GDS or departmental service assessors?
4. Should Level 4–5 descriptors be **left more open** until we've piloted Levels 0–3?
5. Should the **extension points** carry the same weight as GOV.UK points in single ratings, or be reported only as a separate profile?
6. Is a fourth extension point needed for **engineering strategy and recruitment**?

## References

- GOV.UK Service Standard: https://www.gov.uk/service-manual/service-standard
- NHS Service Standard: https://service-manual.nhs.uk/standards-and-technology/service-standard
- GOV.UK Service Manual: https://www.gov.uk/service-manual
- GOV.UK Design System: https://design-system.service.gov.uk
- Technology Code of Practice: https://www.gov.uk/guidance/the-technology-code-of-practice
- UK Government Secure by Design: https://www.security.gov.uk/policy-and-guidance/secure-by-design/
- NCSC Cyber Assessment Framework: https://www.ncsc.gov.uk/collection/cyber-assessment-framework
- WCAG 2.2: https://www.w3.org/TR/WCAG22/
- Public Sector Bodies Accessibility Regulations: https://www.gov.uk/guidance/accessibility-requirements-for-public-sector-websites-and-apps
- DDaT Capability Framework: https://ddat-capability-framework.service.gov.uk
- FinOps Framework: https://www.finops.org/framework/
- SLSA: https://slsa.dev
- CMMI: https://cmmiinstitute.com/cmmi
- DORA: https://dora.dev
- Other frameworks: see [research.md](research.md)
