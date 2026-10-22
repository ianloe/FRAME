# FRAME

![FRAME logo](FRAME-logo.png)

**A governance framework for enterprise AI deployment**

FRAME is a domain-agnostic governance framework for organisations deploying AI systems in production. It provides a structured approach to defining, operating, and evaluating AI initiatives across enterprise environments, with particular application to autonomous and agentic AI deployments.

FRAME was developed through direct enterprise experience across ASEAN operations and is positioned as a practitioner framework: built to be applied, not merely referenced.

---

## The Five Dimensions

FRAME organises AI governance across five dimensions. Each dimension addresses a distinct governance concern and is designed to be assessed independently or as part of a full framework review.

### Focus
Defines the domain, scope, and intended outcome of the AI deployment. Governance begins with clarity about what the AI system is for, what problem it is solving, and what a successful outcome looks like. Without explicit Focus, measurement is arbitrary and accountability is diffuse.

### Roles
Establishes who is responsible for what across the AI deployment lifecycle. This includes human oversight responsibilities, escalation paths, accountability for AI outputs, and the boundaries between human and AI decision authority. Roles must be defined before deployment, not assigned after an incident.

### Authority
Defines the decision rights of the AI system: what it can act on autonomously, what requires human confirmation, and what is outside its permitted scope entirely. Authority boundaries are the primary mechanism for managing risk in agentic deployments and must be explicit, documented, and enforced technically where possible.

### Metrics
Specifies how the AI system's performance and contribution will be measured. FRAME distinguishes between activity metrics (what the system does) and outcome metrics (what changes as a result). Governance-grade measurement is anchored to domain outcomes, not system throughput. Metrics must be defined before deployment and reviewed at each appraisal cycle.

### Evaluation
Establishes the cadence, method, and accountability for ongoing review of the AI system's performance, its alignment with organisational objectives, and its governance compliance. Evaluation is not a one-time post-deployment check. It is a continuous governance function that includes adoption tracking, outcome assessment, and framework review.

---

## When to Use FRAME

FRAME is applicable across AI deployment types, including:

- Conversational AI and copilot deployments
- Agentic and autonomous AI systems
- AI-assisted decision support in regulated functions
- Cross-functional AI platforms serving multiple business units

It is particularly well suited to enterprise environments where AI deployments span organisational boundaries, involve consequential decisions, or operate with significant autonomy.

---

## How to Use This Repository

| Document | Purpose |
|---|---|
| [Specification](docs/specification.md) | Full framework definition, dimension descriptions, and governance requirements |
| [Practitioner Guide](docs/practitioner-guide.md) | Step-by-step guidance for applying FRAME in an enterprise deployment |
| [Maturity Assessment](docs/maturity-assessment.md) | Self-assessment tool for evaluating governance maturity across each dimension |
| [Implementation Checklist](docs/implementation-checklist.md) | Pre-deployment and ongoing governance checklist |

---

## Relationship to AAEF

FRAME provides the governance envelope for AI deployments. The [AI Agent Evaluation Framework (AAEF)](https://github.com/ianloe/AAEF) operates within that envelope, providing a structured approach to evaluating individual AI agents as operational contributors rather than software tools.

The two frameworks are designed to be used together. FRAME sets the governance context. AAEF provides the evaluation methodology for agents operating within it.

---

## Citing FRAME

If you reference FRAME in published work, please cite as follows:

> Loe, I. (2025). *FRAME: A governance framework for enterprise AI deployment*. Tactics Solutions. https://github.com/ianloe/FRAME

---

## Licence

This work is licensed under the [Creative Commons Attribution-NonCommercial 4.0 International Licence](https://creativecommons.org/licenses/by-nc/4.0/).

You are free to use, adapt, and share this framework for non-commercial purposes, provided you give appropriate credit. For commercial use, including consulting engagements, training programmes, and advisory services, please contact Tactics Solutions.

---

## About the Author

**Ian Loe** is  is an AI governance practitioner and enterprise technology leader with deep experience in AI strategy, cybersecurity, and digital transformation across ASEAN. He is the founder of Tactics Solutions, an advisory and speaking practice focused on AI governance and digital transformation, and the author of *The Agency Mandate*, a forthcoming book on governance frameworks for autonomous AI deployment.

- Website: [Tactics Solutions](https://tacticssolutions.com)
- Writing: [ianloe.medium.com](https://ianloe.medium.com)
- Framework companion: [AAEF](https://github.com/ianloe/AAEF)
