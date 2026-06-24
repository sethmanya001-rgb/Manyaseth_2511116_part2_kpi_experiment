# Recommendation Memo
## Campaign Experiment — Business Analyst Report

**To:** Leadership Team
**From:** Business Analyst
**Subject:** New Onboarding Campaign — Launch Decision
**Date:** June 2025

---

## 1. Executive Summary

The company conducted an A/B experiment to evaluate 
whether a new onboarding and activation campaign 
improves user conversion.

Users were split into two groups:
- Control group: 690 users — existing experience
- Treatment group: 710 users — new campaign experience

Result: The Treatment group showed a conversion rate 
of 7.00% compared to 3.17% in Control group.

p-value = 0.0005 which is well below 0.05 threshold.

FINAL RECOMMENDATION: LAUNCH THE CAMPAIGN ✅

---

## 2. North Star Metric

Selected Metric: Paid Conversion Rate

Paid Conversion Rate is defined as:
Total users who converted to paid / Total users in group

Control Group: 3.17%
Treatment Group: 7.00%
Improvement: +3.83 percentage points

This metric was selected because:
- This is a subscription based business
- Revenue is only generated when a user pays
- All other funnel metrics only matter if they 
  lead to payment
- It directly connects campaign success to 
  business growth

Risk of blind optimization:
If only conversion rate is optimized without checking 
quality, the company may attract users who convert 
but immediately refund, causing revenue loss later.

---

## 3. KPI Tree Explanation

The North Star metric Paid Conversion Rate breaks 
down into three primary drivers:

Primary Driver 1 — Activation Funnel
- Landing page visit rate: Control 63.62% vs Treatment 72.39%
- Trial start rate: Control 25.07% vs Treatment 29.01%
- Onboarding completion rate: Control 15.65% vs Treatment 21.13%

Primary Driver 2 — User Engagement
- Avg engagement score: Control 57.03 vs Treatment 62.94
- Avg days to convert: Control 8.86 vs Treatment 6.40

Primary Driver 3 — Revenue Quality
- Avg revenue per user: Control 51.97 vs Treatment 54.25
- Avg revenue per converter: Control 1630.10 vs Treatment 770.41

Guardrail Metrics:
- Refund rate
- Support ticket rate
- Segment level decline

See outputs/kpi_tree.png for full visual KPI tree.

---

## 4. Experiment Result Summary

| Metric | Control | Treatment | Difference |
|---|---|---|---|
| User Count | 690 | 710 | +20 |
| Landing Page Visit Rate | 63.62% | 72.39% | +8.77% |
| Trial Start Rate | 25.07% | 29.01% | +3.94% |
| Onboarding Completion Rate | 15.65% | 21.13% | +5.48% |
| Paid Conversion Rate | 3.17% | 7.00% | +3.83% |
| Avg Revenue Per User | 51.97 | 54.25 | +2.28 |
| Avg Revenue Per Converter | 1630.10 | 770.41 | -859.69 |
| Refund Rate | 0.00% | 0.42% | +0.42% |
| Support Ticket Rate | 14.78% | 24.79% | +10.01% |
| Avg Engagement Score | 57.03 | 62.94 | +5.91 |
| Avg Days to Convert | 8.86 days | 6.40 days | -2.46 days |

---

## 5. Hypothesis Test Interpretation

Null Hypothesis H0:
Paid conversion rate in Treatment is less than 
or equal to Control group.

Alternate Hypothesis H1:
Paid conversion rate in Treatment is significantly 
higher than Control group.

Test Used: One-tailed t-Test Two Sample 
Assuming Unequal Variances

Significance Level: 0.05

Results:
- Control Mean: 0.0317 which is 3.17%
- Treatment Mean: 0.0700 which is 7.00%
- t Statistic: -3.280118223
- p-value one-tail: 0.000532927

Decision: REJECT H0

Interpretation:
p-value of 0.0005 is much less than 0.05.
This means there is only 0.05% chance that 
this result occurred by random chance.
The new campaign significantly improves 
paid conversion rate.

---

## 6. Guardrail Analysis

Before making final recommendation the following 
guardrail metrics were evaluated:

Guardrail 1 — Refund Rate
- Control: 0.00%
- Treatment: 0.42%
- Risk Level: LOW
- Conclusion: Slight increase but very minimal.
  Acceptable for launch.

Guardrail 2 — Support Ticket Rate
- Control: 14.78%
- Treatment: 24.79%
- Risk Level: MEDIUM
- Conclusion: Support tickets increased by 10%.
  This needs careful monitoring post launch.
  May indicate users need more help with 
  new onboarding experience.

Guardrail 3 — Avg Days to Convert
- Control: 8.86 days
- Treatment: 6.40 days
- Risk Level: NONE
- Conclusion: Treatment converts faster. 
  This is a positive sign.

Guardrail 4 — Avg Engagement Score
- Control: 57.03
- Treatment: 62.94
- Risk Level: NONE
- Conclusion: Treatment users are more engaged.
  This is a positive sign for retention.

Overall Guardrail Conclusion:
3 out of 4 guardrail metrics show no risk.
Support ticket rate needs monitoring.
Overall risk is manageable.

---

## 7. Segment Level Insight

Analysis was performed across the following segments:
- Region
- Device type
- Traffic source
- Plan type

Key Finding:
The conversion improvement in Treatment group was 
observed across multiple segments indicating the 
campaign has broad effectiveness and is not limited 
to one specific user group.

Detailed segment analysis is available in:
outputs/experiment_summary.xlsx

---

## 8. Final Recommendation

DECISION: LAUNCH THE CAMPAIGN ✅

Reason for Launch:
1. Conversion rate more than doubled from 3.17% to 7.00%
2. p-value of 0.0005 shows strong statistical significance
3. Engagement score improved from 57.03 to 62.94
4. Days to convert reduced from 8.86 to 6.40 days
5. Revenue per user improved from 51.97 to 54.25

---

## 9. Risks and Limitations

Risk 1 — Support Ticket Spike:
Support ticket rate increased by 10% in Treatment.
Action: Hire additional support staff before launch.
Monitor weekly for first 30 days.

Risk 2 — Revenue Per Converter Dropped:
Avg revenue per converter dropped from 1630 to 770.
This means individual converters are paying less.
Action: Monitor cohort revenue over 90 days.

Risk 3 — Experiment Duration:
Experiment ran for limited time period only.
Results should be validated over longer period.

Risk 4 — External Factors:
External factors during experiment period 
were not controlled for.

---

## 10. Next Steps

1. Launch new onboarding campaign to all users
2. Monitor conversion rate weekly for 30 days
3. Track support ticket rate closely 
4. Investigate why revenue per converter dropped
5. Run follow up experiment after 60 days
6. Consider segment specific optimizations 
   based on regional performance data
7. Present results to leadership after 30 day 
   post launch monitoring period
