# Pitfalls of significance testing

## Insignificant significance

Suppose, for example, that there were 2500 women and 2500 men studying at MIT. Suppose further that the mean GPA of men was 3.5, the mean GPA of women was 3.51, and the standard deviation of the GPA for both men and wom- en was 0.25. Most sensible people would consider the difference in GPAs “insignificant.”

However, from a statistical point of view the difference is “significant” at close to the 2% level. What is the root of this strange dichotomy? , when a study has enough power—i.e, enough examples—even insignificant differences can be statistically significant.

A related problem arises when a study is very small. Suppose you flipped a coin twice and it came up heads both times. Now, let’s use the two-tailed one- sample t-test to test the null hypothesis that the coin is fair. If we assume that the value of heads is 1 and the value of tails is 0, we can get the p-value using the code

```python
stats.ttest_1samp([1, 1], 0.5)[1]
```

It returns a p-value of 0, indicating that if the coin is fair the probability of getting two consecutive heads is nil.

## One tail vs two tail test

We should be wary of using a **one-tailed test** when the direction of the effect isn't pre-specified or when deviations in **either direction** would be meaningful.

For example, in a study where Lyndsay wins **666 out of 1,273 games** of *Words with Friends* against John, John tests the null hypothesis that each player has a 50% chance of winning using a **two-tailed t-test**, which yields a **p-value of \~0.098**, indicating the result is **not statistically significant** at the 5% level. However, Lyndsay runs a **Monte Carlo simulation** assuming that only her winning more than 666 games would be surprising (a **one-tailed test**), and gets a **p-value of \~0.049**, which falsely appears significant.

This result is misleading because it ignores the possibility that **John could have won 666 games**, which would also be surprising under the null.

The correct null hypothesis here is what is the possibility that any player will win 666 games.

When the simulation is correctly adjusted to check for **either player** winning at least 666 games (a **two-tailed approach**), the p-value again rises to \~0.098 — matching the original t-test. This illustrates that using a one-tailed test **after seeing** that Lyndsay won more games biases the result and artificially inflates significance.

## Understanding the Texas Sharpshooter Fallacy

In a 2001 study from the Royal Cornhill Hospital in Aberdeen, researchers reported that **30% more anorexic women were born in June** than the monthly average. With 446 anorexic women studied, the average births per month is \~37. A 30% increase implies **48 women were born in June**.

They estimated the probability of this occurring **by chance** using a simulation, which gave:

```
    Probability of at least 48 births in June = 0.0427
```

This appears statistically significant (*p* < 0.05) **if** June was the pre-specified hypothesis.

However, **the researchers did not hypothesize about June in advance**. They looked at all months and highlighted June **after seeing the data**. This is an example of the **Texas Sharpshooter Fallacy** — finding patterns after the fact and treating them as meaningful.

We are bound to find some outliers even when our null hypothesis is true if we run many tests, seeing these and rejecting the null hypothesis is wrong.

The correct question to ask:

> What is the probability that **any month** would show at least 48 births?

A new simulation showed:

```
Probability of at least 48 births in some month = 0.4357
```

This shows the result is **not statistically unusual** when accounting for **multiple comparisons**.

### Comparing Hypotheses

| Hypothesis                                            | Interpretation                                                      |
| ----------------------------------------------------- | ------------------------------------------------------------------- |
| **H1: More anorexics are born in June**               | A specific, **pre-planned** test. *p* ≈ 0.043 might be significant. |
| **H2: Some month has unusually high anorexic births** | A **general, post-hoc** test. *p* ≈ 0.44 is **not** significant.    |

### Bonferroni Correction

If all 12 months were tested, a Bonferroni correction would adjust the significance level:

- Original α = 0.05
- Adjusted α = 0.05 / 12 ≈ 0.0042

Since *p* = 0.043 > 0.0042, the result would **not be significant** after correction.

## Reference

CHAPTER 21. LIES, DAMNED LIES, AND STATISTICS INTRODUCTION TO COMPUTATION AND PROGRAMMING USING PYTHON
