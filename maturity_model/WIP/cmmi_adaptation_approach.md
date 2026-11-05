# Adapting CMMI for Software Engineering Teams: Approach

*Draft v0.1 for team discussion, November 2026. Companion to [proposal.md](proposal.md)*

## 1. Purpose

CMMI is the most widely recognized maturity model in industry and government. But it was designed to appraise **whole organizations**, and it leans on documented process and formal appraisals. We want something lighter, aimed at **engineering teams**. It should keep CMMI's structure and credibility and describe practice in terms of modern software delivery (DevOps, CI/CD, SRE, platform engineering).

This document sets out how we could do that: what we keep from CMMI, what we change, how the pieces fit together, and how we'd roll it out.

## 2. Adopt vs. Adapt

| | Keep from CMMI | Adapt for teams | Leave out (for now) |
|---|---|---|---|
| **Structure** | Maturity levels; practice areas grouped into capability areas; each area has an intent and a value statement | Group practice areas under our 7 topic areas | CMMI's full capability-area taxonomy |
| **Unit of assessment** | — | The **team** (a product or service team), not the organization | Organization-wide maturity rating |
| **Evidence** | The idea that maturity must be shown, not claimed | Outcomes and metrics (DORA, SLOs) plus lightweight artifacts already in our tools | Heavy process documentation for the sake of compliance |
| **Assessment** | Repeatable, consistent method | Facilitated **self-assessment** workshop | Formal CMMI appraisal (it needs a certified Lead Appraiser and gives an official rating) |
| **Practices** | Practice intent, e.g. "manage requirements", "verify and validate" | Rewritten in team language, with modern practices as examples | Supplier selection, contract management, and other org/procurement areas |

**Two important caveats:**
- **Copyright:** the CMMI model text belongs to ISACA. We can use its *concepts and structure* and cite it. We should not reproduce practice statements word for word without a license. Check with legal or procurement before we distribute the model widely.
- **No official rating:** our adapted model gives us an *internal* view of maturity. It can't be used to claim a CMMI maturity level. If we ever need one (e.g., for government contracts), the model can be our stepping stone toward a formal appraisal.

## 3. Maturity Levels, Reinterpreted for Teams

| Level | CMMI name | What it looks like for a team |
|---|---|---|
| 1 | Initial | Work gets done, but how depends on who's doing it. Results vary; knowledge sits with individuals. |
| 2 | Managed | The team has agreed ways of working, follows them consistently, and tracks its work. |
| 3 | Defined | The team uses shared organizational standards and golden paths, adapts them on purpose, and contributes improvements back. |
| 4 | Quantitatively Managed | The team sets targets using metrics (DORA, SLOs, cost) and can predict its delivery and reliability. |
| 5 | Optimizing | The team runs improvement experiments, measures the effect, and the wins spread to other teams. |

**Note:** Levels 3 and above depend on the **organization** providing shared standards, platforms, and data. A team can't reach Level 3 alone. The model should therefore also track a small set of org-level enablers (see section 8).

## 4. Mapping CMMI Practice Areas to Our Topic Areas

The 7 topic areas come from the team's list in the proposal. The practice areas below are from CMMI v3.0; check them against the licensed model during design. "Overlay" means the external framework we use to give the area concrete, modern practices.

| # | Topic area | CMMI v3.0 practice areas drawn on | Overlay frameworks |
|---|---|---|---|
| 1 | **Engineering Strategy & Governance** | Governance (GOV), Implementation Infrastructure (II), Risk & Opportunity Management (RSK), Decision Analysis & Resolution (DAR), Planning (PLAN) | NIST CSF 2.0 (Govern). Aim: *lightweight* governance that reduces approval and CAB burden |
| 2 | **Software Delivery & CI/CD** | Technical Solution (TS), Product Integration (PI), Configuration Management (CM), Verification & Validation (VV), Peer Reviews (PR), Managing Performance & Measurement (MPM) | DORA metrics and capabilities, DoD DevSecOps Fundamentals |
| 3 | **Security & Secure SDLC** | Enabling Security (ESEC), Managing Security Threats & Vulnerabilities (MST), Supplier Agreement Management (SAM) for dependencies | NIST SSDF, CISA Secure by Design, OWASP SAMM, SLSA |
| 4 | **Reliability, Observability & Incident Management** | Incident Resolution & Prevention (IRP), Continuity (CONT), Causal Analysis & Resolution (CAR) | Google SRE, Well-Architected (Reliability, Ops Excellence) |
| 5 | **Platform, Developer Experience & People** | Process Asset Development (PAD) for golden paths and templates, Process Management (PCM), Organizational Training (OT), Workforce Empowerment (WE) | CNCF Platform Maturity Model, SPACE / DevEx, DORA culture |
| 6 | **Product & Requirements Management** | Requirements Development & Management (RDM), Estimating (EST), Planning (PLAN), Monitor & Control (MC) | ISO/IEC/IEEE 12207 |
| 7 | **FinOps** | Managing Performance & Measurement (MPM). There's no direct CMMI area | FinOps Maturity Model: Crawl ≈ L2, Walk ≈ L3, Run ≈ L4+ |

## 5. How Each Topic Area Is Described

Each area uses the same short template:

- **Intent:** one sentence on what the area is for
- **Value:** why it matters to the team and the business
- **Level descriptors:** 1–3 bullets per level (L1–L5), in plain team language
- **Signals and evidence:** metrics or artifacts that support a rating, ideally pulled from tools we already use
- **Overlay references:** where to go for detailed practice

**Worked example: Software Delivery & CI/CD (illustrative only)**

| Level | Descriptor | Signals |
|---|---|---|
| 1 | Builds and deploys are partly manual; releases are risky, infrequent events | Releases monthly or less often; deploys take a lot of manual work |
| 2 | All code is in version control with peer review; CI runs on every change; deployment is scripted | CI pass rate is tracked; review is required on main |
| 3 | Uses the org's standard pipeline and golden path; automated tests and security scans gate releases | Pipeline template in use; agreed definition of done |
| 4 | DORA metrics are tracked, with team targets; release outcomes are predictable | Deployment frequency, lead time, change fail rate, and recovery time are on a dashboard |
| 5 | The team experiments to improve flow (e.g., trunk-based development, progressive delivery) and shares the results | Measured improvement over time; practices adopted by other teams |

## 6. Assessment Method

- **Format:** a 60–90 minute facilitated workshop per team, run by a facilitator from outside the team.
- **Inputs:** the team's metrics (pulled in beforehand where possible) and a short pre-read questionnaire.
- **Scoring:** the team agrees a level for each topic area. Evidence supports the rating but doesn't need to be exhaustive.
- **Outputs:** a heatmap of levels by area, plus **2–3 improvement goals** the team owns for the next cycle.
- **Calibration:** facilitators compare ratings across teams periodically, so levels mean the same thing everywhere.
- **Ground rule:** the model is for **improvement, not ranking teams or measuring individual performance**. If it's used to judge teams, ratings will be inflated and metrics gamed (Goodhart's law).

## 7. Rollout Phases

| Phase | What happens | Output |
|---|---|---|
| **0. Set up** | Confirm the topic areas, name an owner for each area, check CMMI licensing | Agreed scope and owners |
| **1. Design** | Area owners draft intent, value, level descriptors, and signals using the template | Draft model v0.5 |
| **2. Pilot** | Assess 2–3 volunteer teams that differ from each other | Pilot results and feedback |
| **3. Calibrate** | Revise wording and levels based on the pilot; simplify where it was confusing | Model v1.0 and facilitator guide |
| **4. Roll out** | Expand to all teams in waves; train facilitators | Baseline heatmap across teams |
| **5. Sustain** | Reassess every 6 months; owners refine their areas once a year | Trends over time; improvement backlog |

## 8. Roles

- **Executive sponsor:** backs the initiative and removes org-level blockers.
- **Model owner:** keeps the model coherent and runs the overall cadence.
- **Topic area owners (one per area):** own the content for their area and support teams in it.
- **Facilitators:** run assessments and calibrate ratings.
- **Teams:** assess themselves honestly and own their improvement goals.
- **Org-level enablers:** platform, security, and FinOps functions that provide the shared standards teams need to reach Level 3 and above.

## 9. Risks and Mitigations

| Risk | Mitigation |
|---|---|
| Becomes a box-ticking compliance exercise | Rate on outcomes and metrics, not documents; keep the template short |
| Used to rank or punish teams | State the ground rule up front; report org trends, not team league tables |
| Teams get stuck at L2 because org support is missing | Track org-level enablers alongside team ratings |
| Ratings vary between facilitators | Calibration sessions; worked examples for each area |
| CMMI copyright or licensing issues | Use concepts, cite the source, rewrite text in our own words; check with legal |
| Metrics get gamed | Use several metrics together (e.g., throughput *and* stability); keep them for improvement only |

## 10. Open Questions

1. Should the model include **Level 0 (Incomplete)** as CMMI v3.0 does, or start at Level 1?
2. Will we ever need a **formal CMMI appraisal** (e.g., for government work)? If so, we should keep a closer mapping to CMMI.
3. Does the **people/culture** content stay inside Platform & DevEx, or become its own area?
4. Which **2–3 teams** should pilot?
5. Where will results live: a spreadsheet, an internal tool, or a dashboard?

## References

- CMMI (ISACA / CMMI Institute): https://cmmiinstitute.com/cmmi
- DORA: https://dora.dev
- Overlay frameworks: see the References section in [proposal.md](proposal.md)
