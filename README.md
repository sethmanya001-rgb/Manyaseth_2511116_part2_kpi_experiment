# Manyaseth_2511116_part2_kpi_experiment
A/B Test KPI Experiment Analysis
# Part 2: KPI Experiment Analysis
## Campaign A/B Test — Business Analyst Report

---

## Business Context

A subscription-based digital product company launched a new
onboarding and activation campaign. Users were split into two groups:

- **Control group:** Existing onboarding experience  
- **Treatment group:** New campaign experience

Leadership wants to know whether the new campaign should be
rolled out to all users.

---

## Task 1: Business Problem Statement

### What decision needs to be made?
Should the company launch the new onboarding and activation
campaign to all users, or continue with the existing experience?

### Who does this decision impact?
Every new user who signs up for the product going forward.
If the wrong decision is made:
- Launching a bad campaign = higher refunds, more support issues
- Not launching a good campaign = missed revenue opportunity

### What metric should improve?
The primary metric we expect to improve is the
Paid Conversion Rate — the percentage of users who move
from free or trial to a paid subscription.
This directly connects to company revenue and growth.

### What risks must be monitored?
Even if conversion improves, we must make sure:
- Refund rate does not increase
- Support ticket rate does not spike
- Engagement score remains healthy
- Days to convert does not increase significantly
- No specific user segment is being harmed

### What evidence is required before making a recommendation?
1. Statistically significant improvement in paid conversion rate
2. No negative movement in guardrail metrics
3. Consistent results across segments like region, device,
   traffic source, and plan type
4. Sufficient sample size in both groups

---

## Dataset Description

File: data/campaign_experiment_data.xlsx

The dataset contains user-level experiment data including:
- User ID and group assignment (Control or Treatment)
- Funnel metrics: landing page visit, trial start,
  onboarding completion, paid conversion
- Revenue data
- Engagement score
- Days to convert
- Refund and support ticket flags
- Segment data: region, device type, traffic source, plan type

---

## North Star Metric

Paid Conversion Rate

This is the single most important metric because this is a
subscription business. Revenue only comes when a user pays.
All other metrics like visits, trials, and engagement scores
are only meaningful if they lead to a paid conversion.

Why not other metrics:
- Landing page visit rate = vanity metric, does not mean revenue
- Trial start rate = good leading indicator but not the end goal
- Engagement score = supports retention but alone does not equal revenue

Risk of optimizing blindly:
If we only chase conversion rate, we might attract low quality
users who convert but immediately refund, causing churn later.

---

## KPI Tree Summary

The North Star metric breaks down into three primary drivers:

Primary Driver 1 — Activation Funnel
- Landing page visit rate
- Trial start rate
- Onboarding completion rate

Primary Driver 2 — User Engagement
- Engagement score average
- Days to convert

Primary Driver 3 — Revenue Quality
- Average revenue per user
- Average revenue per converted user

Guardrail Metrics (must not worsen):
- Refund rate
- Support ticket rate
- Segment level decline

---

## Experiment Analysis Approach

- Compared Control vs Treatment across all key metrics
- Performed segment level analysis by region, device type,
  traffic source, and plan type
- Used t-Test in Excel to test statistical significance
- Evaluated guardrail metrics separately

---

## Hypothesis Test Summary

- Null Hypothesis H0: Paid conversion rate in Treatment
  is less than or equal to Control group
- Alternate Hypothesis H1: Paid conversion rate in Treatment
  is greater than Control group
- Test type: One tailed t-Test
- Significance level: 0.05
- Decision rule: If p-value is less than 0.05, reject H0

---

## Guardrail Metrics Considered

1. Refund rate — should not increase in Treatment group
2. Support ticket rate — should not spike in Treatment group
3. Days to convert — should not increase significantly
4. Engagement score — should remain healthy and not drop

---

## Final Recommendation

To be completed after full data analysis.
See outputs/recommendation_memo.md for detailed memo.

---

## Assumptions and Limitations

- Users were randomly assigned to Control or Treatment groups
- No external campaigns ran during the experiment period
- Data represents a single time period only
- Segment sizes may not be equal across groups

---

## Screenshots Included

- screenshots/summary_metrics.png
  Shows Control vs Treatment comparison table

- screenshots/hypothesis_test_output.png
  Shows t-Test result output from Excel

- screenshots/kpi_tree_preview.png
  Shows the full KPI Tree diagram
