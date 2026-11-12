# Engineering Maturity Model

## Aim

This lean maturity model tackles 5 aspects; Architecture and design, Development and quality, Delivery and change, Operations and observability, and Security and resilience, across 3 verticals: people, process and technology. The model is aimed to be a self assessment carried out by teams and based on CMMI, using their existing maturity levels.

## Architecture and design

### People

| Level | Name | In plain English | Signals |
| --- | --- | --- | --- |
| 1 | Initial | Design knowledge sits with one or two people, and others rarely understand why the system is shaped the way it is. | Key-person dependency for design questions; no shared diagrams |
| 2 | Managed | The team has a named owner for design decisions, and everyone takes part in discussing significant changes. | Named design owner; design discussions in team rituals; up-to-date context diagram |
| 3 | Defined | The team has trained design skills and works with architects and other teams, using the organisation's architecture principles and patterns. | Architecture training completed; architects engaged as enablers, not gatekeepers; cross-team design forums attended |
| 4 | Quantitatively Managed | The team uses evidence such as Well-Architected findings and coupling data to decide where to build design skills and effort. | Skills matrix covers design; design effort targeted at high-risk areas from review data |
| 5 | Optimising | Team members mentor others, contribute to shared patterns, and learn from experiments with new design approaches. | Patterns or guidance contributed to the organisation; design learning sessions led for other teams |

### Process

| Level | Name | In plain English | Signals |
| --- | --- | --- | --- |
| 1 | Initial | Design decisions are made informally and are not recorded, so the reasons are lost over time. | No decision records; non-functional needs not written down |
| 2 | Managed | The team records significant decisions and agrees the non-functional requirements that matter for the service. | Architecture decision records (ADRs) in the repo; agreed NFRs (e.g. performance, availability, maintainability) |
| 3 | Defined | The team follows the organisation's design review process, scaled to risk, and aligns choices with the Technology Code of Practice and Service Standard points 11 and 13. | Design reviews held for significant changes; ADRs in the shared template; reuse of common components justified |
| 4 | Quantitatively Managed | NFRs have measurable targets, and the team tracks architecture risk items and technical debt to guide design work. | NFR targets with measurements; architecture risk and debt trend; high-risk review items tracked to closure |
| 5 | Optimising | The team regularly revisits its architecture against outcomes, tries alternative designs safely, and shares what it learns. | Architecture retrospectives; measured results from design experiments; lessons shared across teams |

### Technology

| Level | Name | In plain English | Signals |
| --- | --- | --- | --- |
| 1 | Initial | Technology is chosen case by case, and the system is tightly coupled and hard to change safely. | Bespoke components without reason; changes in one area often break another |
| 2 | Managed | The team keeps current architecture diagrams and an inventory of its components and dependencies. | Diagrams kept with the code; component and dependency inventory; clear service boundaries |
| 3 | Defined | The service is built on the organisation's shared platforms and patterns, with loosely coupled components that can change independently. | Shared platform and golden-path templates in use; APIs between components; open standards used |
| 4 | Quantitatively Managed | Automated checks and regular Well-Architected reviews measure how the architecture performs against its targets. | Architecture fitness functions in CI; count of high-risk review items over time; cost and performance per component |
| 5 | Optimising | The architecture evolves through measured experiments, and improvements are contributed back to shared platforms. | Results from architecture spikes and trials; contributions to shared platforms or patterns |

## Development and quality

### People

| Level | Name | In plain English | Signals |
| --- | --- | --- | --- |
| 1 | Initial | Developers work in their own way, and code quality depends on who wrote it. | No agreed coding conventions; knowledge silos in parts of the codebase |
| 2 | Managed | The team agrees coding standards, reviews each other's code, and shares knowledge of the codebase. | Team coding standards; review spread across the team; pairing or mob sessions |
| 3 | Defined | The team is trained in the organisation's engineering standards and testing practices, and adapts them on purpose to its context. | Engineering standards training completed; testing skills across the team; communities of practice attended |
| 4 | Quantitatively Managed | The team uses developer experience surveys and system data to find friction and target skills and support. | DevEx or SPACE survey results tracked; review wait time and build time trends; actions taken from survey results |
| 5 | Optimising | The team experiments with ways of working, measures the effect on quality and flow, and shares what works. | Before-and-after measures from experiments; talks or guides shared with other teams |

### Process

| Level | Name | In plain English | Signals |
| --- | --- | --- | --- |
| 1 | Initial | Testing and review happen when there's time, and "done" means different things to different people. | No definition of done; defects often found by users |
| 2 | Managed | Every change is peer reviewed, and the team works to an agreed definition of done and test approach. | Required review on the main branch; definition of done; test approach written down |
| 3 | Defined | The team follows the organisation's quality standards and test strategy, including automated testing for agreed quality characteristics. | Shared test strategy in use; quality characteristics (ISO/IEC 25010) chosen for the product; quality gates agreed |
| 4 | Quantitatively Managed | The team sets quality targets and tracks escaped defects, rework, and test results to guide its priorities. | Escaped defect rate; rework rate; flaky test rate; quality targets reviewed regularly |
| 5 | Optimising | The team analyses the root causes of defects, changes its practices to prevent whole types of fault, and shares the changes. | Defect root-cause analysis; falling repeat-defect rate; practice changes adopted by other teams |

### Technology

| Level | Name | In plain English | Signals |
| --- | --- | --- | --- |
| 1 | Initial | Code may not all be in version control, and builds and tests rely on manual steps on individual machines. | Manual builds; few or no automated tests; "works on my machine" problems |
| 2 | Managed | All code is in version control, CI runs automated tests on every change, and failures are fixed quickly. | CI on every pull request; unit and integration tests; CI pass rate tracked |
| 3 | Defined | The team uses the organisation's standard development tooling, with linting, static analysis, and automated tests built into CI. | Standard CI templates; static analysis and linting results; reproducible development environments |
| 4 | Quantitatively Managed | The team measures feedback loop speed and test effectiveness, and keeps them within agreed targets. | Build and test time against targets; coverage and mutation testing trends; flaky test dashboard |
| 5 | Optimising | The team trials new tools and techniques, such as AI-assisted development, measures the impact, and shares the results. | Tool trial results with measured effect; AI coding assistant usage reviewed; tooling improvements reused elsewhere |

## Delivery and change

### People

| Level | Name | In plain English | Signals |
| --- | --- | --- | --- |
| 1 | Initial | Releases rely on one or two people who know the steps, or are handed to another team. | Release knowledge held by individuals; hand-offs to separate release teams |
| 2 | Managed | The team owns its releases, and more than one person can release and roll back changes. | Release rota or shared ownership; several people have released recently |
| 3 | Defined | The whole team is trained to deliver through the organisation's standard pipeline, and owns changes from commit to production. | Everyone can release; delivery training completed; no hand-off needed to reach production |
| 4 | Quantitatively Managed | The team reviews its DORA metrics together and uses them to decide where to improve its delivery skills and habits. | DORA metrics discussed in retrospectives; improvement actions linked to the metrics |
| 5 | Optimising | The team coaches other teams on delivery practice and shares the results of its experiments. | Delivery coaching provided; experiment write-ups shared |

### Process

| Level | Name | In plain English | Signals |
| --- | --- | --- | --- |
| 1 | Initial | Changes are batched into large, infrequent releases, with approval and planning done case by case. | Big-bang releases; release dates slip; no rollback plan |
| 2 | Managed | The team plans its releases, works in small batches, and has an agreed way to approve and roll back changes. | Release checklist; small, frequent merges; rollback steps agreed |
| 3 | Defined | The team follows the organisation's change process, with routine changes pre-approved through pipeline controls instead of a change board. | Standard (pre-approved) change types; CAB used only for high-risk changes; change records generated by the pipeline |
| 4 | Quantitatively Managed | The team sets targets for both delivery speed and stability, and uses them to plan and predict releases. | Lead time and deployment frequency targets alongside change fail rate and recovery time; release predictability tracked |
| 5 | Optimising | The team keeps removing friction from its change process, measures the effect, and shares what it learns. | Approval steps removed with evidence; improved flow over time; changes adopted by other teams |

### Technology

| Level | Name | In plain English | Signals |
| --- | --- | --- | --- |
| 1 | Initial | Builds and deployments are partly manual, so releases are risky and infrequent. | Releases monthly or less often; deploys take a lot of manual work |
| 2 | Managed | Deployment is scripted and repeatable, and every environment is deployed the same way. | Scripted deployments; infrastructure as code for main environments; rollback is scripted |
| 3 | Defined | The team uses the organisation's standard pipeline and golden path, with automated tests and security scans gating releases. | Pipeline template in use; automated release gates; deployments need no manual steps |
| 4 | Quantitatively Managed | DORA metrics are collected automatically from the pipeline and shown on a dashboard against team targets. | Deployment frequency, lead time, change fail rate, recovery time, and rework rate on a dashboard |
| 5 | Optimising | The team uses advanced techniques such as progressive delivery and feature flags, and shares measured improvements. | Canary or blue-green releases; feature flags; measured improvement over time; practices adopted by other teams |

## Operations and observability

### People

| Level | Name | In plain English | Signals |
| --- | --- | --- | --- |
| 1 | Initial | Problems in live services are fixed by whoever is around, often the same few people. | No on-call arrangement; the same people are called out every time |
| 2 | Managed | The team owns its live services, with an agreed on-call rota and clear incident roles. | On-call rota; incident roles (e.g. lead, communications); support contact known |
| 3 | Defined | The team is trained in the organisation's incident and on-call practices, and learns from incidents without blame. | Incident training completed; blameless reviews; fair on-call load across the team |
| 4 | Quantitatively Managed | The team measures on-call load and toil, and acts to keep them within agreed limits. | Pages per shift; toil below about 50% of operational time; well-being survey results |
| 5 | Optimising | The team reduces toil through engineering, and shares operational learning with other teams. | Falling toil trend; automation contributed back; incident learning sessions for other teams |

### Process

| Level | Name | In plain English | Signals |
| --- | --- | --- | --- |
| 1 | Initial | Incidents are handled ad hoc by whoever notices, and nothing is written down afterwards. | No incident records; no runbooks |
| 2 | Managed | The team logs incidents, follows basic runbooks, and reviews major incidents. | Incident tickets; runbooks in repo; review notes |
| 3 | Defined | The team follows the organisation's incident and blameless postmortem process, with SLOs for key user journeys. | Postmortems in the shared template; SLOs defined; problem records for recurring incidents |
| 4 | Quantitatively Managed | Error budgets and recovery time targets guide decisions on whether to release or stabilise. | Error budget policy applied; recovery time trend against target; postmortem actions completed on time |
| 5 | Optimising | The team analyses incident trends to remove whole classes of failure, and shares the fixes. | Recurring-incident rate falling; learnings adopted by other teams |

### Technology

| Level | Name | In plain English | Signals |
| --- | --- | --- | --- |
| 1 | Initial | Monitoring is limited, and the team often hears about problems from users first. | Few or no alerts; issues reported by users before the team notices |
| 2 | Managed | The team collects logs and metrics for its services and has alerts for the main failures. | Central logging; basic dashboards; alerts routed to on-call |
| 3 | Defined | The team uses the organisation's observability platform, with logs, metrics, and traces, and alerts based on symptoms users see. | Distributed tracing; symptom-based alerts; SLO dashboards for key journeys |
| 4 | Quantitatively Managed | SLIs and SLOs are measured automatically, and alert quality and detection time are tracked. | Automated SLO reporting; time to detect; ratio of actionable alerts |
| 5 | Optimising | The team automates diagnosis and recovery where it's safe, and improves its observability from incident evidence. | Automated remediation for known failures; observability gaps closed after incidents; tooling shared with others |

## Security and resilience

### People

| Level | Name | In plain English | Signals |
| --- | --- | --- | --- |
| 1 | Initial | Security is seen as someone else's job, and team members have little security training. | No security training; security questions passed to a central team |
| 2 | Managed | Everyone completes basic security training, and the team has a named security champion. | Training records; named security champion; security covered in team discussions |
| 3 | Defined | The team is trained in the organisation's secure coding, threat modelling, and incident response practices, and owns its service's security. | Secure coding and threat modelling training; champion network attended; team leads its own security work |
| 4 | Quantitatively Managed | The team uses evidence from findings and exercises to target its security skills and awareness. | Training linked to recurring vulnerability types; exercise results tracked over time |
| 5 | Optimising | Team members lead security learning across teams and help shape the organisation's security practice. | Sessions run for other teams; contributions to organisational security guidance |

### Process

| Level | Name | In plain English | Signals |
| --- | --- | --- | --- |
| 1 | Initial | Security and resilience are considered late, often only when an audit or incident forces it. | No threat model; no recovery plan; vulnerabilities fixed only when chased |
| 2 | Managed | The team threat models significant changes, fixes vulnerabilities to agreed timescales, and has a recovery plan. | Threat models in the repo; vulnerability fix timescales; recovery plan with RTO and RPO |
| 3 | Defined | The team follows the organisation's secure development lifecycle and self-assesses its services against the NCSC CAF outcomes. | CAF contributing outcomes rated for the service; secure development practices (SSDF/SAMM) in use; disaster recovery tested regularly |
| 4 | Quantitatively Managed | The team tracks vulnerability fix times, CAF outcome gaps, and recovery test results against targets. | Time to fix by severity; CAF outcomes achieved against target profile; restore test success and timing |
| 5 | Optimising | The team removes whole classes of vulnerability and failure, runs regular exercises, and shares the lessons. | Vulnerability classes eliminated (e.g. memory-safe languages, secure defaults); game days or cyber exercises; lessons shared |

### Technology

| Level | Name | In plain English | Signals |
| --- | --- | --- | --- |
| 1 | Initial | Security checks and backups are manual or missing, and dependencies aren't tracked. | No security scanning; secrets in code or configuration; untested backups |
| 2 | Managed | The team scans dependencies, keeps secrets out of code, and backs up its data automatically. | Dependency scanning; secrets manager in use; automated backups; MFA on admin access |
| 3 | Defined | The team uses the organisation's security tooling, with code, dependency, and secret scanning in the pipeline, and SBOMs and provenance for each release. | SAST and secret scanning in CI; SBOM per release; SLSA Build Level 2 provenance; secure configuration baselines |
| 4 | Quantitatively Managed | Security and resilience measures are collected automatically and reported against targets. | Vulnerability dashboard; patching and fix-time trends; automated restore tests with timings |
| 5 | Optimising | The team hardens its supply chain and resilience through automation and experiments, and shares improvements with others. | SLSA Build Level 3; automated deploy-time policy checks; chaos or failover tests; tooling reused by other teams |
