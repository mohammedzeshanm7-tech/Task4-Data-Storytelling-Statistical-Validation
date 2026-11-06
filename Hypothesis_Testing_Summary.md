# Hypothesis Testing Summary

## Business hypothesis
Orders placed in the busy season (Q4: October–December) have a different average value from orders placed in the rest of the year (January–September).

## Hypotheses
- **H0:** Average order value in Q4 = average order value in Jan–Sep.
- **H1:** The two averages are different (two-sided test).
- **Significance level:** α = 0.05

## Data
320 non-cancelled orders from classicmodels. Order value = sum of (quantity × price) for the order.

| Group | Orders | Mean order value | Std. dev. |
|---|---|---|---|
| Q4 (Oct–Dec) | 114 | $31,757 | $15,547 |
| Jan–Sep | 206 | $27,888 | $15,918 |

## Calculation
The full step-by-step calculation, with formulas, is in `Hypothesis_Test_Calculation.xlsx` (sheet "Hypothesis Test").

## Test chosen
**Welch two-sample t-test** (independent groups, different sizes, no assumption of equal variance).

## Result

| Measure | Value |
|---|---|
| Difference in means | +$3,869 (+13.9%) |
| t-statistic | 2.114 (df ≈ 238) |
| p-value | **0.036** |
| 95% confidence interval | +$263 to +$7,475 |

## Interpretation
- p = 0.036 is below 0.05, so we **reject H0**. If Q4 and the rest of the year really had the same average order value, a gap this large would show up by chance only about 3.6% of the time.
- The 95% confidence interval does not include zero, which agrees with the p-value. But the interval is wide: the true gap could be as small as a few hundred dollars or as large as about $7,500.
- The p-value is only a little below 0.05, so the evidence is moderate, not very strong.

## Business conclusion
Q4 orders are probably somewhat larger than orders in the rest of the year, by roughly 14%, but the evidence is moderate. The bigger Q4 story is **volume**: Q4 brings 45% of orders and 48% of yearly revenue. Plan for the order surge first, and treat the larger order size as a bonus rather than a guarantee.

## Limits to keep in mind
- Observational data, not a controlled experiment, so we can show that Q4 orders are larger but not why.
- The main result is close to the 0.05 line, so it should not be called a certainty.
