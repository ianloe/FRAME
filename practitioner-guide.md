# FRAME: Practitioner Guide

**Version 1.0**
**Author: Ian Loe, Tactics Solutions**

---

## Introduction

This guide is for practitioners applying FRAME to an AI deployment. It assumes familiarity with the FRAME Specification and translates its requirements into actionable steps for each dimension.

The guide is structured around the two phases of FRAME application: pre-deployment governance (getting a deployment ready for production) and operational governance (maintaining governance discipline once the system is live).

---

## Part One: Pre-Deployment Governance

Pre-deployment governance is the process of working through each FRAME dimension before an AI system enters production. The output is a completed governance documentation package that can be reviewed, approved, and maintained throughout the deployment lifecycle.

Allow two to four weeks for a thorough pre-deployment governance process on a new AI deployment. Rushing this phase to accelerate deployment creates governance debt that is significantly more expensive to address after an incident than before.

---

### Step 1: Convene the Right People

Before starting the FRAME process, confirm that you have access to the following:

- The **business owner**: the person accountable for the outcomes the AI system is meant to deliver. If you cannot identify this person, the deployment is not ready to proceed.
- The **technology accountable owner**: the person responsible for the system's technical operation.
- A **compliance or risk representative**: relevant if the deployment touches regulated data, regulated decisions, or a regulated industry.
- The **development or vendor team**: for technical input on authority boundary enforcement and monitoring capability.

FRAME is a governance process, not a technical process. The business owner must be actively involved, not consulted at the end.

---

### Step 2: Define Focus

Sit down with the business owner and work through the four Focus components in sequence. Do not move to Roles until Focus is complete and approved.

**Domain Statement**

Ask: *Where exactly does this AI system operate, and where does it not?*

Write a domain statement that is specific enough to exclude adjacent domains. If you cannot articulate what the system will not do, the domain statement is too broad.

Test: read the domain statement to someone unfamiliar with the deployment. If they cannot tell you what the system does and does not do, rewrite it.

**Problem Definition**

Ask: *What is broken, slow, or missing today that this system addresses?*

Avoid describing the AI solution in the problem definition. The problem should be describable without reference to AI.

Test: if the problem definition would still be valid if you replaced the AI system with a human worker, it is well framed.

**Outcome Statement**

Ask: *If this works, what is different six months from now?*

The outcome statement must describe a change in operational reality, not a change in system activity. "Customers receive faster responses" is an outcome. "The system processes queries faster" is activity.

Write the outcome statement before you select metrics. The outcome statement drives metric selection; metrics should not drive outcome definition.

**Scope Boundaries**

Ask: *What populations, data types, decisions, and channels are in scope? What is explicitly out?*

Document both. The out-of-scope list is as important as the in-scope list, particularly for systems that will interact with end users or process sensitive data.

---

### Step 3: Assign Roles

Work through the six role assignments. For each role, identify a named individual, not a team or function.

If you cannot name an individual for a role, that is a governance gap that must be resolved before deployment. Common blockers:

- **Business Owner unclear**: the deployment is serving multiple business units without a clear primary owner. Resolve by designating a lead owner with authority to make governance decisions, even if other units are stakeholders.
- **Technology Accountable Owner unclear**: the system is procured from a vendor with no internal technical owner. Designate an internal owner who is accountable for vendor performance and governance compliance. The vendor cannot hold this role.
- **Governance Accountable Owner defaulting to the technology team**: reassign to a senior leader outside the development or procurement chain.

Document the escalation path in enough detail to be actionable. Include: trigger conditions (what the AI system does that generates an escalation), recipient (who receives it), channel (how it arrives), expected response time, and the authority the recipient has to act.

Test the escalation path before deployment. Send a test escalation and confirm it arrives, is understood, and can be acted upon.

---

### Step 4: Define Authority Boundaries

This step requires input from the development or vendor team alongside the business owner and risk representative.

**Build the Tier Classification**

List every action type available to the AI system. Group them into Tier 1 (autonomous), Tier 2 (confirmed), and Tier 3 (prohibited). When in doubt about tier assignment, default to Tier 2.

Common mistakes to avoid:

- Classifying broad action categories (e.g. "respond to customer queries") rather than specific action types (e.g. "send a standard acknowledgement message", "issue a refund under $50", "update a customer record"). Governance requires specificity.
- Leaving Tier 3 empty because "we haven't thought of anything that should be prohibited". Tier 3 should always contain something. At minimum: actions that access financial systems, actions that communicate externally on behalf of the organisation without human review, and actions that permanently delete data.

**Confirm Technical Enforcement**

For every Tier 3 prohibition, ask: *is this technically enforced, or is it a policy statement?* Policy statements are necessary but not sufficient. Work with the technical team to implement controls that make Tier 3 violations impossible, not merely prohibited.

For Tier 1 automations, confirm that the system cannot be prompted or manipulated into treating Tier 2 or Tier 3 actions as Tier 1. Test this with adversarial inputs before deployment.

**Document the Change Process**

Define who can authorise a change to the tier classification and how quickly changes can be made. Avoid a process so slow that legitimate operational needs drive informal boundary workarounds.

---

### Step 5: Define Metrics

Return to the outcome statement from Step 2. For each outcome described, define at least one measurable metric.

**Select Outcome Metrics**

For each outcome metric, document:

- What is being measured
- How it is measured (data source, calculation method)
- Measurement frequency
- Who is responsible for producing the measurement
- Baseline value (measured before deployment)

If you cannot measure a baseline before deployment, you cannot demonstrate that the AI system created change. This is a hard requirement, not a nice-to-have.

**Designate Leading and Lagging Indicators**

Leading indicators are measurable early and signal whether the conditions for value creation are in place. They include: adoption rate, task completion rate, escalation accuracy, and system uptime. They do not prove value; they signal whether value is likely to accumulate.

Lagging indicators are the actual outcome measures. They require sufficient time to accumulate before meaningful assessment is possible. Designate a minimum assessment period for each lagging indicator. In most enterprise AI deployments, lagging indicators should not be formally assessed before 90 days.

**Define the Adoption Metric**

Define how adoption will be measured: what counts as an active user, what usage pattern constitutes genuine integration versus occasional or reluctant use, and what the target adoption rate is. The adoption metric must be included in every governance review.

---

### Step 6: Establish the Evaluation Structure

**Set the Review Schedule**

Book the first cycle review before deployment. If you cannot schedule the first review, operational pressure will prevent it from happening.

A practical cadence for most deployments:
- 30-day check-in: operational health, early adoption signal, any boundary concerns
- 90-day cycle review: first formal FRAME review across all dimensions
- Quarterly thereafter

**Define the Review Methodology**

Specify what each cycle review covers, what evidence is required, who must attend, and how findings are documented. A review without a defined methodology defaults to a status update meeting, which is not governance.

**Create the Action Register**

Set up the governance action register before deployment. The register should capture: the action, the owner, the due date, the status, and the review cycle in which it was raised. Actions not closed by the subsequent review require escalation.

---

## Part Two: Operational Governance

Once the AI system is in production, governance shifts from definition to maintenance. The primary governance activities are monitoring, cycle reviews, and action management.

---

### Continuous Monitoring

Operational monitoring is not a governance review. It is the data collection function that makes governance reviews possible. Ensure the following are in place from day one:

- Activity metric dashboards visible to the Operational Oversight role
- Automated alerting for boundary violations and escalation failures
- Audit trail logging that satisfies the evidence requirements for cycle reviews

Do not wait for a cycle review to identify a boundary violation. Violations require immediate response under the Boundary Violation Protocol, regardless of review schedule.

---

### Conducting a Cycle Review

A well-run cycle review follows a consistent structure:

1. **Open the action register**: review outstanding actions from the previous cycle. Close completed items, escalate overdue items, carry forward items with updated status.
2. **Review activity metrics**: confirm operational health. Flag anomalies for investigation.
3. **Review outcome metrics**: assess progress against baseline. For lagging indicators, confirm whether the assessment period has elapsed before drawing conclusions.
4. **Review adoption**: assess current adoption rate against target. If adoption is declining, this is a priority concern regardless of performance metrics.
5. **Review governance compliance**: boundary adherence rate, escalation accuracy, audit trail completeness.
6. **Assess each FRAME dimension**: has anything changed that requires a governance update? New use cases, changed risk appetite, regulatory developments, team changes?
7. **Record findings and actions**: document the review outcome and any new actions in the action register.

The cycle review should produce a one-page governance summary that can be presented to the Governance Accountable Owner and, where relevant, to a risk or audit function.

---

### Managing Governance Drift

Governance drift occurs when the documented governance framework diverges from actual practice. It is the most common governance failure mode in enterprise AI deployments and is rarely the result of deliberate non-compliance. It happens because operational teams adapt to practical realities without updating governance documentation.

Signs of governance drift:

- The tier classification no longer reflects what the system actually does
- Named role holders have changed without the governance documentation being updated
- Metrics are being reported that were not in the original metric set, while original metrics are no longer tracked
- Escalation paths have been informally modified

Prevent governance drift through disciplined cycle reviews that explicitly check each FRAME dimension against current operational reality, not just against the previous review's findings.

---

### When to Trigger an Unscheduled Review

The following events should trigger an unscheduled governance review, regardless of the regular cycle schedule:

- A Tier 3 boundary violation
- A significant incident involving an AI output that caused harm or nearly caused harm
- A material change in the regulatory environment affecting the deployment's domain
- A change in the business owner or governance accountable owner
- A significant change in the AI system's capabilities (model update, scope expansion, new integrations)
- Adoption declining below 50% of target for two consecutive months

---

## Appendix: Common Questions

**How long does a cycle review take?**

A well-prepared cycle review for a single AI deployment should take 60 to 90 minutes. Preparation (pulling metrics, reviewing the action register, preparing the governance summary) typically takes two to three hours. If reviews are consistently taking longer, the methodology is too complex or the governance documentation is not being maintained between reviews.

**What if the business owner is not engaged?**

This is a governance risk. Escalate to the Governance Accountable Owner. An AI deployment without an engaged business owner has no mechanism for outcome accountability. If engagement cannot be secured, consider whether the deployment should be in production.

**Can FRAME be applied retrospectively to a system already in production?**

Yes, but with additional care. Start with the Focus dimension and work forward. Treat any gaps as Tier 2 governance actions with short deadlines. Pay particular attention to the baseline problem: if no pre-deployment baseline was established, work with the business owner to define a proxy baseline from available historical data or accept that the deployment cannot demonstrate change relative to pre-AI state.

**How does FRAME apply to AI systems procured from vendors?**

FRAME applies to the deployment, not the system. The vendor is responsible for the AI system's technical performance within the contracted specification. The organisation deploying the system is responsible for its governance. Vendor SLAs satisfy some technical requirements but do not satisfy governance requirements. The Technology Accountable Owner and Governance Accountable Owner must be internal roles.

---

*FRAME is a proprietary framework developed by Ian Loe, Tactics Solutions. Licensed under CC BY-NC 4.0.*
