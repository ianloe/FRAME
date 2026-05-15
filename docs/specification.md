# FRAME: Framework Specification

**Version 1.0**
**Author: Ian Loe, Tactics Solutions**

---

## 1. Purpose and Scope

FRAME is a governance framework for enterprise AI deployment. It provides a structured, domain-agnostic approach to defining, operating, and evaluating AI systems in production environments, with particular application to autonomous and agentic deployments.

FRAME addresses a gap in existing governance approaches. Most AI governance guidance available to practitioners is either too abstract to operationalise (principle-level ethics frameworks) or too narrow to generalise (single-use-case compliance checklists). FRAME occupies the middle ground: structured enough to enforce governance discipline, flexible enough to apply across deployment types, industries, and organisational contexts.

The framework is applicable to:

- Conversational AI and copilot deployments
- Agentic and autonomous AI systems
- AI-assisted decision support in regulated functions
- Cross-functional AI platforms serving multiple business units
- AI systems operating as components of larger orchestrated pipelines

FRAME is not a technical standard. It does not specify model architectures, infrastructure configurations, or software engineering practices. It is a governance framework: it specifies what decisions must be made, who must make them, how performance must be measured, and how ongoing accountability must be maintained.

---

## 2. Foundational Principles

FRAME is built on four foundational principles that inform the design of each dimension.

### 2.1 Governance Precedes Deployment

AI governance is not a post-deployment activity. It is a pre-condition for deployment. Organisations that deploy first and govern later systematically expose themselves to accountability gaps, measurement failures, and incidents that could have been prevented by upstream governance discipline.

FRAME requires that each of its five dimensions is addressed before an AI system enters production. Partial completion of the framework is a deployment risk, not a minor compliance gap.

### 2.2 Outcomes Over Activity

Governance-grade measurement is anchored to what changes as a result of the AI system's operation, not to what the AI system does. Activity metrics have their place in operational monitoring. They are not sufficient for governance accountability.

Every FRAME deployment must define its outcome measures before deployment. Post-hoc rationalisation of metrics is a governance failure.

### 2.3 Accountability Is Human

AI systems do not hold accountability. Humans do. FRAME requires that for every AI deployment, there is an identifiable human or human body that is accountable for the system's outcomes, its governance compliance, and its ongoing operation. Distributed accountability is no accountability.

### 2.4 Governance Is Continuous

Deployment is not the end of the governance lifecycle. It is the beginning of the operational governance phase. FRAME evaluation is not a one-time post-deployment check. It is a continuous function, executed on a defined cadence, with formal review and documented outcomes.

---

## 3. Framework Architecture

FRAME organises AI governance across five dimensions. The dimensions are not sequential steps. They are concurrent governance concerns, each of which must be addressed and maintained throughout the deployment lifecycle.

```
┌─────────────────────────────────────────────┐
│                   FRAME                     │
├──────────┬──────────┬───────────┬───────────┤
│  Focus   │  Roles   │ Authority │  Metrics  │
│          │          │           │           │
│  What    │  Who     │  Scope    │  How      │
│  and why │  does    │  of       │  success  │
│          │  what    │  action   │  measured │
└──────────┴──────────┴─────────────────────┐ │
│                  Evaluation               │ │
│          Continuous governance review     │ │
└───────────────────────────────────────────┘─┘
```

Each dimension has a defined set of governance requirements, documented in sections 4 through 8 below.

---

## 4. Dimension One: Focus

### 4.1 Definition

Focus defines the domain, scope, and intended outcome of the AI deployment. It establishes what the AI system is for, what problem it is solving, what population it serves, and what a successful outcome looks like.

### 4.2 Governance Requirements

An AI deployment satisfies the Focus dimension when the following are documented and approved before deployment:

**4.2.1 Domain Statement**
A clear description of the operational domain in which the AI system will operate. The domain statement should be specific enough to bound the system's scope and exclude adjacent domains in which the system is not authorised to operate.

*Example: "Customer service enquiry handling for residential property management, covering maintenance requests, lease queries, and payment status. Excludes legal disputes, complaints escalations, and any communication involving third-party contractors."*

**4.2.2 Problem Definition**
A statement of the specific problem the AI system is deployed to address. The problem definition should describe the current state, the gap or inefficiency being addressed, and why AI is the appropriate intervention.

**4.2.3 Outcome Statement**
An explicit definition of what success looks like, expressed in terms of measurable changes to operational outcomes, customer experience, or organisational capability. The outcome statement is the basis for the Metrics dimension and must be defined before metrics are selected.

**4.2.4 Scope Boundaries**
Explicit definition of what is in scope and out of scope for the AI system. Scope boundaries should address: the populations the system serves, the data it is permitted to access, the decisions it is permitted to influence, and the channels or interfaces through which it operates.

**4.2.5 Stakeholder Alignment**
Documentation that the Focus definition has been reviewed and approved by the relevant business owner, the technology accountable owner, and any compliance or risk function with oversight of the domain.

### 4.3 Common Failures

- Outcome statements that describe AI activity ("the system will process 10,000 queries per month") rather than operational outcomes ("customer query resolution time will decrease by 20%")
- Scope boundaries that are too broad to enforce, leaving the system's actual operating domain undefined in practice
- Focus definition completed by the technology team without business owner review or approval

---

## 5. Dimension Two: Roles

### 5.1 Definition

Roles establishes who is responsible for what across the AI deployment lifecycle. It defines human oversight responsibilities, escalation paths, accountability for AI outputs, and the boundaries between human and AI decision authority.

### 5.2 Governance Requirements

An AI deployment satisfies the Roles dimension when the following are documented and assigned before deployment:

**5.2.1 Business Owner**
The individual or body with accountability for the business outcomes the AI system is deployed to achieve. The business owner approves the Focus definition, owns the outcome metrics, and is accountable for governance compliance in their domain.

**5.2.2 Technology Accountable Owner**
The individual with accountability for the AI system's technical operation, performance, and security. This role is distinct from the development or vendor team responsible for building or maintaining the system.

**5.2.3 Operational Oversight Role**
The individual or team responsible for day-to-day monitoring of the AI system's operation, including performance monitoring, escalation handling, and incident response. In smaller deployments this may be the same person as the Technology Accountable Owner; in larger deployments it is typically a distinct operational function.

**5.2.4 Escalation Path**
A documented escalation path that defines: what conditions trigger escalation from the AI system to a human, who receives the escalation, what response time is required, and what authority the receiving human has to act.

**5.2.5 Review and Approval Authority**
For AI systems that produce outputs that feed into consequential decisions, documentation of who reviews AI outputs before they are acted upon, and under what conditions AI outputs may be acted upon without additional human review.

**5.2.6 Governance Accountable Owner**
The individual accountable for ensuring that the FRAME governance framework is maintained for this deployment. In most organisations this will be a senior technology or risk leader. This role cannot be delegated to the development or vendor team.

### 5.3 Common Failures

- Role assignments that identify teams rather than named individuals, producing diffuse accountability
- Escalation paths that exist on paper but have not been tested or communicated to the relevant human recipients
- Governance accountable ownership assigned to the technology team responsible for building the system, creating a conflict of interest

---

## 6. Dimension Three: Authority

### 6.1 Definition

Authority defines the decision rights of the AI system: what it can act on autonomously, what requires human confirmation before action is taken, and what is outside its permitted scope entirely.

Authority boundaries are the primary mechanism for managing risk in agentic deployments. They must be explicit, documented, and enforced technically where possible.

### 6.2 Authority Tiers

FRAME defines three authority tiers for AI system actions:

**Tier 1: Autonomous Action**
Actions the AI system may take without human confirmation. Tier 1 actions are low-consequence, reversible, or both. They are explicitly listed in the Authority documentation; actions not on the Tier 1 list are not autonomous by default.

**Tier 2: Confirmed Action**
Actions the AI system may propose but not execute without explicit human confirmation. Tier 2 actions have material consequences, are difficult to reverse, or involve external parties. The system presents the proposed action and waits for approval before proceeding.

**Tier 3: Prohibited Action**
Actions the AI system is not permitted to take under any circumstances, regardless of instruction. Tier 3 prohibitions should be enforced technically where possible, not merely stated in policy.

### 6.3 Governance Requirements

An AI deployment satisfies the Authority dimension when the following are documented and approved before deployment:

**6.3.1 Tier Classification**
A complete classification of all action types available to the AI system across the three authority tiers. The classification must be exhaustive for Tier 1 and Tier 3; Tier 2 serves as the default for any action not explicitly classified.

**6.3.2 Technical Enforcement**
Documentation of how Tier 1 and Tier 3 boundaries are enforced technically. Policy statements alone do not satisfy this requirement for Tier 3 actions; technical controls must be implemented and tested.

**6.3.3 Boundary Change Control**
A defined process for modifying authority tier classifications. Authority boundaries may not be changed without review and approval by the Governance Accountable Owner. Emergency modifications must be documented within 24 hours.

**6.3.4 Boundary Violation Protocol**
A documented protocol for responding to authority boundary violations, including: immediate containment, impact assessment, root cause analysis, and governance review.

### 6.4 Authority and Agentic Systems

For AI systems operating as agents in multi-step workflows, authority boundaries must address not only individual actions but also action sequences. An agent that is individually permitted to read data, send messages, and create records may not be permitted to execute a workflow that combines all three without human review at defined checkpoints.

Authority documentation for agentic systems must explicitly address workflow-level authority in addition to action-level authority.

### 6.5 Common Failures

- Authority tiers defined at too high a level of abstraction to be technically enforceable
- Tier 3 prohibitions expressed only as policy statements, with no technical enforcement
- Authority boundaries designed for the intended use case but not tested against adversarial inputs or edge cases

---

## 7. Dimension Four: Metrics

### 7.1 Definition

Metrics specifies how the AI system's performance and contribution will be measured. FRAME distinguishes between activity metrics, outcome metrics, and governance metrics. All three are required; none is sufficient alone.

### 7.2 Metric Categories

**Activity Metrics**
Measures of what the AI system does: queries processed, tasks completed, documents generated, decisions made. Activity metrics are operationally useful for monitoring system health and utilisation. They are not governance-grade measures of value.

**Outcome Metrics**
Measures of what changes as a result of the AI system's operation: customer satisfaction, resolution time, error rate in downstream processes, staff capacity freed for higher-value work. Outcome metrics are the primary governance measure and must be traceable to the outcome statement defined in the Focus dimension.

**Governance Metrics**
Measures of the AI system's governance compliance: boundary violation rate, escalation accuracy, human override rate, audit trail completeness. Governance metrics are distinct from performance metrics and must be reported separately.

### 7.3 Governance Requirements

An AI deployment satisfies the Metrics dimension when the following are documented and approved before deployment:

**7.3.1 Outcome Metric Set**
A defined set of outcome metrics, each traceable to the outcome statement in the Focus definition. Each metric must specify: what is being measured, how it is measured, the data source, the measurement frequency, and the baseline against which change will be assessed.

**7.3.2 Baseline Assessment**
A pre-deployment baseline measurement for each outcome metric. Without a baseline, outcome metrics cannot demonstrate change. Baseline assessment must be completed before the AI system enters production.

**7.3.3 Leading and Lagging Indicators**
Explicit designation of which metrics are leading indicators (measurable early, signal conditions for value creation) and which are lagging indicators (accumulate over time, represent actual outcome change). Governance reviews must interpret metrics in light of this designation.

**7.3.4 Adoption Metric**
A defined measure of adoption: the proportion of the intended user population actively using the AI system in the intended way. Adoption is a financial variable, not a soft factor. It belongs in the ROI model and in every governance review.

**7.3.5 Reporting Cadence**
A defined reporting cadence for each metric category. Activity metrics may be reported continuously or weekly. Outcome metrics require sufficient accumulation time before meaningful assessment is possible. Governance metrics should be reported at every formal review cycle.

### 7.4 Common Failures

- Outcome metrics selected after deployment to justify activity metrics that were already being tracked
- No baseline measurement, making it impossible to demonstrate change
- Adoption excluded from the metric set, producing ROI models that assume full deployment when partial adoption is the reality

---

## 8. Dimension Five: Evaluation

### 8.1 Definition

Evaluation establishes the cadence, method, and accountability for ongoing review of the AI system's performance, governance compliance, and alignment with organisational objectives.

Evaluation is not a one-time post-deployment check. It is a continuous governance function.

### 8.2 Evaluation Cadence

FRAME defines three evaluation horizons:

**Operational Monitoring (Continuous)**
Automated and human monitoring of activity metrics, boundary adherence, and system health. Operational monitoring does not constitute a formal governance review but provides the data that informs it.

**Cycle Review (Quarterly)**
A structured review of all five FRAME dimensions, conducted by the Governance Accountable Owner with input from the Business Owner and Technology Accountable Owner. The cycle review produces a documented assessment and any required governance actions.

**Strategic Review (Annual)**
A full reassessment of the AI deployment's alignment with organisational strategy, including consideration of whether the Focus definition remains appropriate, whether authority boundaries remain calibrated to current risk appetite, and whether the deployment continues to justify its cost and governance overhead.

### 8.3 Governance Requirements

An AI deployment satisfies the Evaluation dimension when the following are documented before deployment and maintained throughout the operational lifecycle:

**8.3.1 Review Schedule**
A documented schedule for cycle reviews and strategic reviews, with named responsible parties for each review.

**8.3.2 Review Methodology**
A defined methodology for conducting cycle reviews, including: which dimensions are assessed, what evidence is required, how findings are documented, and what escalation path applies if significant concerns are identified.

**8.3.3 Adoption Review**
Adoption must be a standing agenda item at every cycle review. Adoption trends must be assessed alongside outcome metrics. A deployment with declining adoption is a governance concern regardless of system performance metrics.

**8.3.4 Governance Action Register**
A maintained register of governance actions arising from each review, with owners, due dates, and completion status. The action register is reviewed at the opening of each subsequent cycle review.

**8.3.5 Decommissioning Criteria**
Explicit criteria that would trigger consideration of decommissioning the AI system, including: sustained underperformance against outcome metrics, persistent boundary violations, irreversible adoption decline, or material change in the regulatory or risk environment.

### 8.4 Common Failures

- Evaluation treated as a one-time post-deployment review rather than a continuous governance function
- Cycle reviews conducted without reference to the baseline metrics established before deployment
- Governance action registers that exist but are not reviewed at subsequent cycles, producing outstanding actions that accumulate without resolution

---

## 9. Framework Application

### 9.1 Pre-Deployment Checklist

Before any AI system enters production, the following must be complete:

- [ ] Focus: Domain statement, problem definition, outcome statement, scope boundaries, and stakeholder alignment documented and approved
- [ ] Roles: All six role assignments documented with named individuals
- [ ] Authority: Tier classification complete, technical enforcement documented and tested, boundary change control process defined
- [ ] Metrics: Outcome metric set defined, baseline assessment complete, adoption metric defined, reporting cadence established
- [ ] Evaluation: Review schedule documented, review methodology defined, governance action register created

Partial completion is not acceptable. An AI system with incomplete FRAME documentation should not enter production.

### 9.2 Governance Documentation Package

Each FRAME deployment should maintain a governance documentation package containing:

- The completed FRAME pre-deployment checklist
- The Focus, Roles, Authority, Metrics, and Evaluation documentation for this deployment
- The governance action register
- Records of all completed cycle reviews and strategic reviews
- Any boundary violation records and their resolution

### 9.3 Multi-Deployment Environments

Organisations with multiple AI deployments should maintain a deployment register that provides a consolidated view of FRAME compliance status across all deployments. The deployment register does not replace per-deployment governance documentation; it supplements it.

---

## 10. Relationship to Other Frameworks

### 10.1 AAEF

The [AI Agent Evaluation Framework (AAEF)](https://github.com/ianloe/AAEF) provides agent-level evaluation methodology that operates within the governance envelope established by FRAME. FRAME's Evaluation dimension sets the governance context; AAEF provides the structured approach to evaluating individual agents within it.

### 10.2 Regulatory Frameworks

FRAME is designed to be compatible with and complementary to regulatory frameworks including the EU AI Act, the NIST AI Risk Management Framework, and the NSW Work Health and Safety Amendment (Digital Work Systems) Act 2026. It does not replace compliance obligations under any of these frameworks but provides the governance infrastructure within which compliance can be demonstrated.

---

## 11. Version History

| Version | Date | Notes |
|---|---|---|
| 1.0 | 2025 | Initial publication |

---

*FRAME is a proprietary framework developed by Ian Loe, Tactics Solutions. Licensed under CC BY-NC 4.0. For commercial use enquiries: Tactics Solutions.*
