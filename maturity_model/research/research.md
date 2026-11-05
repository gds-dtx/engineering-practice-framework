
# Engineering Maturity: Reference Model Research Notes

*Working reference, November 2026. Background for [proposal.md](proposal.md) and [cmmi_adaptation_approach.md](cmmi_adaptation_approach.md)*

## 1. Purpose and How to Read This

These notes summarize each reference model the proposal draws on. For each one:

- **At a glance:** who publishes it, current version, what *kind* of framework it is, and its cost or licensing
- **What it covers:** its scope and structure
- **How it is assessed:** formal assessment routes and self-assessment options
- **How software engineering teams can use it:** to find their current maturity and where to improve
- **Applicability by team type:** how relevant and appropriate it is for other kinds of team

### Kinds of framework

They aren't all maturity models, and that affects how we can use them:

| Kind | Meaning | Examples |
|---|---|---|
| **Maturity model** | Defines staged levels you progress through | CMMI, OWASP SAMM, CNCF Platform, FinOps, SLSA |
| **Practice framework** | Lists practices or outcomes, without levels | NIST SSDF, NIST CSF 2.0, Well-Architected, SRE, DoD DevSecOps, NIST AI RMF |
| **Measurement framework** | Says what to measure and how | DORA, SPACE, DevEx |
| **Benchmark** | Describes what other organizations actually do | BSIMM, DORA (benchmark element) |
| **Standard** | Formal standard, sometimes certifiable | ISO/IEC 25010, 12207, 33001, 42001 |

### Team types used in this document

| Team type | Meaning here |
|---|---|
| **Software engineering** | Builds and ships software products or features (the baseline) |
| **Service delivery** | Runs and evolves a live service for users: change, release, operations, service levels |
| **Support** | Handles incidents, requests, and problems for live systems (L2/L3 support, BAU) |
| **Research** | Exploratory work, prototypes, proofs of concept, R&D; output is often knowledge rather than production software |
| **Data** | Data engineering, pipelines, platforms, analytics, and BI |
| **ML/AI** | Builds, trains, evaluates, deploys, and monitors ML models or AI/LLM-based features |

**UK context:** We are UK-based, so UK frameworks (NCSC CAF, GOV.UK and NHS Service Standards, NHS DMA) carry the most weight. Non-UK frameworks are included for comparison and for clients overseas.

**Relevance scale:** **High** = directly applicable, use as a primary reference. **Medium** = parts apply, or it applies with adaptation. **Low** = little direct relevance, or too heavy for the context.

## 2. Reference Models: Overview

| Model | Published by | What we take from it |
|---|---|---|
| **CMMI v3.0** | ISACA / CMMI Institute | The maturity level scale (1–5) and the idea of grouping practices into areas |
| **DORA / *Accelerate*** | Google Cloud DORA research program | The key delivery metrics (throughput and instability) and research-backed capabilities |
| **SPACE & DevEx frameworks** | GitHub, Microsoft Research, U. Victoria | Measuring developer productivity and experience in several dimensions |
| **NIST SP 800-218 (SSDF)** | NIST (US Gov) | Baseline secure development practices, as required by federal software attestation |
| **CISA Secure by Design** | CISA (US Gov) | Security as a product default; vendor accountability principles |
| **OWASP SAMM v2** | OWASP | A maturity model for software security that grows step by step |
| **BSIMM** | Black Duck (formerly Synopsys) | A benchmark of real-world security activities across the industry |
| **NIST CSF 2.0** | NIST (US Gov) | The Govern function; risk-based organizational framing |
| **SLSA** | OpenSSF / Linux Foundation | Levels for build integrity and provenance |
| **NIST SP 800-161r1 / SBOM guidance** | NIST, CISA, NTIA (US Gov) | Supply chain risk management and software bills of materials |
| **Well-Architected Frameworks** | AWS, Microsoft Azure, Google Cloud | Architecture pillars: reliability, security, cost, performance, operations, sustainability |
| **Site Reliability Engineering (SRE)** | Google | SLOs, error budgets, incident management, toil reduction |
| **ISO/IEC 25010** | ISO/IEC | Characteristics of software product quality |
| **ISO/IEC/IEEE 12207 & ISO/IEC 33001 (SPICE)** | ISO/IEC/IEEE | Software lifecycle processes and process assessment method |
| **CNCF Platform Engineering Maturity Model** | CNCF TAG App Delivery | Maturity of internal developer platforms |
| **DoD Enterprise DevSecOps Fundamentals & Software Modernization Strategy** | US Dept. of Defense CIO | Government reference designs for DevSecOps and software factories |
| **FinOps Maturity Model** | FinOps Foundation | Crawl / Walk / Run stages for cloud cost management |
| **NIST AI RMF & ISO/IEC 42001** | NIST; ISO/IEC | Governing and managing risk for AI in our tools and products |
| **NHS Digital Maturity Assessment** | NHS England | How NHS clients are assessed on digital maturity (*What Good Looks Like*); peer-validated self-assessment |
| **NCSC Cyber Assessment Framework (CAF) v4.0** | UK National Cyber Security Centre | UK outcome-based cyber resilience framework and Core Profile; basis of GovAssure and the NHS DSPT |
| **MAS Technology Risk Management Guidelines** | Monetary Authority of Singapore | Regulator-set good practice for development, change, resilience, and cyber (for comparison) |
| **GovTech Digital Service Standards** | GovTech Singapore | Service standards with measurable, automated checks (for comparison) |
| **GOV.UK Service Standard / NHS Service Standard** | GDS; NHS England | 14 / 17-point service standards, delivery phases, and peer-led service assessments |
| **ITIL 4** | PeopleCert (formerly Axelos) | Service management practices (incident, problem, change enablement, service levels) and the ITIL Maturity Model |
| **ISO/IEC 20000-1** | ISO/IEC | Certifiable service management system standard |

---

## 3. Reference Model Details

### 3.1 CMMI v3.0

**At a glance:** ISACA / CMMI Institute. v3.0 released 2023. Maturity model. Model content and appraisals are licensed and paid; an official rating needs a formal appraisal.

**What it covers**

- Practices that build an organization's capability, grouped into **practice areas** (e.g., Requirements Development & Management, Technical Solution, Verification & Validation, Configuration Management, Planning, Risk & Opportunity Management, Causal Analysis & Resolution, Governance).
- Practice areas are grouped into **capability areas** and offered as **domain views**: Development, Services, Supplier Management, People, plus newer views for Safety, Security, Data, and Virtual delivery.
- Each practice area has an *intent*, a *value* statement, and practices arranged in levels. Higher levels build on lower ones.

**How it is assessed**

- **Two ways to rate:** *Maturity levels* 0–5 for the organization (Incomplete, Initial, Managed, Defined, Quantitatively Managed, Optimizing), or *capability levels* per practice area for a targeted view.
- **Formal appraisals** are led by an ISACA-certified Lead Appraiser. A *Benchmark* appraisal gives an official maturity-level rating, usually valid for 3 years; *Sustainment* and *Evaluation* appraisals maintain a rating or check progress. Evidence comes from artifacts and interviews across a sample of projects.
- Often required or valued in **government and defense contracts**.
- **Informal:** organizations commonly do gap analyses against practice-area intent before deciding whether to appraise.

**How software engineering teams can use it**

- **Find maturity:** For each practice area, ask: "Do we do this at all (L1)? Consistently and tracked (L2)? Using shared org standards (L3)? Managed by metrics (L4)? Continuously improved (L5)?"
- **Find improvements:** The practice-area *intent* statements make good prompts for discussion. Gaps usually show up first in Planning, Configuration Management, and Causal Analysis.
- **Watch out:** CMMI is organization-scale, and written for evidence over outcomes. Pair it with DORA metrics so it doesn't drift into box-ticking.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **High** | The Services view (Service Delivery Management, Strategic Service Management, Incident Resolution & Prevention, Continuity) fits directly. |
| Support | **Medium–High** | Incident Resolution & Prevention, Causal Analysis & Resolution, and Service Delivery Management apply. Most other areas are less relevant. |
| Research | **Low** | Defined, repeatable process clashes with exploratory work. Decision Analysis and Risk Management are useful in isolation. |
| Data | **Medium** | v3.0 adds Data Management and Data Quality practice areas, which are useful. The rest applies to data engineering as it does to software. |
| ML/AI | **Medium** | No AI-specific practice areas. Verification & Validation, Data Quality, and Risk Management carry over, but need ML-specific interpretation. |

---

### 3.2 DORA / *Accelerate*

**At a glance:** DORA research program (Google Cloud). Annual reports since 2014; *Accelerate* book 2018. Measurement framework and benchmark. Free.

**What it covers**

- **Software delivery performance metrics**, in two groups:
  - *Throughput*: change lead time, deployment frequency, failed deployment recovery time
  - *Instability*: change fail rate, rework rate
- **Capabilities** that predict performance, grouped as technical (e.g., CI, trunk-based development, test automation, loosely coupled architecture), process (e.g., small batches, visibility of work), and cultural (e.g., Westrum generative culture, learning culture).
- Recent reports cover **AI-assisted software development**, including a DORA AI Capabilities Model, platform engineering, and developer well-being.

**How it is assessed**

- No formal certification.
- **DORA Quick Check** (dora.dev): a free self-assessment that compares a team's delivery metrics to the research population.
- **Annual survey benchmark:** earlier reports grouped teams into elite/high/medium/low clusters. More recent reports describe team profiles that combine performance with well-being and other factors.
- **Tooling:** many engineering-intelligence tools calculate DORA metrics automatically from source control, CI/CD, and incident data.

**How software engineering teams can use it**

- **Find maturity:** Measure the delivery metrics, ideally from system data rather than estimates, and compare them to the DORA benchmark bands.
- **Find improvements:** Use the capability catalogue. Pick the capabilities most likely to be holding the team back (e.g., slow lead time points to batch size, test automation, or approval process), and run small experiments.
- **Watch out:** Don't use the metrics as individual targets or to rank teams. Always look at throughput and stability together.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **High** | Change and recovery metrics are core to running a service. Relevant culture and capabilities apply directly. |
| Support | **Medium** | Recovery time and change fail rate matter. Deployment frequency and lead time apply only if the team ships fixes. The culture findings apply fully. |
| Research | **Low** | Delivery throughput isn't the goal. Culture and learning findings still apply. |
| Data | **Medium–High** | Apply the metrics to pipeline and transformation code (dbt, Airflow, etc.). "Recovery time" maps naturally to data incidents. |
| ML/AI | **Medium–High** | Applies to model and feature deployment (MLOps). Add model-specific measures such as retraining lead time. The AI research is directly relevant to teams using AI assistants. |

---

### 3.3 SPACE and DevEx Frameworks

**At a glance:** SPACE (Forsgren, Storey, Maddila, Zimmermann, Houck, Butler, 2021) and DevEx (Noda, Storey, Forsgren, Greiler, 2023), both published in ACM Queue. Measurement frameworks, not maturity models. Free.

**What it covers**

- **SPACE:** five dimensions of developer productivity: **S**atisfaction & well-being, **P**erformance, **A**ctivity, **C**ommunication & collaboration, **E**fficiency & flow. The core message is that no single metric captures productivity.
- **DevEx:** three core dimensions of developer experience: **feedback loops**, **cognitive load**, and **flow state**. Each is measured through perceptions (surveys) and workflows (system data).

**How it is assessed**

- No formal assessment or levels.
- Teams choose metrics from at least **three SPACE dimensions**, mixing perception data (surveys) with system data (telemetry).
- Common delivery: quarterly developer experience surveys, sometimes through commercial tools that build on these frameworks.

**How software engineering teams can use it**

- **Find maturity:** Not a level, but a baseline. Run a short survey on satisfaction, flow, and cognitive load, and pair it with system data such as review wait time and build time.
- **Find improvements:** The lowest-scoring dimensions point to specific friction, e.g., slow CI (feedback loops), too many tools or unclear ownership (cognitive load), meeting load (flow).
- **Watch out:** Activity metrics (commits, PRs) are easy to measure and easy to misuse. Never use them alone.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **High** | Fully applicable. Toil and interruptions show up clearly under efficiency and flow. |
| Support | **Medium–High** | Satisfaction, well-being, and flow are critical given interrupt-driven work. Adapt "performance" to support outcomes (resolution quality, customer satisfaction). |
| Research | **High** | One of the few frameworks that suits research. Flow, cognitive load, and satisfaction matter more than throughput. |
| Data | **High** | Applies as is. Feedback loops (pipeline run time, data availability) are especially telling. |
| ML/AI | **High** | Applies as is. Feedback loops include experiment and training turnaround time. |

---

### 3.4 NIST SP 800-218: Secure Software Development Framework (SSDF)

**At a glance:** NIST (US Government). SP 800-218 v1.1 (2022), with an update in progress since 2025. SP 800-218A (2024) is a profile for generative AI and dual-use foundation models. Practice framework. Free.

**What it covers**

- Secure development practices in four groups:
  - **PO – Prepare the Organization:** roles, requirements, toolchains, secure environments
  - **PS – Protect the Software:** code integrity, release integrity, archiving and provenance
  - **PW – Produce Well-Secured Software:** secure design, threat modeling, secure coding, review, testing, secure configuration defaults
  - **RV – Respond to Vulnerabilities:** identify, assess, remediate, and analyze root causes
- Each practice has tasks, example implementations, and mappings to other standards (e.g., SAMM, BSIMM, ISO 27034).
- The basis of the **CISA Secure Software Development Attestation Form**, which software producers selling to US federal agencies must complete.

**How it is assessed**

- No maturity levels; you either implement each practice or task or you don't.
- **Self-attestation** to CISA for federal suppliers, or **third-party assessment** by an accredited organization (3PAO).
- **Informal:** gap analysis per task, rated implemented / partially implemented / not implemented, often combined with SAMM to add levels.

**How software engineering teams can use it**

- **Find maturity:** Walk through the PW and RV tasks; they are the most team-level. Mark each as implemented, partial, or missing, with evidence (pipeline config, threat models, scan results).
- **Find improvements:** Missing tasks become backlog items. Combine with SAMM if you want levels and a roadmap.
- **Watch out:** PO tasks are mostly organization-level. Teams depend on central security and platform teams for them.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **High** | Applies to any team changing production software, especially PS (release integrity) and RV. |
| Support | **Medium** | RV (vulnerability response) is directly relevant. Other groups apply only if the team writes fixes or code. |
| Research | **Low–Medium** | Light touch for throwaway prototypes. Becomes essential once research code moves toward production. |
| Data | **Medium** | Applies to pipeline code and infrastructure. Secrets handling, access control, and dependencies are the key areas. |
| ML/AI | **High** | **SP 800-218A** adds tasks for AI model development: training data integrity, model provenance, and protection against model weight theft or tampering. |

---

### 3.5 CISA Secure by Design

**At a glance:** CISA and international partners (US Government). Joint guidance *"Shifting the Balance of Cybersecurity Risk"* (2023) and the Secure by Design Pledge (2024). Set of principles, plus a voluntary pledge. Free.

**What it covers**

- **Three principles:**
  - Take ownership of customer security outcomes
  - Embrace radical transparency and accountability
  - Lead from the top
- **Pledge goals** (for enterprise software vendors), including: wider MFA, removing default passwords, reducing whole classes of vulnerability (e.g., memory-safe languages, parameterized queries), helping customers apply patches, publishing a vulnerability disclosure policy, transparent CVE reporting, and giving customers evidence of intrusions (logging).
- Related CISA guidance: Secure by Default, product security bad practices, memory safety roadmaps, and joint *Guidelines for Secure AI System Development* (2023, with the UK NCSC and partners).

**How it is assessed**

- No formal assessment or levels.
- Pledge signers committed to showing measurable progress publicly within a year.
- **Self-assessment:** check products against each pledge goal and the "bad practices" list.

**How software engineering teams can use it**

- **Find maturity:** Score each product against the pledge goals and bad-practices list (met / partial / not met). This is a quick, outcome-focused check.
- **Find improvements:** Removing whole classes of vulnerability, defaulting to secure configuration, and better logging are concrete engineering roadmap items.
- **Watch out:** It is product-focused. It tells you *what* good looks like, not *how* to build the process (use SSDF/SAMM for that).

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **High** | Applies directly to services users access: MFA, secure defaults, logging, patching. |
| Support | **Medium** | Patching, vulnerability disclosure handling, and intrusion evidence (logs) involve support teams. |
| Research | **Low** | Mostly not applicable until research becomes a product. |
| Data | **Medium** | Secure defaults, access control, and audit logging on data platforms and shared datasets. |
| ML/AI | **Medium–High** | The secure AI system development guidelines apply directly to AI features and model deployment. |

---

### 3.6 OWASP SAMM v2 (Software Assurance Maturity Model)

**At a glance:** OWASP (open community). v2.0 (2020), maintained since. Maturity model. Free and open.

**What it covers**

- **Five business functions**, each with three security practices (15 practices in total):
  - **Governance:** Strategy & Metrics, Policy & Compliance, Education & Guidance
  - **Design:** Threat Assessment, Security Requirements, Security Architecture
  - **Implementation:** Secure Build, Secure Deployment, Defect Management
  - **Verification:** Architecture Assessment, Requirements-driven Testing, Security Testing
  - **Operations:** Incident Management, Environment Management, Operational Management
- Each practice has two **streams** and **maturity levels 1–3**, with 0 meaning nothing is in place.

**How it is assessed**

- **Self-assessment** using the official SAMM questionnaire and toolbox spreadsheet, or online tools.
- Each answer is weighted; the result is a score from 0 to 3 for each practice and stream.
- No certification. Some consultancies run assisted assessments.
- The model is built to support **target setting and roadmaps** (current score, target score, phased plan).

**How software engineering teams can use it**

- **Find maturity:** Answer the questionnaire as a team. It takes 1–2 hours and gives a score per practice.
- **Find improvements:** Set a realistic target (often 1.5–2 in most practices), and focus on the 2–3 practices with the biggest gap and business risk.
- **Watch out:** Some practices (Strategy & Metrics, Policy & Compliance) are organization-level. Score those once centrally rather than per team.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **High** | The Implementation and Operations functions are directly relevant. |
| Support | **Medium** | The Operations function (incident and environment management) applies. Design and Verification are less relevant. |
| Research | **Low** | Too heavy for exploratory work. Threat Assessment can be useful as a light-touch exercise. |
| Data | **Medium** | Applies to data platform and pipeline code. No data-specific practices, e.g., on data classification or privacy. |
| ML/AI | **Medium** | Applies to the software around models. Doesn't cover AI-specific threats (prompt injection, data poisoning); add OWASP Top 10 for LLM Applications and NIST AI RMF. |

---

### 3.7 BSIMM (Building Security In Maturity Model)

**At a glance:** Black Duck (formerly Synopsys). Published annually since 2008 (BSIMM15 is the latest at time of writing). Benchmark that describes what organizations actually do. The report is free; formal assessments are paid.

**What it covers**

- **Four domains, 12 practices,** made up of over 100 observed activities:
  - **Governance:** Strategy & Metrics, Compliance & Policy, Training
  - **Intelligence:** Attack Models, Security Features & Design, Standards & Requirements
  - **SSDL Touchpoints:** Architecture Analysis, Code Review, Security Testing
  - **Deployment:** Penetration Testing, Software Environment, Configuration & Vulnerability Management
- Built from observations of real software security initiatives at many organizations, mostly large enterprises.

**How it is assessed**

- **Formal:** Black Duck assessors interview staff and record which activities the organization carries out. The results are compared to the community (e.g., "x% of firms do this activity").
- **Informal:** use the public activity list as a checklist and compare your coverage to the published frequencies.
- It describes what others do, so it gives **no levels and no targets**. It's a way to compare yourself with peers.

**How software engineering teams can use it**

- **Find maturity:** Mostly org-level, but teams can check which common activities (code review, security testing, environment hardening) they practice.
- **Find improvements:** Activities that most organizations do but we don't are strong candidates for improvement.
- **Watch out:** Built for central security groups. Use SAMM for team-level assessment and BSIMM to compare with industry.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **Medium** | The Deployment domain is relevant. The rest is mostly org-level. |
| Support | **Low–Medium** | Configuration & Vulnerability Management activities apply. |
| Research | **Low** | Not relevant. |
| Data | **Low–Medium** | Little coverage specific to data. |
| ML/AI | **Low–Medium** | Recent editions note AI-related activities, but coverage is thin compared to dedicated AI frameworks. |

---

### 3.8 NIST Cybersecurity Framework (CSF) 2.0

**At a glance:** NIST (US Government). v2.0 released February 2024. Practice framework, organized around outcomes. Free, widely used globally.

**What it covers**

- **Six functions:** **Govern** (new in 2.0), **Identify**, **Protect**, **Detect**, **Respond**, **Recover**. They are broken down into categories and subcategories, each an outcome to achieve.
- **Profiles:** *Current* and *Target* profiles describe where you are and where you want to be. *Community Profiles* are shared templates for a sector or use case.
- **Tiers 1–4** (Partial, Risk Informed, Repeatable, Adaptive) describe how rigorous cybersecurity risk governance and management are.
- **Informative references** map to other standards (SP 800-53, ISO 27001, CIS Controls, etc.).

**How it is assessed**

- No certification. Assessment is done through current and target profiles and tier ratings.
- Often assessed by internal audit or third parties. Commonly used for board-level reporting.
- Tiers are *not* officially a maturity model, but many organizations use them as one.

**How software engineering teams can use it**

- **Find maturity:** Mostly org-level. Teams can rate the subcategories they own (e.g., asset inventory, logging and detection for their services, recovery testing).
- **Find improvements:** Gaps between current and target profiles in Detect, Respond, and Recover often turn into engineering work (alerting, runbooks, backups, restore tests).
- **Watch out:** Not about how software is built; pair it with SSDF for that.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **High** | Protect, Detect, Respond, and Recover map directly to running a service. |
| Support | **High** | Detect, Respond, and Recover are central to support work. |
| Research | **Low** | Only basic Protect outcomes (access, data handling) apply. |
| Data | **Medium–High** | Identify (data inventory, classification) and Protect (data security) are highly relevant. |
| ML/AI | **Medium** | General outcomes apply. AI-specific risks need NIST AI RMF alongside. |

---

### 3.9 SLSA (Supply-chain Levels for Software Artifacts)

**At a glance:** OpenSSF / Linux Foundation. v1.0 (2023), extended since. Maturity model with levels. Free and open.

**What it covers**

- Integrity of the software supply chain: guarding against tampering between source code and the artifact people deploy.
- **Build track levels:**
  - **L0:** No guarantees
  - **L1:** Provenance exists, showing how the artifact was built
  - **L2:** Built on a hosted build platform that signs the provenance
  - **L3:** Hardened build platform; builds are isolated from each other and signing material is protected
- Later versions add tracks beyond the build, such as source integrity.

**How it is assessed**

- **Self-assessment** of build platforms and pipelines against each level's requirements. Many CI platforms state the SLSA level they support.
- **Verifiable at use:** consumers can check provenance automatically (e.g., with `slsa-verifier` or policy engines at deploy time).
- No certification body.

**How software engineering teams can use it**

- **Find maturity:** Check what each build pipeline currently produces. Is there any provenance? Is it signed? Does the build run on a hosted, isolated platform?
- **Find improvements:** L1 to L2 is usually a platform change (use the standard hosted CI and generate signed provenance). L3 depends on the platform team.
- **Watch out:** Covers build integrity only. Pair it with SBOMs and dependency management.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **High** | Any team deploying built artifacts. |
| Support | **Low** | Only relevant if the team builds and ships hotfixes. |
| Research | **Low** | Not relevant until code is released or shared outside the team. |
| Data | **Medium** | Applies to pipeline images and packages. The ideas can extend to data artifacts. |
| ML/AI | **Medium–High** | Model artifacts need provenance just as binaries do. Industry work on model signing and provenance builds on SLSA's ideas. |

---

### 3.10 NIST SP 800-161r1 and SBOM Guidance

**At a glance:** NIST SP 800-161 Rev. 1 (2022, updated 2024) for cybersecurity supply chain risk management (C-SCRM). SBOM guidance from NTIA (*Minimum Elements*, 2021) and CISA (ongoing updates). Practice framework and standards. Free.

**What it covers**

- **SP 800-161r1:** organization-wide supply chain risk management: governance, supplier risk assessment, and supply chain controls that build on SP 800-53. Largely aimed at agencies and the organizations that buy from or supply them.
- **SBOM:** a machine-readable list of software components. *Minimum elements* cover the data fields, automation support, and practices (how often, how deep). Common formats are **SPDX** and **CycloneDX**.
- **Extensions:** SPDX 3.0 adds **AI** and **Dataset** profiles; CycloneDX supports **ML-BOMs**. Both are relevant to data and AI teams.

**How it is assessed**

- **800-161:** control assessments as part of the wider security and risk program, usually led by risk or compliance teams.
- **SBOM:** can we produce SBOMs automatically for every release? Do they meet the minimum elements? Can we ingest supplier SBOMs and act on vulnerabilities in them (e.g., using VEX)?
- No maturity levels. Some community maturity models for SBOM practice exist (generate, then manage, then use operationally).

**How software engineering teams can use it**

- **Find maturity:** For each product: is an SBOM generated in CI, stored with the release, and used to monitor vulnerabilities?
- **Find improvements:** Generate SBOMs automatically, connect them to vulnerability monitoring, track license compliance, and identify dependencies at risk (unmaintained, single maintainer).
- **Watch out:** 800-161 is heavy. Most teams only need the SBOM and dependency hygiene parts.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **High** | SBOMs for deployed services, and dependency vulnerability management. |
| Support | **Medium** | SBOMs speed up answering "are we affected?" when a new vulnerability is announced. |
| Research | **Low** | Basic awareness only; check licenses before research code is reused. |
| Data | **Medium** | Dependencies of pipeline tooling; SPDX dataset profiles for data lineage and provenance. |
| ML/AI | **High** | AI-BOMs and ML-BOMs record models, datasets, and frameworks. Increasingly expected for AI transparency. |

---

### 3.11 Well-Architected Frameworks (AWS, Azure, Google Cloud)

**At a glance:** AWS Well-Architected Framework, Microsoft Azure Well-Architected Framework, and Google Cloud Well-Architected Framework. All updated continuously. Practice frameworks with review tools. Free.

**What it covers**

- **Pillars:**
  - **AWS (six):** Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, Sustainability
  - **Azure (five):** Reliability, Security, Cost Optimization, Operational Excellence, Performance Efficiency
  - **Google Cloud:** a similar set, including operational excellence, security, reliability, cost, performance, and sustainability
- Design principles, best practices, and review questions for each pillar.
- **Lenses and workload guidance**, including for **machine learning, generative AI, data analytics,** serverless, and SaaS (AWS), and AI workload guidance (Azure).

**How it is assessed**

- **Self-review tools:** the AWS Well-Architected Tool and the Azure Well-Architected Review in Microsoft Assessments. Both are free questionnaires per workload that identify high- and medium-risk issues and generate improvement plans.
- Cloud providers and partners offer facilitated reviews, sometimes with funding attached.
- Assessed per **workload**, not per team. Results are lists of risk items, not maturity levels.

**How software engineering teams can use it**

- **Find maturity:** Run a review of each major workload once or twice a year. The number of high-risk issues is a simple, trackable indicator.
- **Find improvements:** Remediating high-risk issues goes into the backlog. Reliability, security, and cost pillars usually give the quickest wins.
- **Watch out:** Each is specific to a cloud provider. For multi-cloud or on-premises, stick to the principles and ignore service-specific advice.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **High** | Reliability and Operational Excellence pillars fit directly. |
| Support | **Medium** | Operational Excellence (runbooks, observability, operational readiness) is directly useful. |
| Research | **Low–Medium** | The Cost pillar is useful for keeping experimental cloud spend under control. |
| Data | **High** | Data analytics lens and guidance cover data lakes, pipelines, and governance. |
| ML/AI | **High** | Machine learning and generative AI lenses (AWS) and AI workload guidance (Azure) cover the full ML lifecycle. |

---

### 3.12 Site Reliability Engineering (SRE)

**At a glance:** Google. *Site Reliability Engineering* (2016), *The Site Reliability Workbook* (2018), *Building Secure & Reliable Systems* (2020). Practice framework (a discipline). Books are free online at sre.google.

**What it covers**

- **SLIs, SLOs, and error budgets:** defining reliability from the user's point of view and balancing it against the pace of change.
- **Toil reduction**, monitoring and alerting (symptom-based), **on-call**, **incident management**, **blameless postmortems**, release engineering, capacity planning, and **production readiness reviews**.
- Cultural principles: engineering solutions to operational problems, shared ownership with development teams.

**How it is assessed**

- No official assessment or levels.
- Common approaches: production readiness review checklists, SLO coverage (share of services with defined SLOs and error budget policies), toil measurement, and postmortem quality and follow-through.
- Various community and vendor SRE maturity models exist. None is authoritative.

**How software engineering teams can use it**

- **Find maturity:** Check each service. Does it have SLIs and SLOs users care about? Is there an error budget policy? Are alerts based on symptoms users see? Are postmortems blameless, and are their actions completed?
- **Find improvements:** Start with SLOs for the most important user journeys. Measure toil and aim for it to stay below about 50% of operational time (Google's guideline).
- **Watch out:** Don't copy Google's organizational model (a separate SRE team) without thinking. The practices work well within product teams too.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **High** | This is SRE's home ground. |
| Support | **High** | Incident management, postmortems, toil reduction, and on-call practices transform support work. |
| Research | **Low** | Not applicable to exploration. |
| Data | **High** | The SRE Workbook covers data processing pipelines; freshness, completeness, and correctness make natural data SLOs. |
| ML/AI | **Medium–High** | Model serving latency and availability fit SRE directly. Add model quality and drift SLOs. |

---

### 3.13 ISO/IEC 25010 (Product Quality Model)

**At a glance:** ISO/IEC, part of the SQuaRE (25000) series. 25010:2023 is the current edition. Standard. Paid to purchase.

**What it covers**

- A **product quality model** with nine characteristics: functional suitability, performance efficiency, compatibility, interaction capability (previously usability), reliability, security, maintainability, flexibility (previously portability), and **safety** (new in 2023). Each has sub-characteristics.
- Related standards in the same series:
  - **ISO/IEC 25012:** a **data quality** model (accuracy, completeness, consistency, timeliness, etc.)
  - **ISO/IEC 25059:** a quality model for **AI systems**, adding AI-specific characteristics such as robustness, transparency, and controllability
  - **ISO/IEC 25023:** quality measures
  - **ISO/IEC 25040:** the evaluation process
  - **ISO/IEC 25019:** quality in use (split out in the 2023 revision)

**How it is assessed**

- A product quality evaluation following ISO/IEC 25040, using measures from ISO/IEC 25023.
- No certification of products against 25010 itself. It is a model for *defining and assessing* quality requirements.
- No maturity levels.

**How software engineering teams can use it**

- **Find maturity:** Not a maturity tool. Use it to check that the quality characteristics that matter are *defined, measured, and tested*, e.g., do we have non-functional requirements for performance, security, and maintainability?
- **Find improvements:** Choose the 3–4 characteristics that matter most for the product, define measurable targets, and add tests or checks for them to CI.
- **Watch out:** Can turn into a theoretical exercise. Keep it tied to real quality targets.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **Medium** | Reliability, performance, and security characteristics shape service level targets. |
| Support | **Low–Medium** | Useful vocabulary for classifying defects and recurring problems. |
| Research | **Low** | Minimal relevance, apart from the vocabulary for describing prototype quality. |
| Data | **High** (via 25012) | ISO/IEC 25012 is one of the few formal data quality models, a strong reference for data teams. |
| ML/AI | **High** (via 25059) | ISO/IEC 25059 gives an AI-specific quality vocabulary useful for evaluation criteria. |

---

### 3.14 ISO/IEC/IEEE 12207 and ISO/IEC 33001 (SPICE)

**At a glance:** ISO/IEC/IEEE 12207:2017 (software lifecycle processes) and the ISO/IEC 33001 family (process assessment, which replaced ISO/IEC 15504 "SPICE"). Standards. Paid to purchase.

**What it covers**

- **12207:** a full set of software lifecycle processes in four groups: agreement, organizational project-enabling, technical management, and technical. Technical covers requirements, architecture, design, implementation, integration, verification, transition, validation, operation, maintenance, and disposal.
- **33001 series:** the framework for assessing processes.
  - **Capability levels 0–5:** Incomplete, Performed, Managed, Established, Predictable, Innovating
  - Assessment process requirements (ISO/IEC 33002) and process assessment models, e.g., ISO/IEC 33061 for software lifecycle processes
- Well-known industry variant: **Automotive SPICE**, widely required in automotive software.

**How it is assessed**

- **Formal assessments** by competent or certified assessors, following ISO/IEC 33002, rating each process's capability level.
- Common in regulated or safety-critical industries (automotive, aerospace, medical).
- **Informal:** self-assessment of selected processes against capability levels.

**How software engineering teams can use it**

- **Find maturity:** Rate key processes (e.g., requirements, verification, configuration management) against the 0–5 capability levels.
- **Find improvements:** Use 12207 as a checklist of lifecycle processes, to make sure none are missing (operations and disposal are often forgotten).
- **Watch out:** Heavy and document-centric. Usually only worth it where regulation or customers require it.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **Medium** | Operation and maintenance processes apply. For service management, **ITIL 4** (3.24) and **ISO/IEC 20000-1** (3.25) fit better. |
| Support | **Low–Medium** | Maintenance processes apply. ITIL 4 (3.24) and ISO/IEC 20000-1 (3.25) are more appropriate. |
| Research | **Low** | Not appropriate for exploratory work. |
| Data | **Low–Medium** | General lifecycle processes apply. No data-specific processes. |
| ML/AI | **Low–Medium** | General lifecycle processes apply. **ISO/IEC 5338** (AI system lifecycle processes) is the AI-specific extension worth looking at. |

---

### 3.15 CNCF Platform Engineering Maturity Model

**At a glance:** CNCF TAG App Delivery (Platforms Working Group). Published 2023. Maturity model. Free and open.

**What it covers**

- Maturity of **internal developer platforms** and platform teams across **five aspects:**
  - **Investment:** how the platform is staffed and funded
  - **Adoption:** how and why users find and use it
  - **Interfaces:** how users interact with it (self-service, APIs, golden paths)
  - **Operations:** how platform capabilities are planned, run, and maintained
  - **Measurement:** how feedback and metrics drive improvement
- **Four levels:** **Provisional**, **Operational**, **Scalable**, **Optimizing**.
- Companion CNCF *Platforms White Paper* defines what platforms and platform capabilities are.

**How it is assessed**

- **Self-assessment** only. Rate each aspect against the level descriptions.
- No certification or formal process.

**How software engineering teams can use it**

- **Find maturity:** Platform teams rate themselves per aspect. Product teams can give the consumer view: do golden paths exist, can they self-serve, does the platform reduce cognitive load?
- **Find improvements:** Common gaps are Adoption (the platform is mandated rather than chosen) and Measurement (no feedback on platform use or developer satisfaction).
- **Watch out:** It assesses the *platform*, not the teams using it. Use it alongside DevEx surveys of the platform's users.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **Medium–High** | Consumers of the platform, and sometimes operators of platform capabilities. |
| Support | **Low–Medium** | Benefit from standardization; the operations aspect is relevant. |
| Research | **Medium** | Self-service sandboxes and compute speed up research. Research teams are an important platform user group. |
| Data | **High** | Applies directly to **data platforms** (self-service ingestion, catalogs, compute). |
| ML/AI | **High** | Applies directly to **ML/AI platforms** (feature stores, training infrastructure, model registry and serving). |

---

### 3.16 DoD Enterprise DevSecOps Fundamentals and Software Modernization Strategy

**At a glance:** US Department of Defense CIO. DevSecOps Strategy Guide, Fundamentals, Reference Designs, Playbook, and Activities & Tools guidebook (2021 onward); DoD Software Modernization Strategy (2022) and implementation plan. Practice frameworks and reference architectures. Free, published in the DoD CIO Library.

**What it covers**

- **DevSecOps fundamentals:** lifecycle phases (plan, develop, build, test, release, deliver, deploy, operate, monitor, feedback), the *software factory* concept, continuous security, and required activities and tools at each phase.
- **Reference designs:** e.g., CNCF Kubernetes-based designs and multi-cluster or cloud-provider variants.
- **Continuous Authority to Operate (cATO):** moving from point-in-time security authorization to continuous monitoring, with criteria for continuous assessment.
- **Software Modernization Strategy:** software factories, cloud adoption, faster delivery, and workforce goals across DoD.
- Related: the DoD *Data, Analytics, and AI Adoption Strategy* (2023) for data and AI teams.

**How it is assessed**

- No maturity scoring.
- Assessment happens through **authorization**: software factories and programs are evaluated by Authorizing Officials, increasingly under cATO criteria (continuous monitoring, active cyber defense, secure software supply chain).
- Organizations can self-assess against the Activities & Tools guidebook and Playbook practices.

**How software engineering teams can use it**

- **Find maturity:** Check the team's pipeline against the required DevSecOps activities and tools per phase. Look for gaps in automated security testing, artifact management, and monitoring.
- **Find improvements:** The Playbook "plays" are practical improvement items. The cATO criteria show what a continuous-compliance pipeline looks like.
- **Watch out:** Written for the DoD context. Valuable when working with government, but some requirements (specific tools, hardened container sources) may be more than a non-government team needs.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **High** (gov) / **Medium** (non-gov) | Operate and monitor phases, and continuous monitoring for cATO. |
| Support | **Medium** | Operate, monitor, and feedback phases apply. |
| Research | **Low** | Not applicable, except for research moving into DoD programs. |
| Data | **Medium** | Apply DevSecOps to pipelines. The DoD data and AI strategy gives the government context. |
| ML/AI | **Medium** | DevSecOps carries over to MLOps. The DoD AI strategy and Responsible AI guidance cover AI-specific issues. |

---

### 3.17 FinOps Framework and Maturity Model

**At a glance:** FinOps Foundation (Linux Foundation). Framework updated regularly; recent versions widen scope beyond public cloud. Practice framework with maturity stages. Free.

**What it covers**

- **Principles** (e.g., teams take ownership of their usage; decisions are driven by business value).
- **Phases:** **Inform** → **Optimize** → **Operate**, repeated continuously.
- **Domains:** understand usage and cost, quantify business value, optimize usage and cost, manage the FinOps practice. Each domain contains **capabilities** such as allocation, forecasting, budgeting, unit economics, rate optimization, and workload optimization.
- **Personas:** engineering, finance, product, procurement, leadership.
- **Scope** now extends beyond public cloud to areas such as SaaS, data centers, licensing, and **AI** spend.

**How it is assessed**

- **Maturity per capability:** **Crawl / Walk / Run**.
- The FinOps Foundation provides **assessment guidance**, rating capabilities across lenses such as knowledge, process, metrics, adoption, and automation.
- No organizational certification. Individual practitioners can be certified (e.g., FinOps Certified Practitioner).

**How software engineering teams can use it**

- **Find maturity:** Can the team see its own costs (allocation and tagging)? Does it have a unit cost metric (e.g., cost per customer or per transaction)? Are cost signals part of engineering decisions?
- **Find improvements:** Common first steps are tagging and allocation (Crawl), cost per service on team dashboards (Walk), and automated rightsizing or scheduling plus unit economics targets (Run).
- **Watch out:** "Run" isn't the target for every capability. The framework itself says to aim for the maturity each capability actually needs.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **High** | Teams running services drive most cloud spend. |
| Support | **Low** | Little direct control over spend, though they may spot waste. |
| Research | **Medium** | Budgets for experimental compute and cost guardrails (auto-shutdown, quotas) are valuable. |
| Data | **High** | Data platforms (warehouses, lakehouses, query engines) are often among the biggest and least predictable costs. |
| ML/AI | **High** | GPU, training, and inference/token costs are significant; FinOps for AI is now an explicit focus area. |

---

### 3.18 NIST AI RMF and ISO/IEC 42001

**At a glance:** NIST AI Risk Management Framework 1.0 (January 2023), with the Playbook and the Generative AI Profile (NIST AI 600-1, 2024). ISO/IEC 42001:2023, the AI management system standard. NIST is a free practice framework. ISO 42001 is a paid, **certifiable** standard.

**What it covers**

- **NIST AI RMF:** four functions:
  - **Govern:** culture, policies, accountability
  - **Map:** context, intended use, risks
  - **Measure:** testing, evaluation, metrics
  - **Manage:** prioritization, response, monitoring

  It also defines characteristics of trustworthy AI: valid & reliable, safe, secure & resilient, accountable & transparent, explainable & interpretable, privacy-enhanced, fair with harmful bias managed. The **GenAI Profile** adds risks specific to generative AI (e.g., confabulation, information integrity, data privacy, intellectual property).
- **ISO/IEC 42001:** an AI management system (AIMS), similar in structure to ISO 27001. It covers policy, roles, AI risk and impact assessment, lifecycle controls (Annex A), supplier and third-party AI, and continual improvement. Related: **ISO/IEC 23894** (AI risk management), **ISO/IEC 42005** (AI impact assessment).
- Both are useful for preparing for regulation such as the **EU AI Act**.

**How it is assessed**

- **NIST AI RMF:** voluntary, with no certification. Self-assessment through current and target profiles and the Playbook's suggested actions.
- **ISO/IEC 42001:** **third-party certification audits** by accredited certification bodies, with surveillance audits each year, plus internal audits and management reviews.
- No maturity levels in either. Organizations often add their own levels or combine with other models.

**How software engineering teams can use it**

- **Find maturity:** For teams building AI features: is intended use documented? Are risks mapped? Do evaluations cover the trustworthy characteristics? Is the model monitored after release?
- **Find improvements:** Common gaps are evaluation coverage (bias, robustness), documentation (model cards, data sheets), and monitoring after deployment.
- **For all teams using AI coding assistants:** Govern outcomes apply, covering acceptable use, review of AI-generated code, and data sent to AI tools.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **Medium** | Relevant when the service includes AI features, or the team uses AI in operations. |
| Support | **Low–Medium** | Relevant for AI chatbots or triage, and for handling AI-related incidents. |
| Research | **Medium–High** | Map and Measure support responsible research; documenting risk early makes it easier to move into production. |
| Data | **High** | Training data quality, provenance, privacy, and bias are core to both frameworks. |
| ML/AI | **High** | The primary governance and risk frameworks for these teams. |

---

---

### 3.19 NHS Digital Maturity Assessment (DMA)

**At a glance:** NHS England. New programme commissioned in 2022; national results published for 2024 and 2025. Maturity assessment for health and care organizations. Free to NHS providers and integrated care systems (ICSs).

**What it covers**

- Digital maturity of NHS **providers and ICSs**, measured against the seven dimensions of NHS England's ***What Good Looks Like* (WGLL)** framework:
  - **Well led:** digital strategy, leadership, and governance
  - **Ensure smart foundations:** infrastructure, cyber security, digital workforce and skills
  - **Safe practice:** clinical safety, information governance, standards
  - **Support people:** digital tools that help staff do their jobs
  - **Empower citizens:** digital access to services and records for patients
  - **Improve care:** digitally enabled pathways and decision support
  - **Healthy populations:** data and analytics for population health
- Each organization's strengths and gaps in providing digital services, tracked year on year across the NHS.

**How it is assessed**

- **Self-assessment** by providers and ICSs, using a standard national question set mapped to the seven WGLL dimensions.
- Results are **validated through peer review sessions and workshops**.
- Organizations can compare themselves against a **national baseline dataset**. NHS England uses the results to plan and commission digital transformation.
- No certification. The results are a planning tool, not a pass/fail test.

**How software engineering teams can use it**

- **Find maturity:** It's an organization-level tool, so teams don't assess themselves with it directly. Teams supporting NHS organizations can find out their client's DMA results and see which dimensions their work contributes to (most often *smart foundations*, *support people*, and *empower citizens*).
- **Find improvements:** Use the WGLL dimensions to make sure the engineering roadmap supports what NHS clients are being measured on. Interoperability, cyber security, and usability are common themes.
- **Design idea to borrow:** Self-assessment **validated by peer review**, with a **national baseline** to compare against, is a strong pattern for our own model.
- **Watch out:** Built for health and care organizations, not engineering teams. Use it to understand context, not as our assessment.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **Medium** | "Smart foundations", "support people", and "empower citizens" set expectations for NHS-facing services. |
| Support | **Low–Medium** | Smart foundations (infrastructure, cyber) relates to support work indirectly. |
| Research | **Low** | Little direct relevance. "Improve care" can frame research aimed at clinical value. |
| Data | **Medium–High** | "Healthy populations" and "improve care" depend heavily on data and analytics maturity. |
| ML/AI | **Medium** | Decision support and population health analytics are where AI shows up. Pair with clinical safety (DCB0129/DCB0160) and the NICE Evidence Standards Framework. |

---

### 3.20 NCSC Cyber Assessment Framework (CAF)

**At a glance:** UK National Cyber Security Centre. **Version 4.0** is current, with a new **CAF Core Profile**. Practice framework based on outcomes, used with profiles. Free. **Directly relevant to us as a UK organization.**

**What it covers**

- **Four objectives** and their principles:
  - **A. Managing security risk:** A1 Governance, A2 Risk Management, A3 Asset Management, A4 Supply Chain
  - **B. Protecting against cyber attacks:** B1 Service protection policies, processes and procedures; B2 Identity and Access Control; B3 Data Security; B4 System Security; B5 Resilient Networks and Systems; B6 Staff Awareness and Training
  - **C. Detecting cyber security events:** C1 Security Monitoring, C2 Threat Hunting
  - **D. Minimising the impact of incidents:** D1 Response and Recovery Planning, D2 Lessons Learned
- Each principle breaks down into **contributing outcomes**, with **Indicators of Good Practice (IGPs)**.
- It describes outcomes rather than prescribing controls, so it adapts to different technology and risk profiles.
- **Profiles** set the minimum level of achievement expected against a defined threat level. The **Core Profile** (v4.0) is a cross-sector baseline against moderately capable attackers (ransomware, supply chain compromise, exploiting legacy technology). Regulators and oversight bodies can set higher profiles.
- **Used in:**
  - The **NIS Regulations** (operators of essential services)
  - **GovAssure**, the cyber assurance scheme for UK government departments
  - The **NHS Data Security and Protection Toolkit (DSPT)**, which has moved to a CAF-aligned format for many NHS organizations

**How it is assessed**

- Each contributing outcome is rated **Achieved / Partially achieved / Not achieved**, using evidence and expert judgement against the IGPs, not as a simple checklist.
- Results are compared to a **target profile**: the Core Profile or one set by a sector regulator.
- **Routes:** self-assessment, independent assurance (e.g., GovAssure uses independent assessors), or review by a sector regulator under NIS.
- **Not a certification scheme.** The NCSC says achieving a profile doesn't guarantee security and must not be presented as NCSC certification. For a certificate, the UK scheme is **Cyber Essentials / Cyber Essentials Plus**.

**How software engineering teams can use it**

- **Find maturity:** Teams own or contribute to many contributing outcomes, especially **B2** (identity and access), **B4** (system security: secure configuration, vulnerability management, secure development), **B5** (resilience), **C1** (monitoring), and **D1/D2** (response, recovery, lessons learned). Rate these for the team's services against the Core Profile.
- **Find improvements:** Outcomes rated "Partially achieved" make a ready-made, prioritized backlog: logging coverage, patch timeliness, restore tests, incident runbooks, post-incident reviews.
- **Watch out:** Objective A is mostly organization-level, and the CAF doesn't cover *how* software is built in depth. Pair it with NIST SSDF or OWASP SAMM for that.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **High** | B4, B5, C1, and D1 map directly to running secure, resilient services. Likely to be expected by UK public-sector and NHS clients. |
| Support | **High** | Detection (C), response and recovery (D1), and lessons learned (D2) are central to support work. |
| Research | **Low** | Only basic identity, data security, and asset outcomes apply. |
| Data | **High** | B3 Data Security and A3 Asset Management (data inventory) are directly relevant, and especially important for NHS data under the DSPT. |
| ML/AI | **Medium** | General outcomes apply to AI systems. AI-specific threats need NCSC/CISA secure AI guidance and NIST AI RMF alongside. |

---

### 3.21 MAS Technology Risk Management (TRM) Guidelines

**At a glance:** Monetary Authority of Singapore (financial regulator). Revised edition issued **January 2021**. Regulatory guidelines (practice framework), with related binding MAS *Notices*. Free. *Details below are from my own knowledge; verify against the MAS website, which couldn't be fetched automatically.*

**What it covers**

- Technology risk expectations for financial institutions, with unusually specific coverage of engineering practice:
  - **Technology risk governance and oversight:** board and senior management roles, policies, competence
  - **Technology risk management framework:** risk identification, assessment, treatment, and monitoring
  - **IT project management and security-by-design**
  - **Software application development and management:** secure coding, source code review, application security testing, **DevSecOps**, API security, managing end-user-developed applications
  - **IT service management:** configuration, change, software release, incident and problem management
  - **IT resilience:** system availability, recoverability, disaster recovery testing, data backup
  - **Access control, cryptography, data and infrastructure security**
  - **Cyber security operations and assessment:** vulnerability assessment, penetration testing, red teaming, cyber exercises
  - **Third-party and cloud risk**, plus online financial services and IT audit
- Related MAS Notices set **binding requirements**, e.g., cyber hygiene, timely incident notification, and availability and recovery targets for critical systems.

**How it is assessed**

- The guidelines aren't legally binding, but MAS expects institutions to follow them; the Notices are mandatory.
- Assessed through **MAS supervisory reviews and inspections**, internal and external **IT audit**, and the institution's own self-assessment against each section.
- No maturity levels or certification.

**How software engineering teams can use it**

- **Find maturity:** Use it as a **check of good practice set by a regulator**, even outside Singapore and finance. The sections on software development and IT service management make a concise checklist: secure coding standards, code review, security testing, release controls, change management, incident and problem management.
- **Find improvements:** The resilience sections give concrete, measurable expectations (defined recovery targets, regular disaster recovery testing, backups), which are good benchmarks for critical services.
- **Watch out:** Written for regulated financial institutions. Take the engineering practices, not the compliance machinery. For UK financial clients, the **PRA/FCA operational resilience** rules are the local equivalent.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **High** (as a reference) | Change, release, resilience, and availability expectations map directly to running a service. |
| Support | **High** (as a reference) | Incident and problem management, disaster recovery, and cyber operations sections apply directly. |
| Research | **Low** | Not applicable to exploratory work. |
| Data | **Medium** | Data security, cryptography, and backup and recovery sections apply. |
| ML/AI | **Low–Medium** | General development and security practices apply. AI is covered separately by MAS FEAT and Veritas. |

**UK relevance:** Comparison only. Useful as a well-written benchmark, and relevant if we work with Singapore-regulated financial clients.

---

### 3.22 Singapore GovTech Digital Service Standards (DSS)

**At a glance:** GovTech Singapore / Smart Nation and Digital Government Group. Introduced around 2018 and updated since. Service standard for Singapore government digital services. Free. *Details below are from my own knowledge; the GovTech page has moved and couldn't be fetched, so verify before relying on it.*

**What it covers**

- Minimum standards that Singapore government digital services must meet, broadly covering:
  - **User experience and usability:** user-centred design, clear content, consistent design (supported by the Singapore Government Design System)
  - **Accessibility:** alignment with WCAG
  - **User feedback and service quality:** collecting and acting on user feedback, measuring user satisfaction
  - **Security and privacy:** in line with Singapore government security policies
  - **Performance and reliability:** page performance, availability, mobile responsiveness
- Supporting tools and guidance from GovTech, e.g., the design system, accessibility checking tools, and analytics for measuring performance.

**How it is assessed**

- Agencies **self-assess** their services against the standards, supported by GovTech checks and tooling, e.g., automated accessibility and performance checks.
- Pass or comply against each standard. No maturity levels.

**How software engineering teams can use it**

- **Find maturity:** Use it as a second reference alongside the GOV.UK Service Standard. It puts more weight on **measurable, often automated checks** (accessibility, performance, design consistency) than on reviews by assessment panels.
- **Find improvements:** Add automated accessibility and performance checks to CI. Measure user satisfaction routinely.
- **Watch out:** Specific to Singapore's government. For UK work, the GOV.UK and NHS Service Standards are what clients will expect.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **Medium** | Usability, accessibility, and performance standards apply to user-facing services. |
| Support | **Low–Medium** | User feedback and service quality measures are relevant. |
| Research | **Low** | Applies to user research methods only. |
| Data | **Low** | Little direct relevance, apart from analytics for measuring service performance. |
| ML/AI | **Low** | Applies only where AI is part of a citizen-facing service. |

**UK relevance:** Comparison only. Mainly useful for its emphasis on automated, measurable checks.

---

### 3.23 GOV.UK Service Standard (and NHS Service Standard)

**At a glance:** Government Digital Service (GDS), UK. Published in the GOV.UK Service Manual and maintained continuously. Service standard with **peer-led service assessments**. Free. **Directly relevant to us as a UK organization; kept here for future reference.** The **NHS Service Standard** (NHS England) is the health-specific version.

**What it covers**

- **GOV.UK Service Standard: 14 points**
  1. Understand users and their needs
  2. Solve a whole problem for users
  3. Provide a joined up experience across all channels
  4. Make the service simple to use
  5. Make sure everyone can use the service
  6. Have a multidisciplinary team
  7. Use agile ways of working
  8. Iterate and improve frequently
  9. Create a secure service which protects users' privacy
  10. Define what success looks like and publish performance data
  11. Choose the right tools and technology
  12. Make new source code open
  13. Use and contribute to open standards, common components and patterns
  14. Operate a reliable service
- **NHS Service Standard: 17 points.** It adapts the 14 above for health and care, and adds:
  - **Support a culture of care**
  - **Make your service clinically safe** (linked to DCB0129/DCB0160)
  - **Make your service interoperable** (e.g., FHIR and NHS interoperability standards)
- **Delivery phases:** **discovery → alpha → beta → live** (→ retirement), with guidance on what each phase should achieve.
- Related UK guidance: the **Technology Code of Practice** for technology spend and design decisions, and the **Government Design System**.

**How it is assessed**

- **Service assessments** at the end of alpha, beta, and before going live. A panel of experienced peers (e.g., delivery, user research, design, technical) reviews the service against each point, rating it met or not met, with recommendations.
- Required for central government services above certain thresholds (department or GDS-led, depending on scale). Many public bodies and NHS organizations run their own assessments against the standard.
- No maturity levels. The **phase** a service has reached shows how mature it is.

**How software engineering teams can use it**

- **Find maturity:** Ask which phase each product is really in, and whether it would pass an assessment for that phase. Points 6–14 are the most relevant to engineering (team, agile, iteration, security, metrics, technology, open source, open standards, reliability).
- **Find improvements:** Points not met become improvement goals. Point 10 (publish performance data) and point 14 (operate a reliable service) link naturally to DORA metrics and SRE practices.
- **Design ideas to borrow:**
  - **Peer assessment panels** of mixed disciplines are a proven way to run consistent, constructive assessments.
  - Assessing **by phase** fits work at different stages, including research.
- **Watch out:** Focuses on services and users, not engineering internals. Use it alongside the CAF (security) and our topic areas, not instead of them.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Service delivery | **High** | The standard was written for teams that deliver and run services. Expected by UK public sector and NHS clients. |
| Support | **Medium** | Point 14 (reliable service) and point 8 (iterate and improve) apply. Support often feeds user insight back to the team. |
| Research | **High** | Discovery and alpha are exactly where research and prototyping fit. The **best-fit framework for research teams** in this document. |
| Data | **Medium** | Points 9–13 apply to data products. Pair with the CDDO Data Maturity Assessment for data-specific maturity. |
| ML/AI | **Medium** | Applies to AI-enabled services. Add the Algorithmic Transparency Recording Standard and the NHS clinical safety standards where relevant. |


---

### 3.24 ITIL 4 (IT Service Management)

**At a glance:** PeopleCert (which acquired Axelos, the previous owner). ITIL 4 launched in 2019 and is still the most widely adopted version. **ITIL Version 5 has since been released**, with an upgrade route for ITIL 4–certified practitioners. Check what changed before standardizing on a version. Practice framework, with a maturity model available. The content is licensed and paid; certification is for individuals.

**What it covers**

- **Service Value System (SVS):** how all parts of an organization work together to create value through services. Its parts are:
  - **Seven guiding principles:** focus on value; start where you are; progress iteratively with feedback; collaborate and promote visibility; think and work holistically; keep it simple and practical; optimize and automate
  - **Governance**
  - **Service value chain** of six activities: plan, improve, engage, design & transition, obtain/build, deliver & support
  - **Practices**
  - **Continual improvement**
- **Four dimensions** of service management: organizations & people, information & technology, partners & suppliers, value streams & processes.
- **34 practices** in three groups: general management, service management, and technical management. The most relevant for engineering are:
  - **Incident management, problem management, service desk, service request management**
  - **Change enablement, release management, deployment management, service configuration management, IT asset management**
  - **Service level management, monitoring & event management, availability, capacity & performance, service continuity**
  - **Software development & management, infrastructure & platform management** (technical practices)
  - **Continual improvement, knowledge management, information security management, relationship and supplier management**
- ITIL 4 is much more compatible with **Agile, DevOps, and Lean** than ITIL v3 was. Change enablement explicitly supports delegated change authorities and automated, pre-approved standard changes.

**How it is assessed**

- **ITIL Maturity Model** (PeopleCert): rates **capability levels 1–5 per practice** and **organizational maturity levels 1–5** across the SVS.
  - Available as a **self-assessment** and as **formal assessments** by accredited assessment partners. The formal route comes in high-level and comprehensive scopes.
- **Individual certification:** ITIL Foundation, then Practitioner modules, Managing Professional, and Strategic Leader.
- No organizational certification for ITIL itself. For that, see **ISO/IEC 20000-1** (3.25).

**How software engineering teams can use it**

- **Find maturity:** Rate the practices the team actually performs, often incident, problem, change enablement, release and deployment, monitoring, and service level management. Ask whether each is ad hoc, defined, measured, or continually improved.
- **Find improvements:**
  - **Problem management** is often the weakest practice. Recurring incidents that are fixed but never analyzed are a classic gap; link to SRE postmortems.
  - **Change enablement:** move routine changes from CAB approval to **standard, pre-approved, automated changes** backed by pipeline controls. This links directly to the governance burden and CAB concerns in our topic list, and to DORA's finding that heavyweight change approval slows delivery without improving stability.
  - **Service level management:** align ITIL service levels with SRE-style SLOs, so there's one reliability target, not two.
- **Watch out:**
  - Applying ITIL as a rigid process can clash with DevOps. Use the guiding principles (*keep it simple and practical*, *optimize and automate*) to keep it light.
  - Map ITIL practices to existing engineering practices rather than running them in parallel.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Software engineering | **Medium** | Change enablement, release and deployment, and software development & management practices apply. Use it to agree interfaces with operations and support. |
| Service delivery | **High** | ITIL was designed for this team type. Service level, change, release, continuity, and relationship management are core. |
| Support | **High** | **Best-fit framework for support teams:** incident, problem, service desk, service request, knowledge management, and continual improvement. |
| Research | **Low** | Not applicable to exploratory work. |
| Data | **Medium** | Incident, problem, change, and service level practices apply to data platforms and data products run as services. |
| ML/AI | **Low–Medium** | Applies to AI services in production (incidents, changes, service levels). No model-specific practices; pair with MLOps and NIST AI RMF. |

---

### 3.25 ISO/IEC 20000-1 (Service Management System)

**At a glance:** ISO/IEC. ISO/IEC 20000-1:2018 is the current edition, with a 2024 amendment adding climate change considerations, as for other ISO management system standards. Standard for a management system. Paid to purchase. **Certifiable**: in the UK, through certification bodies accredited by **UKAS**.

**What it covers**

- Requirements for a **Service Management System (SMS)**. It uses ISO's common management system structure (clauses 4–10: context, leadership, planning, support, operation, performance evaluation, improvement), so it fits alongside **ISO/IEC 27001** and **ISO 9001**.
- **Clause 8 (Operation)** holds the service management processes:
  - **Service portfolio:** service delivery planning, control of parties involved, service catalogue management, asset management, configuration management
  - **Relationship and agreement:** business relationship management, service level management, supplier management
  - **Supply and demand:** budgeting and accounting for services, demand management, capacity management
  - **Service design, build and transition:** change management, service design and transition, release and deployment management
  - **Resolution and fulfilment:** incident management, service request management, problem management
  - **Service assurance:** service availability management, service continuity management, information security management
- Other parts in the series give guidance, e.g., **ISO/IEC 20000-2** (applying the SMS) and **ISO/IEC 20000-10** (concepts and vocabulary).
- **Relationship to ITIL:** ISO/IEC 20000-1 says *what* must be in place; ITIL describes *how* to do it. The standard doesn't require ITIL, but most organizations use ITIL to meet it.

**How it is assessed**

- **Third-party certification audit** by an accredited certification body. Typically a two-stage initial audit, yearly surveillance audits, and recertification every **three years**.
- Certification applies to a **defined scope**, e.g., specific services, locations, or teams.
- **Internal audits** and **management reviews** are required as part of the standard.
- No maturity levels. The result is certified or not, plus nonconformities and observations to address.
- Sometimes requested in **public sector and enterprise tenders** as evidence of mature service management.

**How software engineering teams can use it**

- **Find maturity:** Mostly organization-level. Teams can check whether the processes clause 8 requires exist for their services and are evidenced: e.g., defined service levels, a working change and release process, incident and problem records, continuity plans.
- **Find improvements:**
  - Gaps against clause 8 are concrete process gaps.
  - The **performance evaluation and improvement** clauses (9–10) push for measured, reviewed service performance. This links to DORA metrics and SLO reporting.
- **When to pursue it:** Only if clients or tenders require certification, or if we're already running an ISO 27001 management system and want an integrated one. Otherwise, use ITIL and SRE practices without the certification overhead.
- **Watch out:** Certification audits are evidence-heavy. Keep the scope tight and generate evidence from tools (ticketing, CI/CD, monitoring) rather than writing documents by hand.

**Applicability by team type**

| Team type | Relevance | Notes |
|---|---|---|
| Software engineering | **Low–Medium** | Release, deployment, and change management requirements affect how code reaches production. Otherwise mostly indirect. |
| Service delivery | **High** | The standard is written for organizations that deliver services. Service levels, continuity, capacity, and supplier management all apply. |
| Support | **High** | Incident, service request, and problem management are core requirements, along with evidence of continual improvement. |
| Research | **Low** | Not applicable. |
| Data | **Medium** | Applies where data platforms or data products are delivered as services within the certified scope. |
| ML/AI | **Low–Medium** | Applies to AI services in production within scope. For AI-specific management systems, see **ISO/IEC 42001** (3.18), which has the same structure and can be integrated. |


## 4. Summary: Relevance by Team Type

H = High, M = Medium, L = Low (combined ratings such as M–H are shown as written above).

| Model | SW eng | Service delivery | Support | Research | Data | ML/AI |
|---|---|---|---|---|---|---|
| CMMI v3.0 | H | H | M–H | L | M | M |
| DORA | H | H | M | L | M–H | M–H |
| SPACE / DevEx | H | H | M–H | H | H | H |
| NIST SSDF (+800-218A) | H | H | M | L–M | M | H |
| CISA Secure by Design | H | H | M | L | M | M–H |
| OWASP SAMM | H | H | M | L | M | M |
| BSIMM | M | M | L–M | L | L–M | L–M |
| NIST CSF 2.0 | M | H | H | L | M–H | M |
| SLSA | H | H | L | L | M | M–H |
| SP 800-161 / SBOM | H | H | M | L | M | H |
| Well-Architected | H | H | M | L–M | H | H |
| SRE | H | H | H | L | H | M–H |
| ISO/IEC 25010 family | M | M | L–M | L | H (25012) | H (25059) |
| ISO 12207 / 33001 | M | M | L–M | L | L–M | L–M |
| CNCF Platform Maturity | M–H | M–H | L–M | M | H | H |
| DoD DevSecOps | M (H for gov) | H/M | M | L | M | M |
| FinOps | M–H | H | L | M | H | H |
| NIST AI RMF / ISO 42001 | M | M | L–M | M–H | H | H |
| NHS Digital Maturity Assessment | M | M | L–M | L | M–H | M |
| NCSC CAF v4.0 | H | H | H | L | H | M |
| MAS TRM (comparison) | H | H | H | L | M | L–M |
| GovTech DSS (comparison) | M | M | L–M | L | L | L |
| GOV.UK / NHS Service Standard | H | H | M | H | M | M |
| ITIL 4 | M | H | H | L | M | L–M |
| ISO/IEC 20000-1 | L–M | H | H | L | M | L–M |

**What stands out**

- **Service delivery** and **software engineering** teams are well served by most models.
- **Support** teams are served best by SRE, NIST CSF (Detect, Respond, Recover), and SPACE/DevEx. Most development-focused models only partly apply. **ITIL 4** (3.24) is the best fit for support practices, with **ISO/IEC 20000-1** (3.25) if certification is needed.
- **Research** teams are poorly served by maturity models in general. The **GOV.UK / NHS Service Standard** phases (discovery and alpha) fit them best, followed by SPACE/DevEx and NIST AI RMF. Assess lightly, mainly on how ready work is to move from research into production.
- **Support** and **service delivery** teams in the UK should treat the **NCSC CAF** as their main security and resilience reference, as UK public-sector and NHS clients increasingly expect it.
- **Data** teams need data-specific additions: ISO/IEC 25012, the Well-Architected data lenses, SRE pipeline practices, and a data management model (see section 5).
- **ML/AI** teams are well covered for governance and cost (NIST AI RMF, ISO 42001, FinOps, Well-Architected ML lenses), but need an MLOps maturity model for delivery practice (see section 5).

## 5. Gaps: Additional Models Worth Considering

These are outside the current reference list, but would fill gaps for non-software teams:

| Model | Fills gap for | What it offers |
|---|---|---|
| **DAMA-DMBOK** (DAMA International) | Data | Data management body of knowledge covering governance, quality, metadata, architecture, and more |
| **EDM Council DCAM** | Data | Data management capability assessment model with scored maturity |
| **Google MLOps maturity levels** | ML/AI | Levels 0–2 of ML pipeline automation (manual, then ML pipeline automation, then CI/CD for pipelines) |
| **Microsoft MLOps maturity model** | ML/AI | Five-level MLOps maturity model covering people, model creation, release, and integration |
| **OWASP Top 10 for LLM Applications** | ML/AI | Security risks specific to LLM-based applications (prompt injection, data poisoning, etc.) |
| **NASA Technology Readiness Levels (TRL)** | Research | A 1–9 scale of how close a technology is to real use. Useful for assessing *outputs*, not teams |
| **ISO/IEC 5338** | ML/AI | AI system lifecycle processes, extending 12207 |

## 6. References

**Core models**

- CMMI: https://cmmiinstitute.com/cmmi
- DORA: https://dora.dev
- DORA Quick Check: https://dora.dev/quickcheck/
- *Accelerate* (Forsgren, Humble, Kim, 2018). IT Revolution Press
- SPACE framework: https://queue.acm.org/detail.cfm?id=3454124
- DevEx framework: https://queue.acm.org/detail.cfm?id=3595878
- NIST SP 800-218 SSDF: https://csrc.nist.gov/projects/ssdf
- NIST SP 800-218A (SSDF profile for generative AI): https://csrc.nist.gov/pubs/sp/800/218/a/final
- CISA Secure Software Development Attestation Form: https://www.cisa.gov/secure-software-attestation-form
- CISA Secure by Design: https://www.cisa.gov/securebydesign
- CISA Secure by Design Pledge: https://www.cisa.gov/securebydesign/pledge
- OWASP SAMM: https://owaspsamm.org
- BSIMM: https://www.bsimm.com
- NIST Cybersecurity Framework 2.0: https://www.nist.gov/cyberframework
- SLSA: https://slsa.dev
- NIST SP 800-161r1: https://csrc.nist.gov/pubs/sp/800/161/r1/final
- CISA SBOM: https://www.cisa.gov/sbom
- NTIA SBOM Minimum Elements: https://www.ntia.gov/report/2021/minimum-elements-software-bill-materials-sbom
- AWS Well-Architected: https://aws.amazon.com/architecture/well-architected/
- AWS Well-Architected Tool: https://aws.amazon.com/well-architected-tool/
- Azure Well-Architected: https://learn.microsoft.com/en-us/azure/well-architected/
- Google Cloud Well-Architected: https://cloud.google.com/architecture/framework
- Google SRE books: https://sre.google/books/
- ISO/IEC 25010: https://www.iso.org/standard/78176.html
- ISO/IEC/IEEE 12207: https://www.iso.org/standard/63712.html
- ISO/IEC 33001: https://www.iso.org/standard/54175.html
- CNCF Platform Engineering Maturity Model: https://tag-app-delivery.cncf.io/whitepapers/platform-eng-maturity-model/
- DoD CIO Library (DevSecOps, Software Modernization): https://dodcio.defense.gov/library/
- FinOps Framework: https://www.finops.org/framework/
- FinOps Maturity Model: https://www.finops.org/framework/maturity-model/
- NIST AI RMF: https://www.nist.gov/itl/ai-risk-management-framework
- NIST AI 600-1 (Generative AI Profile): https://doi.org/10.6028/NIST.AI.600-1
- ISO/IEC 42001: https://www.iso.org/standard/81230.html

**UK and Singapore frameworks (sections 3.19–3.23)**

- NHS Digital Maturity Assessment: https://www.england.nhs.uk/digitaltechnology/digital-maturity-assessment/
- NCSC Cyber Assessment Framework: https://www.ncsc.gov.uk/collection/cyber-assessment-framework
- MAS Technology Risk Management Guidelines: https://www.mas.gov.sg/regulation/guidelines/technology-risk-management-guidelines
- GovTech Digital Service Standards: search tech.gov.sg (the page has moved; current URL not confirmed)
- GOV.UK Service Standard: https://www.gov.uk/service-manual/service-standard
- NHS Service Standard: https://service-manual.nhs.uk/standards-and-technology/service-standard

**Service management (sections 3.24–3.25)**

- ITIL (Axelos / PeopleCert): https://www.axelos.com/certifications/itil-service-management
- ITIL certifications (PeopleCert): https://www.peoplecert.org/browse-certifications/it-governance-and-service-management/ITIL-1
- ISO/IEC 20000-1:2018: https://www.iso.org/standard/70636.html
- UKAS (find accredited certification bodies): https://www.ukas.com

**Gap-filling models (section 5)**

- OWASP Top 10 for LLM Applications: https://genai.owasp.org
- DAMA International (DMBOK): https://www.dama.org
- EDM Council (DCAM): https://edmcouncil.org
- Google MLOps (continuous delivery and automation pipelines): https://cloud.google.com/architecture/mlops-continuous-delivery-and-automation-pipelines-in-machine-learning
- Microsoft MLOps maturity model: https://learn.microsoft.com/en-us/azure/architecture/ai-ml/guide/mlops-maturity-model
- ISO/IEC 25012, 25059, 5338, 23894, 42005: search the ISO catalogue (iso.org)
