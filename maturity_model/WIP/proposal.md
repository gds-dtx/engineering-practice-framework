# Engineering Maturity Model: Proposed Topic Areas

*Draft v0.1 for team discussion, November 2026*

## 1. Purpose and Approach

We want a shared, repeatable way to see where our engineering practices stand today, decide where to invest, and track progress. We won't invent a model from scratch. We'll **borrow from established industry and government frameworks**: they give us credible structure, common vocabulary, and benchmarks we can compare against. This document proposes the **topic areas** the model should cover and names the frameworks behind each one. It is a starting point, not a final design; detail will come as we go.

## 2. Proposed Maturity Scale

Adapted from the CMMI levels so we use language others recognize:

| Level | Name | In short |
|---|---|---|
| 1 | **Initial** | Ad hoc; results depend on individual heroics |
| 2 | **Managed** | Practices exist at team level and are planned and tracked |
| 3 | **Defined** | Standard practices across the organization, documented and consistent |
| 4 | **Quantitatively Managed** | Managed with metrics; performance is predictable |
| 5 | **Optimizing** | Continuous, data-driven improvement and innovation |

*Option to consider:* some areas (e.g., FinOps, SAMM) use their own scales. We can map those onto the scale above instead of using several scales.

## 3. Proposed Topic Areas - AI Assisted

| # | Topic area | Scope (high level) | Primary influences |
|---|---|---|---|
| 1 | **Engineering Strategy & Governance** | Engineering vision, decision rights, standards, policy, risk oversight | CMMI (Governance), NIST CSF 2.0 (Govern) |
| 2 | **Software Delivery & CI/CD** | Version control, build/test/deploy automation, release practices, deployment frequency | DORA, DoD DevSecOps Fundamentals |
| 3 | **Code Quality & Testing** | Code review, test automation and coverage strategy, static analysis, definition of done | ISO/IEC 25010, CMMI (Verification & Validation), DORA (test automation) |
| 4 | **Architecture** | Architecture decisions and records, modularity, scalability, tracking and paying down tech debt | Well-Architected Frameworks, ISO/IEC 25010 |
| 5 | **Security & Secure SDLC** | Threat modeling, secure coding, vulnerability management, security testing | NIST SSDF, OWASP SAMM, BSIMM, CISA Secure by Design |
| 6 | **Software Supply Chain** | Dependency management, SBOMs, build provenance, third-party risk | SLSA, NIST SP 800-161r1, CISA SBOM guidance |
| 7 | **Reliability, Observability & Incident Management** | SLOs, monitoring and alerting, on-call, incident response, blameless postmortems | Google SRE, Well-Architected (Reliability, Operational Excellence) |
| 8 | **Platform & Developer Experience** | Internal developer platform, self-service, golden paths, onboarding, cognitive load | CNCF Platform Maturity Model, SPACE / DevEx |
| 9 | **Engineering Metrics & Measurement** | Which metrics we track, dashboards, how we use data to make decisions | DORA metrics, SPACE, CMMI Levels 4–5 |
| 10 | **Product & Requirements Management** | Discovery, requirements, prioritization, traceability, feedback loops | CMMI (Requirements Development & Management), ISO/IEC/IEEE 12207 |
| 11 | **Cloud & Cost Management** | Cloud usage, cost visibility and accountability, efficiency, sustainability | FinOps Maturity Model, Well-Architected (Cost, Sustainability) |
| 12 | **People, Culture & Continuous Improvement** | Learning culture, psychological safety, career growth, knowledge sharing, retrospectives | DORA (Westrum culture), CMMI (Optimizing) |
| 13 | **AI in Engineering** *(emerging / optional)* | AI-assisted development practices, governance of AI features, model risk | NIST AI RMF, ISO/IEC 42001, DORA AI Capabilities research |

## 4. Proposed topic areas - Aran

| # | Topic area | Scope (high level) | Notes |
|---|---|---|---|
| 1 | **Engineering Strategy & Governance** | Engineering vision, decision rights, standards, policy, risk oversight | Strategy, recruitment,Governance burden, CAB boards, risk oversight seem key|
| 2 | **Software Delivery & CI/CD** | Version control, build/test/deploy automation, release practices, deployment frequency. Code review, test automation and coverage strategy, static analysis, definition of done | How the team and individual work, including quant data on metrics and measurement|
| 3 | **Security & Secure SDLC** | Threat modeling, secure coding, vulnerability management, security testing, supply chain, Dependency management | CISA Secure by Design adherance|
| 4 | **Reliability, Observability & Incident Management** | SLOs, monitoring and alerting, on-call, incident response, blameless postmortems | Post Build stuff |
| 5 | **Platform & Developer Experience** | Internal developer platform, self-service, golden paths, onboarding, cognitive load. Learning culture, psychological safety, career growth, knowledge sharing, retrospectives | People stuff |
| 6 | **Product & Requirements Management** | Discovery, requirements, prioritization, traceability, feedback loops | CMMI (Requirements Development & Management), ISO/IEC/IEEE 12207 |
| 7 | **FinOps** | Cloud usage, cost visibility and accountability, efficiency, sustainability | FinOps Maturity Model, Well-Architected (Cost, Sustainability) |

## 5. Suggested Next Steps

- **Review and trim.** Agree as a team which areas are in scope for v1. We could merge some (e.g., 9 into 1, or 6 into 5).
- **Define level descriptors.** For each area, write 1–2 sentences describing what levels 1–5 look like.
- **Choose a few key metrics.** Start with the DORA metrics as a common baseline.
- **Pilot a self-assessment.** Try it with one or two teams, then calibrate.
- **Set a review cadence.** Reassess every 6–12 months and refine the model as we learn.

## 6. References

- CMMI: https://cmmiinstitute.com/cmmi
- DORA: https://dora.dev
- *Accelerate* (Forsgren, Humble, Kim, 2018). IT Revolution Press
- SPACE framework: https://queue.acm.org/detail.cfm?id=3454124
- DevEx framework: https://queue.acm.org/detail.cfm?id=3595878
- NIST SP 800-218 SSDF: https://csrc.nist.gov/projects/ssdf
- CISA Secure by Design: https://www.cisa.gov/securebydesign
- OWASP SAMM: https://owaspsamm.org
- BSIMM: https://www.bsimm.com
- NIST Cybersecurity Framework 2.0: https://www.nist.gov/cyberframework
- SLSA: https://slsa.dev
- NIST SP 800-161r1: https://csrc.nist.gov/pubs/sp/800/161/r1/final
- CISA SBOM: https://www.cisa.gov/sbom
- AWS Well-Architected: https://aws.amazon.com/architecture/well-architected/
- Azure Well-Architected: https://learn.microsoft.com/en-us/azure/well-architected/
- Google Cloud Well-Architected: https://cloud.google.com/architecture/framework
- Google SRE books: https://sre.google/books/
- ISO/IEC 25010: https://www.iso.org/standard/78176.html
- ISO/IEC/IEEE 12207: https://www.iso.org/standard/63712.html
- ISO/IEC 33001: https://www.iso.org/standard/54175.html
- CNCF Platform Engineering Maturity Model: https://tag-app-delivery.cncf.io/whitepapers/platform-eng-maturity-model/
- DoD CIO Library (DevSecOps, Software Modernization): https://dodcio.defense.gov/library/
- FinOps Maturity Model: https://www.finops.org/framework/maturity-model/
- NIST AI RMF: https://www.nist.gov/itl/ai-risk-management-framework
- ISO/IEC 42001: https://www.iso.org/standard/81230.html
