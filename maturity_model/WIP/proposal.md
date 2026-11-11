# Engineering Maturity Model: Proposed Topic Areas

*Draft v0.1 for team discussion, November 2026*

## 1. Purpose and Approach

We want a shared, repeatable way to see where our engineering practices stand today, decide where to invest, and track progress. We won't invent a model from scratch. We'll **borrow from established industry and government frameworks**: they give us credible structure, common vocabulary, and benchmarks we can compare against. This document proposes the **topic areas** the model should cover and names the frameworks behind each one. It is a starting point, not a final design; detail will come as we go.

### Principles 

These principles guide engineering choices across the Civil Service, the wider UK public sector, and delivery partners. 

* **Put people first**: Understand what people need and build services that everyone can use. 
* **Own the whole service**: Give people clear responsibility for keeping each service useful and safe throughout its life. 
* **Build quality in**: Design and test for reliable, secure services from the start, and keep checking them as they run. 
* **Keep things simple**: Reuse proven solutions, and avoid extra features, tools, and steps that add little value. 
* **Let risk guide effort**: Choose checks and improvements that match what could go wrong and how much harm it could cause. 
* **Deliver small, safe changes**: Make small improvements often, check that they work, and be ready to undo them. 
* **Learn and share openly**: Help each other learn, discuss mistakes without blame, and share what works across teams. 
* **Measure what matters**: Check whether changes improve the whole service for people and make public money go further. 

These proposed EPF principles are informed by: 

* NHS Digital engineering principles, covering quality, simplicity, learning, small changes, respect, and the whole service. 
* Government Secure by Design principles, covering ownership, risk, usable protection, and continued checks throughout a service's life. 

### Engineering Maturity Model (EMM) 

The purposefully small and lean model has five aspects, each covering a different part of engineering practice. 

| Aspect | The simple question it asks |
| --- | --- |
| Architecture and design | Are we designing services that meet needs and can evolve? |
| Development and quality | Can we build software confidently and check that it works? |
| Delivery and change | Can we release useful changes safely and reliably? |
| Operations and observability | Can we understand how services are behaving and respond when something goes wrong? |
| Security and resilience | Can we protect services and help them withstand and recover from disruption? |

 

For every aspect, expectations cover three things together: 

* People: skills, responsibilities, ownership, and learning. 
* Process (governance): repeatable ways of working, clear decisions, and appropriate oversight. 
* Technology: tools and technical capabilities that support the practice. 

A tool alone does not make a practice mature. Teams also need the skills, ownership, and ways of working to use it effectively. 

The maturity model will be made of Five cumulative levels 

These levels are inspired by CMMI. Each level builds on the expectations of the levels before it. 

Assess each aspect independently, using evidence of everyday practice. A team might be at level 3 for development and quality and level 2 for operations and observability. Keep that profile visible rather than hiding it in a single average score. Level 5 is not a universal target. Choose a target for each aspect that fits the service's needs and risk. A critical public service may need different capabilities from a small, short-lived prototype. 

| Level | Name | In plain English |
| --- | --- | --- |
| 1 | Initial | Work depends heavily on individual effort, and responses are often reactive. |
| 2 | Managed | Teams have owners, basic plans, and repeatable practices for their work. |
| 3 | Defined | Trained teams use shared standards and agreed ways of working, adapted to their context. |
| 4 | Quantitatively Managed | Teams use reliable measurements and analysis to understand performance and guide decisions. |
| 5 | Optimising | Teams continually test improvements, measure their effects, and share what they learn. |



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
