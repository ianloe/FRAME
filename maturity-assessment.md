# FRAME: Maturity Assessment

**Version 1.0**
**Author: Ian Loe, Tactics Solutions**

---

## Introduction

This maturity assessment tool enables organisations to evaluate their AI governance maturity across each of the five FRAME dimensions. It can be applied at the individual deployment level or at the organisational level across a portfolio of AI deployments.

The assessment is designed for self-assessment by a governance team, facilitated review by an internal audit or risk function, or advisory review by an external party. It produces a maturity profile, a set of identified gaps, and a prioritised improvement roadmap.

---

## Maturity Levels

FRAME uses a four-level maturity scale:

| Level | Label | Description |
|---|---|---|
| 1 | **Initial** | Governance exists informally or ad hoc. No documented framework. Accountability is unclear. |
| 2 | **Developing** | Governance documentation exists but is incomplete, inconsistent, or not actively maintained. Some accountability is defined. |
| 3 | **Defined** | Governance documentation is complete, approved, and maintained. Accountability is clear. Review cadence is in place. |
| 4 | **Optimising** | Governance is embedded in operational practice. Reviews drive continuous improvement. The organisation learns from governance data and improves its framework over time. |

Maturity Level 3 is the target for any AI deployment in production. Level 4 is the target for an organisation managing a portfolio of AI deployments.

---

## Assessment Instructions

For each dimension, score each indicator on a 1 to 4 scale using the level descriptions above. Where an indicator does not apply to the deployment or organisation being assessed, mark it N/A and exclude it from the dimension score calculation.

Calculate the dimension score as the average of applicable indicator scores. Calculate the overall maturity score as the average of dimension scores.

---

## Dimension 1: Focus

### Indicators

| # | Indicator | Score (1-4) | Evidence / Notes |
|---|---|---|---|
| F1 | A domain statement exists that clearly bounds the AI system's operating scope | | |
| F2 | A problem definition exists that describes the current state being addressed | | |
| F3 | An outcome statement exists that defines success in terms of operational change | | |
| F4 | Scope boundaries are documented for populations, data, decisions, and channels | | |
| F5 | The Focus definition has been reviewed and approved by the business owner | | |
| F6 | The Focus definition has been reviewed by the compliance or risk function where applicable | | |
| F7 | The Focus definition is reviewed and updated as part of each cycle review | | |

**Dimension Score:** _____ / 4

### Maturity Indicators by Level

**Level 1:** No documented domain statement or outcome definition. The deployment's purpose is understood informally by the team that built it.

**Level 2:** A domain statement and outcome statement exist but were written by the technology team without business owner input. Scope boundaries are implied rather than documented.

**Level 3:** All Focus components are documented, approved by the business owner, and included in the governance documentation package. The Focus definition is reviewed at each cycle review.

**Level 4:** The Focus definition is actively used to evaluate whether the deployment remains fit for purpose. Changes in business strategy or operational context trigger proactive Focus reviews outside the regular cycle.

---

## Dimension 2: Roles

### Indicators

| # | Indicator | Score (1-4) | Evidence / Notes |
|---|---|---|---|
| R1 | A named business owner is documented with clear accountability for outcomes | | |
| R2 | A named technology accountable owner is documented | | |
| R3 | An operational oversight role is defined with day-to-day monitoring responsibilities | | |
| R4 | An escalation path is documented with trigger conditions, recipient, channel, and response time | | |
| R5 | The escalation path has been tested and confirmed to work | | |
| R6 | A review and approval authority is defined for AI outputs feeding into consequential decisions | | |
| R7 | A governance accountable owner is named, outside the development or vendor chain | | |
| R8 | Role documentation is kept current as personnel changes occur | | |

**Dimension Score:** _____ / 4

### Maturity Indicators by Level

**Level 1:** No formal role documentation. Accountability is informally understood within the team.

**Level 2:** Some roles are documented but with team-level rather than individual assignments. The escalation path exists on paper but has not been tested.

**Level 3:** All roles are documented with named individuals. The escalation path has been tested. Role documentation is updated within two weeks of any personnel change.

**Level 4:** Role effectiveness is assessed at each cycle review. Escalation path performance is tracked and used to improve the path over time. Succession planning exists for governance-critical roles.

---

## Dimension 3: Authority

### Indicators

| # | Indicator | Score (1-4) | Evidence / Notes |
|---|---|---|---|
| A1 | All action types are classified across Tier 1, Tier 2, and Tier 3 | | |
| A2 | The Tier 1 list is specific (individual action types, not broad categories) | | |
| A3 | The Tier 3 list exists and contains meaningful prohibitions | | |
| A4 | Tier 3 prohibitions are technically enforced, not just stated in policy | | |
| A5 | A boundary change control process is documented and followed | | |
| A6 | A boundary violation protocol exists with defined response steps | | |
| A7 | Authority boundaries have been tested against adversarial inputs | | |
| A8 | For agentic systems: workflow-level authority is defined in addition to action-level authority | | |

**Dimension Score:** _____ / 4

### Maturity Indicators by Level

**Level 1:** No formal authority tier classification. The system operates without documented boundaries.

**Level 2:** A tier classification exists but uses broad action categories. Tier 3 prohibitions are policy statements only, with no technical enforcement.

**Level 3:** Tier classification is specific and complete. Tier 3 is technically enforced. A boundary change control process is followed. Violations are responded to under a documented protocol.

**Level 4:** Authority boundaries are regularly reviewed against emerging risk scenarios. Adversarial testing is conducted at each major system update. Boundary violation data is used to improve the tier classification over time.

---

## Dimension 4: Metrics

### Indicators

| # | Indicator | Score (1-4) | Evidence / Notes |
|---|---|---|---|
| M1 | Outcome metrics are defined and traceable to the Focus outcome statement | | |
| M2 | A pre-deployment baseline has been established for each outcome metric | | |
| M3 | Leading and lagging indicators are explicitly designated | | |
| M4 | An adoption metric is defined and tracked | | |
| M5 | A reporting cadence is defined for each metric category | | |
| M6 | Metrics are reviewed against baseline at each cycle review | | |
| M7 | The metric set has not been changed post-deployment to flatter performance | | |
| M8 | Activity metrics are distinguished from outcome metrics in all reporting | | |

**Dimension Score:** _____ / 4

### Maturity Indicators by Level

**Level 1:** Metrics are activity-based and were selected after deployment. No baseline exists.

**Level 2:** Some outcome metrics exist but were defined after deployment. A partial baseline exists. Adoption is not tracked.

**Level 3:** Outcome metrics are defined pre-deployment, traceable to the Focus outcome statement, and measured against a pre-deployment baseline. Adoption is tracked. Leading and lagging indicators are designated.

**Level 4:** The metric set is reviewed at each cycle review for continued relevance. Metric data drives governance decisions, not just reporting. The organisation has built institutional knowledge about which metrics are most predictive of deployment success.

---

## Dimension 5: Evaluation

### Indicators

| # | Indicator | Score (1-4) | Evidence / Notes |
|---|---|---|---|
| E1 | A review schedule is documented with named responsible parties | | |
| E2 | A review methodology is defined with consistent structure and evidence requirements | | |
| E3 | Cycle reviews are conducted on schedule | | |
| E4 | Adoption is a standing agenda item at every cycle review | | |
| E5 | A governance action register is maintained and reviewed at each cycle | | |
| E6 | Cycle review findings are documented in a consistent format | | |
| E7 | Decommissioning criteria are documented | | |
| E8 | Unscheduled reviews are triggered by defined events | | |
| E9 | Strategic reviews are conducted annually | | |

**Dimension Score:** _____ / 4

### Maturity Indicators by Level

**Level 1:** No formal review cadence. Governance is reactive, triggered by incidents.

**Level 2:** Reviews are scheduled but irregular. No consistent methodology. Action register exists but is not reviewed systematically.

**Level 3:** Reviews are conducted on schedule using a defined methodology. The action register is actively maintained. Adoption is reviewed at every cycle. Decommissioning criteria are documented.

**Level 4:** Review findings drive measurable improvements to governance practice. The organisation benchmarks its governance maturity across deployments and applies lessons learned systematically. Strategic reviews produce governance roadmaps, not just status assessments.

---

## Scoring Summary

| Dimension | Score | Level Label |
|---|---|---|
| Focus | | |
| Roles | | |
| Authority | | |
| Metrics | | |
| Evaluation | | |
| **Overall** | | |

---

## Interpreting Results

**Overall score below 2.0**
The deployment has significant governance gaps. It should not remain in production without an immediate remediation plan with short deadlines. Consider restricted operation (reduced authority scope) until Level 2 is achieved across all dimensions.

**Overall score 2.0 to 2.9**
The deployment has a developing governance foundation. A structured improvement plan is required to reach Level 3. Prioritise the lowest-scoring dimensions and any dimension with individual indicators scored at 1.

**Overall score 3.0 to 3.4**
The deployment meets the target governance standard. Focus improvement efforts on the gap between current and Level 4 for the dimensions most material to this deployment's risk profile.

**Overall score 3.5 and above**
The deployment demonstrates strong governance maturity. Maintain current practices and consider whether this deployment can serve as a reference case for other deployments in the portfolio.

---

## Priority Gap Analysis

After completing the assessment, identify the top three governance gaps by selecting the indicators with the lowest scores that have the highest governance consequence. Use the table below:

| Priority | Indicator | Current Score | Target Score | Required Action | Owner | Due Date |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |

---

## Assessment Record

| Field | Detail |
|---|---|
| Deployment name | |
| Assessment date | |
| Assessment conducted by | |
| Assessment type | Self-assessment / Facilitated / Advisory |
| Next assessment due | |

---

*FRAME is a proprietary framework developed by Ian Loe, Tactics Solutions. Licensed under CC BY-NC 4.0.*
