## Inferential Stats

- In inferential stats we perform multiple statical tests based on the problem statement and based on that we make conclusion to reject the Null Hypothesis or fail to reject the null hypothesis.

- Hypothesis testing usually stated as: Null Hypothesis and Alternate Hypothesis.

### P-value

- A p-value is the probability of getting your observed result (or something more extreme) if the null hypothesis is actually true.

- It tells you how likely your data is ( What is the probabilty of getting the data as you observed ), if the null hypothesis is true.

- A p-value does NOT tell you whether the hypothesis is true, the effect is large, or the conclusion is correct.

-  It only measures how unusual the data is if the null hypothesis were true.
  
- p-values come from tests like the t-test and z-test.

[P-Value](images/p-value.png)

### Confidence Interval

- Confidence Interval is a range of values that is likely to contain the true population value (mean, proportion, difference, etc.).

- CI answers, given the data I collected, what are the possible values the true population parameter could be?

- 95% Confidence Interval does not mean there is a 95% chance the true mean is inside this interval

- It means If you repeated this experiment many times and built a CI each time, 95% of those intervals would contain the true population value.

- It is a guarantee about the reliability of the method, not the specific interval.

- **Use Cases of CI**

[Use Case 1](images/ci_usecase_1.png)

[Use Case 2](images/ci_usecase_2.png)

[Use Case 3](images/ci_usecase_3.png)

### Significance Level (α) 

- The threshold you choose for deciding when to reject the null hypothesis.

- The significance level tells you, how much risk you are willing to take of making a wrong rejection of the null hypothesis.

- **Example:**

- If you choose α = 0.05, you are saying:

- “I am okay with a 5% chance of being wrong when I reject the null hypothesis.”

- If you choose α = 0.01, you are saying:

- “I want to be very strict; only 1% chance of being wrong is acceptable.”

- **Significance level relationship with p-value**:

- If p-value ≤ α → Reject the null hypothesis

- f p-value > α → Do NOT reject the null hypothesis

## Z - test

- A z-test is a statistical test used to determine whether a sample mean significantly differs from a known population mean (or another sample mean) when the population variance is known or the sample size is large.

- **Why is it called a Z-test**

- Because the test statistic you compute is a Z-score, which tells you how many standard deviations your sample mean is from the population mean.

### Types of Z - test

#### One-Sample Z-test

[One-Sample Z-test](images/one_sample_z_test.png)

#### Two-Sample Z-test ( Difference of Means )

[Two-Sample Z-test](images/two_sample_z_test.png)

#### One-Proportion Z-test

- A One-Proportion Z-test is used when you want to test whether a sample proportion (p̂) is significantly different from a claimed or known population proportion (p₀).

- **When to use**:

    - You are working with one sample
    - The population proportion p₀ is known
    - Sample size is large enough ==> [ n * p0​ ≥ 5 ], and [ n * (1−p0​) ≥ 5 ]
    - Data is categorical (like Yes/No, Pass/Fail, Win/Loss)

[Formula](images/one_proportion_z_test.png)

- **Example**:

[Example 1](images/one_proportion_z_test_example_1.png)
[Example 2](images/one_proportion_z_test_example_2.png)

#### Two-Proportion Z-test

- A Two-Proportion Z-test is used to check whether the proportion of success is different between two independent groups

- It compares p₁ (proportion in group 1) with p₂ (proportion in group 2)

- We are checking whether: p1 ​= p2 ​or p1​ != p2​

[Two Proportion 1](images/two_proportion_z_test_1.png)
[Two Proportion 2](images/two_proportion_z_test_2.png)

- **Example**:

[Example 1](images/two_proportion_z_test_example_1.png)
[Example 2](images/two_proportion_z_test_example_2.png)
[Example 3](images/two_proportion_z_test_example_3.png)

## T - test

- A t-test is a method to check if two groups are really different, or if their difference happened just by luck.

[T-test](images/t-test.png)

### Types of t-test

#### One-sample t-test

- When you compare your sample to a known value.

[One Sample t-test](images/one_sample_t_test.png)

- **Types of One-sample t-test:**

[One Sample T-test Type](images/one_sample_t_test_type.png)

- **One-sample t-test formula**

- [Formula](images/one_sample_t_test_formula.png)

#### Independent (Two-sample) t-test

- When you compare two separate groups

[Independent sample test](images/independent_sample_test.png)

- **Types of Independent (Two-sample) t-test**

##### Standard Independent t-test ( Pooled variance t-test ) ( Student’s t-test )

- Used when:
  
  - Both groups are independent
  - Both have equal variances (σ₁² = σ₂²)

- Calculation formula:

[Pooled Variance Formula](images/pooled_variance_t_test.png)
    
##### Welch’s t-test ( Welch correction )

- Welch’s t-test is the default recommended test because it is more robust.

- Used when:

    - Groups are independent
    - Variances are not equal (σ₁² ≠ σ₂²)
    - Sample sizes may also be different

- Calculation formula:

[Welch Formula](images/welch_formula.png)

##### One-tailed vs Two-tailed versions

- These are not different mathematical tests, but different hypothesis directions for the above two tests.

- Types:

    - Right-tailed test → Testing if mean₁ > mean₂
    - Left-tailed test → Testing if mean₁ < mean₂
    - Two-tailed test → Testing if mean₁ ≠ mean₂

- The same formula is used here according to the type of test used.


#### Paired (Dependent) t-test

- When you compare scores of the same people at two different times.

[Paired t-test](images/paired_t_test.png)

- This test is only differentiable only based of One-tailed vs Two-tailed versions

[Summary](images/paired_t_test_summary.png)

- Formula:
    - [Formula](images/paired_t_test_formula.png)
    - Now find Critical value from t-table based on DOF and significance level ( alpha )
    - Now compare the Critical value with calculated t-value and make decision according to One-tailed vs Two-tailed versions


### Note

#### Which test is used in which problem

[Test Selection](images/test_according_to_problem.png)

#### How to accept or reject null hypothesis

[Accept/Reject Null Hypothesis](images/accept_reject_h0_1.png)

[Accept/Reject Null Hypothesis](images/accept_reject_h0_2.png)