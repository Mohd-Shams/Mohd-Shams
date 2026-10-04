# Hi, I'm Shams 👋

### Data Analyst | SQL | Python | Power BI | Excel | Statistics

I build data analytics projects that solve real-world business
problems using SQL, Python, Power BI, and statistical analysis.

---

# ANALYTICS PROJECTS

---

# 1. NovCart — E-commerce Performance & Leakage Analytics

> An end-to-end e-commerce analytics project analyzing profitability decline,
> operational issues, revenue leakage, and recovery opportunities using
> Python, SQL, Power BI, and AI.

## Business Problem

NovCart experienced a significant Q4 profitability decline, with profit falling much faster than revenue compared with Q3.
Management needed to identify where the profit leakage was occurring across discounts, costs, returns, delivery, products and regions.
The goal was to convert these findings into actionable recovery opportunities and provide an AI-powered system for answering business questions.

## Key Findings
| Key Finding                                                                                     | Business Impact                                                   | Recommendation                                                                                                    |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **Profit declined 44.44% in Q4** while revenue declined 28.03%                                  | Profit deteriorated significantly faster than sales               | Prioritize **margin and cost-driver analysis** alongside revenue recovery                                         |
| **Profit margin fell from 24.38% to 18.82%**                                                    | Lower profitability per ₹ of revenue                              | Review **discounting, product costs and shipping costs** and optimize high-impact drivers                         |
| **Delayed orders had 26.61% returns vs 10.48% without delays**                                  | Delivery performance is strongly associated with customer returns | Investigate delayed orders by **region, product and delivery partner** and reduce recurring delays                |
| **Quality issues were 32.33% of returns; Wireless Earbuds had 14.41% return rate**              | Returns create potential revenue and margin leakage               | Investigate **product quality, supplier/product batches and customer complaints** for high-return products        |
| **Discounting, returns, delivery, shipping and marketing efficiency emerged as recovery areas** | Multiple drivers may be contributing to value leakage             | Build **driver-level recovery scenarios**, validate assumptions, and prioritize initiatives using measured impact |

## Dashboard
#### Root Cause & Operations

Diagnosed the operational drivers behind the leakage: delivery delays nearly double return rates (26.6% vs 10.5%), and return volume is concentrated in two underperforming SKUs (Wireless Earbuds, Gaming Laptop) with "Quality Issue" as the top return reason. Confirmed the decline was structural, not regional, by showing a consistent ~40–50% profit drop across all four regions.

![Root Cause & Operations](https://github.com/Mohd-Shams/NovCart-E-commerce-Performance-Leakage-Analytics/blob/main/Power_Bi_Dashboard/RootCause_%26_Operations.png?raw=true)

#### Q4 Leakage Analysis

Quantified a ₹4.19M (44%) profit decline in Q4 using a profit-bridge waterfall, isolating discounting as the dominant leakage driver (₹2.4M of ₹3.5M total modeled recovery opportunity) — far outweighing marketing inefficiency, returns, and delivery combined. Built a return-count breakdown by reason and linked delivery delay directly to margin compression (24.4% → 18.8%).

![Q4 Leakage Analysis](https://github.com/Mohd-Shams/NovCart-E-commerce-Performance-Leakage-Analytics/blob/main/Power_Bi_Dashboard/Q4Leakage_Analysis.png?raw=true)

## AI Analyst
**[Launch NovCart AI Analyst](https://novcart-ai.streamlit.app/)**

1. Semantic Layer for standardized KPI definitions — Revenue, Profit, Margin, Returns, ROAS, etc.

2. Evidence Layer connecting validated Python/SQL findings to business questions.

3. LLM-powered reasoning to translate analytical evidence into concise business insights.

4. Natural Language Querying for exploring Q3–Q4 performance, root causes and recovery opportunities.

5. Streamlit AI interface combining LLM + Semantic Layer + Evidence Pack for grounded business decision support.

## GitHub Repository
**[📂 View Repository](https://github.com/Mohd-Shams/Agentic-Revenue-Intelligence-)**

---

# 2. A/B Testing — Mobile Game Retention (Cookie Cats)

> An end-to-end A/B test analysis of ~90,000 mobile game players, using hypothesis
> testing, confidence intervals, and bootstrap resampling in Python.

## Business Problem

A mobile game company wanted to know whether moving the first progression gate from Level 30 to Level 40 would improve Day-1 and Day-7 player retention, and whether any effect was large enough to matter at scale.
The goal was to turn the statistical result into a clear ship / don't-ship recommendation for the product team.

## Key Findings
| Key Finding | Business Impact | Recommendation |
| --- | --- | --- |
| **Day-7 retention fell from 19.02% to 18.20%** (−0.82 pp, p = 0.0016, 95% CI −1.33 to −0.31 pp) | **≈ 8,183 fewer Day-7 retained players per 1M users** | **Do not adopt the Level 40 gate yet** |
| **Day-1 retention fell from 44.82% to 44.23%** (−0.59 pp, p = 0.074), CI crosses zero | Inconclusive: the test could reliably detect only ~0.9 pp changes at Day-1 | Treat as **no evidence of improvement**, not proof of no effect; confirm in a follow-up experiment |
| **10,000-iteration bootstrap matched the z-test intervals** (D7: −1.33 to −0.32 pp) | The Day-7 drop does not depend on normality assumptions | Use the result with confidence for the Day-7 decision |
| **Bonferroni correction for two metrics** (α = 0.025) | Day-7 stays significant, Day-1 stays not significant | Conclusion is robust to testing two metrics |
| **One extreme outlier (49,854 rounds) removed; group split 44,699 vs 45,489** (SRM p ≈ 0.0085) | Data quality and randomisation checked before testing | Monitor group balance in any follow-up experiment |

## Results by Metric
| Metric | Gate 30 (Control) | Gate 40 (Treatment) | Difference | p-value | 95% CI | Result |
| --- | ---: | ---: | ---: | ---: | --- | --- |
| **Day-1 Retention** | 44.82% | 44.23% | −0.59 pp | 0.0739 | −1.24 to +0.06 pp | Not significant |
| **Day-7 Retention** | 19.02% | 18.20% | −0.82 pp | 0.00159 | −1.33 to −0.31 pp | Significant |

## Dashboard

![A/B Testing Report](https://github.com/Mohd-Shams/A-B-Testing/blob/main/A_B_test_report.png?raw=true)

## Product Decision

**Do not adopt Gate 40 yet.** Day-1 retention was inconclusive and Day-7 retention was significantly lower. Validate D14/D30 retention, revenue/LTV and engagement in a follow-up experiment before any rollout.

**Tools:** Python • Pandas • NumPy • SciPy • Statsmodels • Matplotlib

## GitHub Repository
**[📂 View Repository](https://github.com/Mohd-Shams/A-B-Testing)**
