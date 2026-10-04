# Hi, I'm Shams 👋

### Data Analyst | SQL | Python | Power BI | Excel | Statistics

I build data analytics projects that solve real-world business
problems using SQL, Python, Power BI, and statistical analysis.


ANALYTICS PROJECTS
=========================
# NovCart — E-commerce Performance & Leakage Analytics

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
![Root Cause & Operations](https://github.com/Mohd-Shams/NovCart-E-commerce-Performance-Leakage-Analytics/blob/main/Power_Bi_Dashboard/RootCause_%26_Operations.png)

#### Q4 Leakage Analysis

Quantified a ₹4.19M (44%) profit decline in Q4 using a profit-bridge waterfall, isolating discounting as the dominant leakage driver (₹2.4M of ₹3.5M total modeled recovery opportunity) — far outweighing marketing inefficiency, returns, and delivery combined. Built a return-count breakdown by reason and linked delivery delay directly to margin compression (24.4% → 18.8%).
![Q4 Leakage Analysis](https://github.com/Mohd-Shams/NovCart-E-commerce-Performance-Leakage-Analytics/blob/main/Power_Bi_Dashboard/Q4Leakage_Analysis.png)


## AI Analyst
**[Launch NovCart AI Analyst](https://novcart-ai.streamlit.app/)**

1. Semantic Layer for standardized KPI definitions — Revenue, Profit, Margin, Returns, ROAS, etc.

2. Evidence Layer connecting validated Python/SQL findings to business questions.

3. LLM-powered reasoning to translate analytical evidence into concise business insights.

4. Natural Language Querying for exploring Q3–Q4 performance, root causes and recovery opportunities.

5. Streamlit AI interface combining LLM + Semantic Layer + Evidence Pack for grounded business decision support.


## Github Repsitory
**[📂 View Repository](https://github.com/Mohd-Shams/Agentic-Revenue-Intelligence-)**
================

# 🎮 A/B Testing: Mobile Game Retention (Cookie Cats)

**Question:** Does moving the first progression gate from Level 30 to Level 40 improve player retention?

**Approach:** Checked data quality and group balance (including a sample ratio mismatch test), removed one extreme outlier, ran two-proportion z-tests with 95% confidence intervals, validated them with a 10,000-iteration bootstrap, and applied a Bonferroni correction for the two metrics.

### 📊 Key Findings

| Metric | Gate 30 (Control) | Gate 40 (Treatment) | Difference | p-value | 95% CI | Result |
| --- | ---: | ---: | ---: | ---: | --- | --- |
| **Day-1 Retention** | 44.82% | 44.23% | −0.59 pp | 0.0739 | −1.24 to +0.06 pp | Not significant |
| **Day-7 Retention** | 19.02% | 18.20% | −0.82 pp | 0.00159 | −1.33 to −0.31 pp | Significant |

### ✅ Validation & Impact

| Check | Result |
| --- | --- |
| Users analyzed | 90,188 (1 outlier removed) |
| Group sizes | 44,699 vs 45,489 (SRM p ≈ 0.0085, acceptable) |
| Bootstrap (10,000 runs) | D1 CI crosses zero; D7 CI stays below zero |
| Bonferroni (α = 0.025) | D7 still significant, D1 still not |
| Business impact | ≈ 8,183 fewer Day-7 retained players per 1M users |

### 🧠 Decision

**Do not adopt Gate 40 yet.** Day-1 retention was inconclusive and Day-7 retention was significantly lower. Validate D14/D30 retention, revenue/LTV and engagement in a follow-up experiment before any rollout.

**Tools:** Python • Pandas • NumPy • SciPy • Statsmodels • Matplotlib

🔗 [View project](https://github.com/Mohd-Shams/A-B-Testing)
