# Hypothesis Testing Summary

## Business Hypothesis
**"The new email marketing campaign led to a statistically significant increase in conversion rate."**

- **H0 (null):** The new campaign has no effect on conversion rate.
- **H1 (alternative):** The new campaign increases conversion rate.

## Experiment Design
- Customers were split into two groups: **Treatment** (new campaign) and **Control** (old campaign)
- n = 1,989 (Treatment), n = 2,005 (Control)
- Outcome measured: whether the customer converted (purchased), and order value

## Test 1: Chi-Squared Test of Independence (Conversion Rate)

| Group | Conversion Rate | n |
|---|---|---|
| Control | 21.80% | 2,005 |
| Treatment | 26.14% | 1,989 |

- **Chi-squared statistic:** 10.13
- **Degrees of freedom:** 1
- **P-value:** 0.00146
- **95% Confidence Interval on the lift:** [1.70%, 6.99%]
- **Decision (α = 0.05):** Reject H0

## Test 2: Independent T-Test (Average Order Value)

| Group | Avg Order Value | n |
|---|---|---|
| Control | $678.59 | 2,005 |
| Treatment | $707.95 | 1,989 |

- **T-statistic:** 1.347
- **P-value:** 0.178
- **Decision (α = 0.05):** Fail to reject H0

## Business Conclusion

The new email campaign produced a **statistically significant increase in conversion rate** (26.1% vs 21.8%, p = 0.0015). Because the 95% confidence interval for the true lift (1.70pp to 6.99pp) does not cross zero, we can be confident this is a real effect rather than random variation.

However, average order value did **not** differ significantly between groups (p = 0.178). This means the campaign is effective at converting more customers into buyers, but it does not change how much they spend once they decide to purchase.

**Recommendation:** Roll out the new campaign to the full customer base to capture the conversion lift. Do not expect an uplift in order value from this change alone — a separate initiative (e.g. upsell/cross-sell prompts) would be needed to move that metric.

## Methodology Notes
- Test used: Chi-squared test of independence (categorical outcome: converted / not converted); Welch's t-test (continuous outcome: order value, unequal variances assumed)
- Significance level: α = 0.05
- Tools: Python (pandas, scipy.stats)
