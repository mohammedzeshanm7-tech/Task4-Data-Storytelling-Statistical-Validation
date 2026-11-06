# Task 4: Data Storytelling & Statistical Validation

**ApexPlanet Data Analytics Internship** · Mohammed Zeshan Mohiuddin
**Dataset:** classicmodels sales database (same data as Task 2 and Task 3)
**Tools:** Excel (hypothesis test working), PowerPoint

## Files in this repo

| File | What it is |
|---|---|
| `Task4_Final_Presentation.pptx` | Final presentation deck (9 slides, speaker notes included) |
| `Hypothesis_Testing_Summary.md` | One-page summary of the statistical test |
| `Hypothesis_Test_Calculation.xlsx` | The same test worked out step by step in Excel, with a formula in every cell |
| `Data_Story.md` | The written business narrative (objective, analysis, conclusions, call to action) |

## Headline findings

- **$9.37M** revenue from **320** orders (Jan 2003 – May 2005); 6 cancelled orders excluded.
- **Seasonality:** Q4 (Oct–Dec) brings **48%** of yearly revenue; November alone is **26%**.
- **Products:** Classic Cars and Vintage Cars are **59%** of revenue; margins are 35–42% across all lines.
- **Customers:** 85% of the 2003 cohort ordered again in 2004; the top 10 customers make 28% of sales.
- **Hypothesis test:** Q4 orders are about **14% larger** (+$3,869), p = 0.036, so we reject H0 at the 5% level. The effect is small.

## Hypothesis test in one line

Welch t-test: t(238) = 2.114, p = 0.036, 95% CI for the difference +$263 to +$7,475.
See `Hypothesis_Testing_Summary.md` for the full write-up, and `Hypothesis_Test_Calculation.xlsx` to follow the calculation step by step.

## Notes and limits

- Data ends in May 2005, so seasonal comparisons use the two full years (2003–2004) only.
- The 2004 cohort has had less time to reorder than the 2003 cohort, so the retention gap is partly age.
- The test result is close to the 0.05 line, so the evidence is moderate, not certain.
