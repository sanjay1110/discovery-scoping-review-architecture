# AI Discovery & Scoping Strategy Review

**Context:** The company wants to deploy AI across Customer Support, Operations, Compliance and Internal Knowledge Management. Leadership expects productivity gains but has not set priorities.
**Approach:** Problem-first and evidence-led. The goal of discovery is not to "find places for AI." It is to identify the 2–3 highest-value, lowest-risk pilots, each with a baseline, an owner and an agreed scope, and to get them signed off within four weeks.

---

## 1. Stakeholder Analysis

| Group | Primary priorities | Key concerns | Influence / Interest | Engagement |
|---|---|---|---|---|
| **Executive leadership** (CEO, COO, CFO) | ROI, productivity, competitive position | Unclear value, uncontrolled spend | High / High | Sponsor; bi-weekly steering committee |
| **Customer Support** (head, leads, agents) | Handle time, CSAT, backlog | Wrong answers reaching customers, job displacement | Medium / High | Co-design workshops, pilot users |
| **Operations** | Throughput, error reduction, less manual work | Disruption to workflows, legacy integration | Medium / High | Process mapping, shadowing |
| **Compliance, Legal & Risk** | Regulatory adherence, auditability, privacy | Hallucination, data leakage, lack of explainability | High (veto) / Medium | Involved from Week 1; review gates |
| **Knowledge Mgmt / HR / L&D** | Findability, onboarding speed | Stale content, unclear content ownership | Medium / Medium | Content audit, search pilot |
| **IT, Data & Security** | Integration, data quality, security, cost to run | Shadow AI, technical debt | High / High | Data and systems audit, feasibility spikes |
| **End users** (all functions) | Less repetitive work, usable tools | Trust, change fatigue | Low / High | Interviews, feedback loops |

## 2. Discovery Plan (Weeks 1–4)

| Week | Focus | Key activities | Deliverable |
|---|---|---|---|
| **1. Align & frame** | Mandate and governance | Sponsor kickoff; stakeholder map and RACI; review org charts, process docs, KPIs and ticket data; submit data-access requests; form steering group with Compliance and IT | Discovery charter, interview plan |
| **2. Current state** | Evidence gathering | 20–30 interviews across all four roles and functions; 2–3 shadowing sessions per function; collect baselines (AHT, volumes, manual hours, review cycle times, search time); data and systems audit | Process maps, pain-point log, baseline sheet |
| **3. Assess options** | Use-case evaluation | Build long list (15–25 use cases); scoring workshop on value, feasibility, data readiness, risk and time-to-value; compliance screening; technical spikes on top candidates | Scored use-case matrix (see `analysis/`) |
| **4. Prioritize & scope** | Decision | MoSCoW prioritization; pilot definitions (in/out of scope, owners, metrics); roadmap, business case, risk register; executive readout | Signed-off scoping document |

## 3. Interview Strategy

Interviews are 45–60 minutes, semi-structured, with two interviewers (lead and note-taker). We ask about **current work before AI**, ask for numbers and examples rather than opinions, and sample across functions and seniority levels.

| Group | Core questions |
|---|---|
| **Executives** | 1) Which business outcomes must improve in the next 12 months, and how would you judge AI's contribution? 2) If you could fund only one function first, which and why? 3) What risks are unacceptable (customer, regulatory, reputational)? 4) What budget, timeline or result would make you stop? |
| **Managers** | 1) Which processes consume the most time or cause the most rework, and how is that measured today? 2) Where do backlogs, handoffs and escalations occur? 3) Which KPIs do you own, and what are the current baselines? 4) What would your team need in order to adopt a new tool? |
| **End users** | 1) Walk me through your last difficult case. Where did the time go? 2) Where do you look for information, and how often do you fail to find it? 3) Which tasks are repetitive and rule-based, and which need judgment? 4) What would make you distrust an AI suggestion? |
| **Technical teams** | 1) Where does the relevant data live, who owns it, and how clean and accessible is it? 2) What integration constraints exist (APIs, legacy systems, identity)? 3) Which security, privacy and data-residency policies apply to AI/LLM use? 4) What capacity exists to run and monitor AI in production? |

## 4. Requirement Prioritization (MoSCoW)

| Priority | Requirements |
|---|---|
| **Must Have** | Responsible-AI policy approved by Compliance (data classification, acceptable use, human-in-the-loop) · Role-based secure data access; sensitive data stays within approved boundaries · Audit logging and traceability of AI outputs · Documented baseline and business owner for every pilot · **Pilot A:** Support agent-assist (drafted replies and knowledge retrieval, human-approved) · **Pilot B:** Internal knowledge search over curated sources, with citations |
| **Should Have** | Integration with ticketing/CRM and the knowledge base · Ticket triage and routing · Ops document intake and extraction · Compliance document review assistant (drafts only, human sign-off) · Evaluation framework (accuracy and groundedness test sets) · Training and change-management program |
| **Could Have** | Customer-facing chatbot (only after agent-assist proves accurate) · Meeting and case summarization · AI usage analytics dashboard · Ops demand forecasting · Multilingual support |
| **Won't (this phase)** | Autonomous customer-impacting decisions · Automated compliance sign-off · Custom model training |

Sequencing follows weighted scoring of value, feasibility, data readiness, risk and time-to-value (`analysis/use-case-scoring.md`).

## 5. Success Metrics

The targets below are starting hypotheses. They are recalibrated against the baselines collected in Week 2.

| Area | Metric | Target |
|---|---|---|
| **Discovery** | Stakeholder groups interviewed; baselined use cases; sign-off date | ≥90% of groups; ≥3 use cases; end of Week 4 |
| **Support** | Average handle time; first-contact resolution; CSAT | −15–20%; +10%; no decline |
| **Operations** | Manual processing hours on the scoped process; error rate | −25%; −30% |
| **Compliance** | Review cycle time; AI-related incidents; outputs logged | −30%; 0; 100% |
| **Knowledge** | Time to find information; search success rate | −40%; ≥80% |
| **Adoption & quality** | Weekly active pilot users; suggestion acceptance rate; answer accuracy on eval set | ≥70%; ≥50%; ≥90% |
| **Financial** | Payback period of the pilot portfolio | <12 months |

## 6. Risk Assessment

| Risk | Source | Likelihood / Impact | Mitigation |
|---|---|---|---|
| Solving the wrong problem (technology-first thinking) | Poor discovery | High / High | Require evidence of pain, a baseline and an owner for every use case |
| Missing stakeholders, especially Compliance, leading to a late veto | Poor discovery | Medium / High | Compliance on the steering group from Week 1; formal review gates |
| Unknown data quality or access stalls pilots | Poor discovery | High / High | Data audit and access requests in Weeks 1–2; feasibility spikes |
| No baselines, so ROI cannot be proven | Poor discovery | Medium / High | Baseline sheet is an exit criterion |
| Scope creep across four functions | Poor scoping | High / High | Cap at 2–3 pilots; change control through the steering group |
| Underestimated integration and change effort | Poor scoping | Medium / Medium | Technical spikes; explicit change-management budget |
| Privacy or regulatory breach | Poor scoping | Low / Very high | Data classification, human-in-the-loop, logging, compliance sign-off |
| Low adoption driven by fear of replacement | Both | Medium / High | Co-design with users; position AI as augmentation; train pilot champions |
| Vague success criteria prevent a go/no-go decision | Poor scoping | Medium / High | Quantified metrics and targets agreed per pilot before build |

## 7. Exit Criteria

The engagement is complete only when **all** of the following are verifiably true:

1. **Coverage:** At least 20 interviews spanning all four roles and all four functions (≥90% of mapped stakeholder groups), with findings validated in a playback session.
2. **Baselines:** Current-state metrics documented, with data sources, for every shortlisted use case.
3. **Prioritization:** The long list is scored against agreed criteria, and the top 2–3 pilots are selected with documented rationale.
4. **Scope:** Each pilot has an in/out scope statement, a named business owner, quantified success metrics and confirmed data access.
5. **Compliance & security:** Review completed with no unresolved blocking issues.
6. **Risk:** A risk register exists with an owner and mitigation for every high-impact risk.
7. **Plan:** A roadmap, resource plan and budget estimate are produced.
8. **Approval:** The steering committee formally signs off the scoping document.
