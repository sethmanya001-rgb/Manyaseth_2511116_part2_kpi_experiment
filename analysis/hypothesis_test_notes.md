
# Hypothesis Test Notes
## Campaign A/B Experiment — Statistical Analysis

---

## 1. Metric Being Tested

**Metric:** Paid Conversion Rate

**Definition:** 
Total users who converted to paid / Total users in group

**Why this metric:**
This is the North Star metric for this experiment.
It directly measures whether the new campaign is 
successfully converting users to paid subscribers.
A meaningful improvement here directly impacts revenue.

---

## 2. Hypothesis Statement

**Null Hypothesis (H0):**
The paid conversion rate of the Treatment group is 
equal to or less than the Control group.
The new campaign has no positive effect on conversion.

**Alternate Hypothesis (H1):**
The paid conversion rate of the Treatment group is 
significantly higher than the Control group.
The new campaign improves conversion rate.

---

## 3. Test Design

| Parameter | Value |
|---|---|
| Test Used | t-Test: Two-Sample Assuming Unequal Variances |
| Test Type | One-tailed |
| Significance Level (Alpha) | 0.05 |
| Control Observations | 692 |
| Treatment Observations | 714 |
| Hypothesized Mean Difference | 0 |

**Why one-tailed test:**
We only care if Treatment is BETTER than Control.
We are not testing if it is just different.
So one-tailed test is the correct choice here.

**Why t-Test Assuming Unequal Variances:**
Control variance = 0.0308
Treatment variance = 0.0652
Both variances are different so we use 
unequal variances version of t-Test.

---

## 4. Test Inputs

| Input | Control | Treatment |
|---|---|---|
| Mean Conversion Rate | 0.0317 (3.17%) | 0.0700 (7.00%) |
| Variance | 0.030825728 | 0.065215427 |
| Observations | 692 | 714 |

---

## 5. Test Output

| Output | Value |
|---|---|
| t Statistic | -3.280118223 |
| Degrees of Freedom | 1267 |
| P(T<=t) one-tail | **0.000532927** |
| t Critical one-tail | 1.646057171 |
| P(T<=t) two-tail | 0.001065853 |
| t Critical two-tail | 1.961838097 |

See screenshot: screenshots/hypothesis_test_output.png

---

## 6. Decision Rule
