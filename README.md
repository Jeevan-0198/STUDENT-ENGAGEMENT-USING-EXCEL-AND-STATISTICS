# STUDENT-ENGAGEMENT-USING-EXCEL-AND-STATISTICS
## PROJECT OBJECTIVE
 An Edu-Tech company wanted to increase student engagement on their platform, so they introduced various additional features. These included an XP system that enabled students to track their progress, level up, and earn rewards by completing various learning objectives. The platform also offered in-app coins that could be exchanged for special awards, a leaderboard where students could compete for top positions in different divisions—earning weekly rewards and advancing up the ladder—and streaks to motivate students to maintain consistent learning habits.Now, the company wants to determine whether student engagement increased separately for free and paid students between Q4 2021 and Q4 2022, during the period when these features were introduced.
## DATASETS
The <a href="https://github.com/Jeevan-0198/STUDENT-ENGAGEMENT-USING-EXCEL-AND-STATISTICS/raw/refs/heads/main/Datasets%20for%20Student%20Engagement.xlsx">Datasets</a> used for the analysis is taken from the 365 Data Science website.  
It includes fields such as student_id, paid status, minutes_watched_21, and minutes_watched_22, separately recorded for free and paid students.
## PROJECT EXPLANATION
To determine whether student engagement increased between Q4 2021 and Q4 2022, I performed hypothesis testing using statistical methods in Excel. Specifically, I compared the means of engagement separately for free and paid students during these periods. To improve accuracy and minimize errors, I also calculated the median and standard deviation.  
### Descriptive Statistics and Data Distribution
Before proceeding with hypothesis testing, I analyzed the dataset’s distribution by calculating skewness and kurtosis:
- **Skewness** helps determine the asymmetry of the distribution.
- **Kurtosis** measures the tailedness of the distribution, indicating the presence of extreme values.
For **paid plan** students:
- The mean increased significantly between Q4 2021 and Q4 2022.
- The median also increased, suggesting a consistent rise in engagement.
- Skewness was positive and increased significantly, indicating a right-skewed distribution. When skewness is high, the median often provides a more reliable central 
tendency measure than the mean.
- Kurtosis was greater than 3 (approximately 58), classifying the distribution as leptokurtic, meaning there is a higher likelihood of extreme values.
For **free plan** students:
- The mean increased, but the median decreased.
- Skewness increased significantly towards the right, suggesting extreme values heavily influence the mean.
- This combination (rising skewness but decreasing median) weakens our alternate hypothesis that engagement improved for free plan students.
### Confidence Interval Analysis
To further validate our hypothesis testing, I calculated **confidence intervals** for the means:
- A confidence interval represents a range within which the true population mean is likely to fall.
- For example, the 95% confidence interval for Q4 2021 (paid students) was between 318.86 and 499.43, with a mean of 332.5.
- If the confidence interval for Q4 2022 does not overlap significantly with Q4 2021, it supports the claim that engagement increased.
### Hypothesis Testing
#### Step 1: F-Test (Checking Variance Equality)
**F-Test Hypotheses:**
- Null Hypothesis (H₀): The variances of Q4 2021 and Q4 2022 are equal.
- Alternate Hypothesis (H₁): The variances of Q4 2021 and Q4 2022 are not equal.
**Decision Criteria:**
  - If P-value ≤ significance level (α = 0.05), reject the null hypothesis.
  - If P-value ≥ significance level, fail to reject the null hypothesis.
**Results**
- The P-value for both paid and free plan students was 0, which is below 0.05.
- This leads us to reject the null hypothesis and conclude that the variances are not equal.
- As a result, I proceeded with a T-Test assuming unequal variances (Welch’s T-Test).
**Step 2: T-Test (Comparing Means)**
  To determine whether engagement significantly increased, I performed a one-tailed T-Test with the following hypotheses:
   - Null Hypothesis (H₀): Engagement in Q4 2021 is greater than or equal to engagement in Q4 2022 (no significant improvement).
-  Alternate Hypothesis (H₁): Engagement in Q4 2021 is less than in Q4 2022 (significant improvement).
-  Decision Criteria:
    - If T-score ≥ T-critical value, reject H₀.
    - If P-value ≤ significance level (0.05), reject H₀.
