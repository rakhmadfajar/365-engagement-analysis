# 365-engagement-analysis
# Study Case - Customer Engagement Analysis in 365 Learning Website
## Introduction
In 2022, 365 company revamped its learning platform with gamification features (XP, coins, leaderboard), course library expansion, aiming to boost student engagement and company growth. This study case aims to help company to assess if the new additions to the platform have increased student engagement. Excel will be the main tool to analyze the data. 
## Phase 1: Ask
To evaluate the effectiveness of the 365 company's platform update, data analyst will compare user engagement with learning content by analyzing minutes watched. Specifically, they will compare watch time data from 2021 (pre-update) to 2022 (post-update) to determine if the platform changes.

**Key Objective**: Analyze by measuring pre- vs. post-update (2021-2022) impact on learning content engagement using minutes watched as the primary metric.

## Phase 2: Prepare
To analyze this, we will need 365 Company's user engagement data (minutes watched) in 2021 and 2022. Data can be obtained from the [365 website.](https://storage.googleapis.com/lms-365-production//project-uploads/downloadables/3/files.zip?GoogleAccessId=lms-nodejs-to-storage@abiding-cedar-292408.iam.gserviceaccount.com&Expires=1708400288&Signature=WLOccTuFjgKWKAMfhIPTnoVb8ag%2bQ5Ucvq8YQNCz89gbzNn2IQtjjIJoFIRaY3%2br3F7O2qP34dDlfBp7TFUZrxhFnaKu4FhFjtN5hk2aOmXWuWvukVl0mU7wXdPP3LOLxIWLWlcnLOc6IEPwSRqAVQ4sH7rWOBBcHnz8DPDETlQdv4jFBiLZlM3KvYXPv8RsKxDF0fa4AbqtC/97gRBHIUPFKuzYBZhWPJwJOj7EUDmsYAFkauP6JF0POu2tlncKeVgLPoVJWPRSYP%2b7UscEaLIUV1t2fY90vxPxyBROFzbfOYEiJsC4lNCz9Dqu7UyOHVpTt6WXmYLtqyeqZ7JrlQ==&response-content-disposition=attachment;%20filename%20=%22project-files-customer-engagement-analysis-in-excel.zip%22) 
 
**The Credibility and Privacy of The Data**:   This data originates from 365 Company's operations. To protect user privacy, personal information has been anonymized. Additionally, the data volume has been reduced for practical purposes. Despite these modifications, the data remains representative of the company's activities

## Phase 3: Process
**Tools needed**: Excel and Data Analysis ToolPak (Excel Add In)

Upon opening the data in Excel format, we'll find the data separated into 5 distinct sheets for comprehensive analysis.

Here is the columns data summary:
 -   **student_id:** Unique identifier for students using the platform in Q4 2021 & 2022 (free & paid accounts).
-   **student_country:** Geographic location of students.
-   **Paid:** Binary variable (1 = paid account, 0 = free/unpaid).
-   **minutes_watched_21 & 22:** Engagement level measured in minutes watched for Q4 2021 & 2022

## Phase 4: Analyzing

### Descriptive Statistics 
To understand the data better, I will use simple descriptive statistics to measure the central tendency and variability (standard deviation). The mean shows where most values would fall. The median represents the center value, unaffected by outliers. The standard deviation shows how scattered the data is around the mean.

#### Paid-Plan Students
![Paid Mean Median](https://i.ibb.co/02qtPCX/Paid-Mean-Median.png%22%20alt=%22Paid-Mean-Median)
- Mean : The mean minutes watched by paid-plan students **increased significantly**.  Data from 2021 and 2022 indicates a marked rise in activity among paid-plan users who previously showed low engagement.
- Median: The median minutes watched also **climbed**, indicating even the "middle-of-the-pack" student participated more. This suggests the **engagement boost wasn't limited to a few outliers** but spread more evenly across paid-plan users.
#### Free-Plan Students
![Free Mean and Median](https://i.ibb.co/G0939mT/Free-Mean-Median.png%22%20alt=%22Free-Mean-Median)
- Mean: Low minute mean on free-plan student in 2021 saw a **big jump** in 2022. While this suggest increased engagement, **it was still smaller than the paid plan-students**, indicating a gap.
- Median: While mean viewing time quadrupled, the median **free-plan students actually watched less**, indicating an increase by a few outliers not broader engagement. 

![Standard Deviations](https://i.ibb.co/hcW82p4/Paid-vs-Free-Standard-Deviation.png)
- Paid-Plan Standard Deviations: A very high change in the mean value followed by a slight median value indicates the presence of outliers. The **massive increase in standard deviation (28.21 to 854.58 minutes)** confirms this, highlighting a **wider range of engagement**, with some students watching a lot more and others barely any.
- Free-Plan Standard Deviations: Free-plan students followed a similar pattern to paid-plan users:  **both groups showed a wider range of engagement**. However, the **shift was smaller for free-plan users**, suggesting their engagement patterns changed less dramatically.
#### Skewness and Kurtosis
![Skewness and Kurtosis](https://i.ibb.co/0JSqNgK/Paid-vs-Free-Skewness-and-Kurtosis.png)
- **Increased Skewness Towards Right (Positive Skew):**
	-   Skewness increased significantly in 2022, indicating a **shift towards distributions with more observations concentrated on the left side and a longer tail on the right.** This suggests that **more students are watching significantly more content than the majority**.
	-   The smaller starting skewness (0.63) and sharper increase (to 7.07) compared to free-plan (1.17 to 15.06) **hint at a potentially larger shift towards extreme values** (high engagement) for paid-plan users. 

-  Increased Kurtosis (Heavy-Tailed Distributions):**
	-   Kurtosis increased significantly, indicating **distributions with heavier tails than normal.** This suggests the **presence of more outliers (both high and low engagement)** compared to a normal distribution.
	-   The dramatic increase in kurtosis (from 0.36 to 315.76) compared to paid-plan (from -0.85 to 58.48) suggests a **potentially larger shift towards extreme values** (both very high and very low engagement) for free-plan users. Again, this needs further analysis.
### Confidence Intervals
Paid-plan users watch much more than free-plan users on average, with statistical certainty.
**Breakdown:**
-   **Free-plan users:**  Average watch time in Q4 2022 was between 67 and 70 minutes (95% confidence interval).
![CI Free Plan](https://i.ibb.co/hy6D2rS/CI-Free-Plan.png)
-    **Paid-plan users:**  Average watch time in Q4 2022 was between 352 and 385 minutes (95% confidence interval).
![CI Paid Plan](https://i.ibb.co/54M8Nxc/CI-Paid-Plan.png)


-    The large difference in confidence intervals confirms that the difference in average watch time is  **statistically significant**, meaning it's unlikely due to chance.
- This aligns with the expectation that paid-plan students who have invested in the platform tend to be more engaged than free-plan users.
### Hypothesis Testing
In this phase, I will try to analyze and identify is there any impact given by new features by hypothesis testing for each type of users and country.  Comparing watch times in 2021 and 2022 for paid-plan and free-plan users helps identify changes in engagement, evaluate interventions, compare subgroups, and benchmark against industry standards. Tools used for displaying t-Test value is Data Analysis Tool Pak in Excel Add in.
![paid t test](https://i.ibb.co/MPbxyKN/Paid-Plan-t-Test.png)
-   **Significant decrease:**  The test found a  **statistically significant difference**  (p-value < 0.05) in watch time between Q4 2021 and Q4 2022 for paid-plan users.
-   **Lower in 2021:**  The t-statistic (-3.05) being negative indicates that  **students in Q4 2021 watched significantly less**  than those in Q4 2022.
-   **Further investigation:**  While the null hypothesis is rejected, it doesn't confirm the alternative hypothesis directly.
**Conclusion:**  **Reject null** because the p-value is lower than the specified significance level α (0.05).

![free t test](https://i.ibb.co/Y7sGPw5/Free-Plan-t-Test.png)
-   **No Significant Difference**: Two-sample t-test (unequal variances) found no significant difference in watch time between Q4 2021 and Q4 2022 (t-statistic = 29.78 > critical value).
-   This supports the null hypothesis:  **mean watch time in 2021 is not smaller than 2022**, potentially indicating higher or equal engagement in 2021.
-   This aligns with previous findings and highlights the different engagement patterns between paid and free-plan users.
- **Conclusion:**  **Fail to** **Reject** because the calculated **t-statistic** is higher than the critical value.

![usa vs in](https://i.ibb.co/99kT6W1/USA-vs-IN-t-Test.png)
In this part I will try to understand the differences in usage patterns. This can help in product localization. The platform might need to tailor its content, features, or user interface to better fit the preferences or needs of users in different regions. 

**Conclusion:**  **Fail to** **Reject** because the p-value is higher than the specified significance level α (0.05).

If the hypothesis that US students watch more or an equal amount of content as Indian students is rejected, this suggests that US students watch less content on average than students in India.

## Phase 5: Share and Act
**Overall findings:**

-   **Paid-plan students see a stronger increase in engagement**.
	-    The  **confidence interval**  confirms that  **paid-plan students watched significantly more**  than free-plan students in Q4 2022 (61.71 - 70.59 minutes vs. 351.99 - 384.72 minutes).
-   **Monetary investment**  might lead to  **higher usage**  due to seeking value for money.
-    **Free-plan students' median watch time decreased**, suggesting the current strategies might be  **less effective**  for them. This decrease could be due to various factors beyond the subscription model, such as:
	    -   **Changes in the platform**
	    -   **Competition from other platforms**
	    -   **Changes in the user base**
-   The platform needs  **personalized approaches**  for  **different user segments**.
-   Increased  **skewness and kurtosis**  in both groups suggest a  **growing number of high-engagement users**, especially among free-plan students in Q4 2022.
- Both the US and Indian markets could potentially benefit from **strategies to increase engagement**.
	-   **US market:**  If engagement is lower, targeted marketing efforts, content additions relevant to US students, or alternative strategies could be explored.
	-   **Indian market:**  Given their potentially higher engagement (based on the tested hypothesis), investing in further content and features catering to this audience might be strategically beneficial.

**Further analysis** is recommended to understand the **factors driving engagement** for each group and personalize strategies for optimal impact.
## Final: Thank You!
![asda](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExaTE3cmhsZ3lnbTB0czJwZGhyMTh2Zm5ia201dXdpOXczYnkzbHltbCZlcD12MV9naWZzX3NlYXJjaCZjdD1n/Lj9bGPMF9jmz4gk9QA/giphy.gif)
