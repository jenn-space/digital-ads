# digital-ads
The analysis found that while increased digital advertising spending positively influences customer conversions, returns diminish beyond a mid-range investment level, indicating the need for optimized, data-driven ad budget allocation to maximize ROI.

# Business Problem
The company seeks to understand how digital advertising spending drives customer conversions.
Executives want to determine if increased ad investment yields meaningful growth and whether the
returns justify the cost.
Key Findings
Analysis of recent marketing data shows a clear, positive relationship between ad spend and cus-
tomer conversions.
In the initial model, advertising spend explained r round(r2_model1*100,1)% of conversion varia-
tion.
After refining the model using a logarithmic transformation, the fit improved to r round(r2_model2*100,1)%,
indicating stronger consistency between ad investment and conversion outcomes.
The results confirm that higher ad spend typically leads to more conversions, though the impact
levels off at higher spending levels. The relationship is statistically reliable and aligns with expected
marketing behavior — diminishing returns beyond a certain threshold.
# Recommendation
Continue investing in digital advertising, but at an optimized level rather than pursuing unlimited
growth in ad budgets. Allocate resources strategically to the most responsive campaigns and
audiences. Consider further segmentation by platform, audience type, and creative performance to
enhance cost eﬀiciency and return on investment (ROI).
Supporting Evidence

Consistent positive trend: Conversions rise steadily with ad spend across campaigns.
Improved model accuracy: Log-transformed model explains more variation (r round((r2_model2 -
r2_model1)*100,1) percentage points higher R²).
Diminishing returns: Gains in conversions slow beyond mid-range ad spend levels.
Reliable prediction: 95% confidence intervals indicate a statistically sound relationship.
No evidence for CFO’s claim: The claim of “5 or more conversions per $1,000 increase” was not
supported at the 95% confidence level.
Limitations
This analysis is based on observational data, not controlled experiments, so causal conclusions
are limited. Other unmeasured factors (e.g., seasonality, creative quality, or channel type) may
influence results. Future work should include campaign-level metrics and audience segmentation
for deeper insight.


---

## Overview

This visualization explores the relationship between **advertising spend** and **conversions** using linear regression. The goal is to understand whether higher investment in ad campaigns corresponds with increased conversion rates.

---

## Code Summary

The plot was created in **R** using the `ggplot2` package.  
Below is the script:

```r
ggplot(df, aes(x = AdSpend, y = Conversions)) +
  geom_point(color = "#2E86C1", alpha = 0.7) +
  geom_smooth(method = "lm", color = "#B03A2E", se = TRUE) +
  labs(
    title = "Figure 1. Relationship Between Ad Spend and Conversions",
    x = "Ad Spend ($000s)",
    y = "Conversions"
  ) +
  theme_minimal(base_size = 11)
