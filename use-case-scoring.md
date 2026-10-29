# Supporting Analysis: Use-Case Scoring Matrix

This analysis supports Sections 2 (Week 3) and 4 of `REVIEW.md`. The scores are **illustrative hypotheses**. During Week 3 they are re-scored with stakeholders using the evidence and baselines gathered in Week 2.

## Criteria and weights

| Criterion | Weight | 5 = | 1 = |
|---|---|---|---|
| Business value | 30% | Large, measurable impact on a priority KPI | Marginal impact |
| Technical feasibility | 20% | Proven pattern, few integrations | Novel approach, complex integrations |
| Data readiness | 20% | Clean, accessible, owned data | Scattered, poor-quality or restricted data |
| Risk (inverse) | 15% | Internal-only, human-reviewed, low regulatory exposure | Customer- or regulator-facing, autonomous |
| Time to value | 15% | Pilot in under 8 weeks | More than 6 months |

**Weighted score** = Σ (score × weight), on a scale of 1 to 5.

## Scored long list

| # | Use case | Function | Value | Feas. | Data | Risk | Time | **Score** | MoSCoW |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Agent-assist (drafted replies and retrieval) | Support | 5 | 4 | 4 | 4 | 4 | **4.30** | Must |
| 2 | Internal knowledge search with citations | Knowledge | 4 | 5 | 3 | 5 | 5 | **4.30** | Must |
| 3 | Ticket triage and routing | Support | 4 | 4 | 4 | 4 | 4 | **4.00** | Should |
| 4 | Meeting and case summarization | Cross-functional | 2 | 5 | 5 | 4 | 5 | **3.95** | Could |
| 5 | Document intake and extraction | Operations | 4 | 3 | 3 | 4 | 3 | **3.45** | Should |
| 6 | Regulatory change monitoring | Compliance | 3 | 4 | 4 | 3 | 3 | **3.40** | Should |
| 7 | Compliance document review assistant | Compliance | 5 | 3 | 3 | 2 | 2 | **3.30** | Should |
| 8 | Customer-facing chatbot | Support | 4 | 3 | 3 | 2 | 3 | **3.15** | Could |
| 9 | Demand / workload forecasting | Operations | 3 | 2 | 2 | 4 | 2 | **2.60** | Could |

## Reading the matrix

- **Pilots A and B** (rows 1–2) combine high value with manageable risk and reuse the same retrieval foundation. Building that foundation once lowers the cost of later use cases.
- **Summarization** scores highly on ease but has low strategic value. It stays a Could: a quick win, not a priority.
- **Compliance review** has high value but high risk. It is sequenced after governance, logging and the evaluation framework are proven in Pilots A and B.
- **The customer-facing chatbot** is deliberately deferred. Agent-assist validates answer quality with a human in the loop before anything reaches customers directly.
