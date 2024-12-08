# Predicting-Customer-Churn-at-SyriaTel-A-Strategic-Analysis-to-Improve-Retention
This project predicts customer churn at SyriaTel, a telecommunications company, using data science and machine learning. It analyzes historical data to identify churn patterns, helping SyriaTel improve retention, reduce revenue loss, and make informed decisions through a binary classification model.

## Table of Contents 
1. [Business Understanding](#Business-Understanding)
2. [Problem Statement](#Problem-Statement)
3. [Objectives](#Objectives)
4. [Success metrics](#Success-Metrics)
5. [Data Understanding and Preparation](#Data-Understanding-and-Preparation)
6. [Data Visualization and Analysis](#Data-Visualization-and-Analysis)
7. [Conclusion](#Conclusion)
8. [Recommendations](#Recommendations)
9. [Next Steps](#Next-Steps)
10. [Reference](#References)

## Business Understanding 
Churn, also known as customer attrition, refers to the percentage of customers who discontinue or stop using a company’s services during a given period. For telecommunications companies like SyriaTel, churn is a critical metric because it directly impacts revenue growth and profitability. When a customer leaves, the company not only loses the revenue from that customer but also incurs higher costs in trying to acquire new customers to replace them.

Acquiring new customers is significantly more expensive than retaining existing ones, [with estimates suggesting that it's up to 5 times more costly](https://www.surveysensum.com/customer-experience/saas-customer-retention#:~:text=The%20same%20study%20shows%20that,and%20addressing%20clients'%20evolving%20needs.). In a highly competitive global market, telecom companies face the constant challenge of retaining customers who have various options and can easily switch providers. High churn rates increase the costs of acquiring new customers and maintaining market share, affecting a company’s ability to grow and invest in new technologies or services.

Predicting and reducing churn is not only essential for sustaining SyriaTel’s market position but also for ensuring its capacity to grow, innovate, and provide competitive services in a rapidly evolving industry.

## Problem Statement
SyriaTel, a telecommunications company, is facing a high customer churn rate, negatively impacting its revenue growth and profitability. Customer acquisition is up to five times more expensive than retaining existing customers, making this a significant financial challenge. In an increasingly competitive market with numerous alternatives for customers, high churn rates make it difficult for SyriaTel to maintain its market share, reinvest in innovation, and achieve long-term growth.

## Objectives
1. To Identify Churn Rates by Region and which region is highly affected.
2. To examine the impact of Account Length on Churn. Which customers are highly prone to attrition.
3. To assess the influence of subscription plans (voicemail and international plans) on churn.
4. To evaluate the impact of customer service calls on churn and determine if there is a statistically significant relationship.
5. To predict churn by focusing on the most influential features that drive customer behavior and retention patterns.

## Success Metrics
The success metric for this project would be to achieve a recall rate of at least 70%, ensuring that the model identifies a significant percentage of customers at risk of churning. This will allow the business to proactively target retention efforts, minimizing customer loss while balancing the cost of engaging non-churners. With this, SyriaTel will take timely retention actions and allocate resources more effectively to prevent churn.

## Data Understanding and Preparation

This dataset was obtained from [kaggle](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset?resource=download) and contains customers' data from SyriaTel, a telecommunications company. It includes various features related to customer behavior, usage patterns, and service details, which are crucial for analyzing customer churn and understanding the factors that influence retention. The dataset entails 21 columns and 3333 rows. 

The cleaning of this dataset entailed dealing with outliers, dealing with duplicates, checking for missing values which the dataset didn't have, harmonizing the various data types and also operating both dummy encoding and label encoding in preparation of the data for modeling.

## Data Visualization and Analysis

**1. To Identify Churn Rates by Region and which region is highly affected.**

![Churns by Region](https://github.com/user-attachments/assets/8eb75eea-5dae-4896-9df4-a877640753e8)

**Interpretation**

- Area Code 408, presents to have the highest Churn Rate followed by 510 then 415.
  
**2. To examine the impact of Account Length on Churn. Which customers are highly prone to attrition.**

![Churns by account length](https://github.com/user-attachments/assets/0d8527ec-e438-47bc-ba75-ff11b7b9274d)

**Interpretation**

- The analysis shows that long-term customers (over 14 years) have the highest churn rate, followed by short-term customers (7 years or less) with the second-highest churn rate, while mid-term customers (7-14 years) exhibit the lowest churn rate.

**3. To assess the influence of subscription plans (voicemail and international plans) on churn.**

![Churns by subscription plans](https://github.com/user-attachments/assets/90fc3ced-27a3-4e25-844f-30ccf1bd0547)

**Interpretation**

- Customers with an International Plan but no Voicemail Plan have the highest churn rate, followed by those with both plans, while customers without either plan have the third-highest churn rate, and those with only a Voicemail Plan have the lowest churn rate.

**4. To evaluate the impact of customer service calls on churn and determine if there is a statistically significant relationship.**

![Churns by customer service](https://github.com/user-attachments/assets/b36800b4-464d-4618-848f-8e8a956c40ca)

**Interpretation**
- Both customers who churn (True) and those who don't churn (False) seem to have a relatively high number of customer service calls, with values around 0.7.

- In terms of hypothesis, the P-values for both T-test and Mann-Whitney tests presented to be >than 0.05. So, we failed to reject the null hypothesis with a conclusion that there is no statistically significant relationship between customer service calls and churn rate. In other words, the frequency of customer service calls does not have a significant impact on whether a customer churns or not. This implied that customer service is not a major factor influencing customer churn.

**5. To predict churn by focusing on the most influential features that drive customer behavior and retention patterns.**

Achieving this objective involved training four distinct models: basic logistic regression and decision tree models, along with enhanced versions of both. The second models incorporated feature selection, addressed class imbalance using class weights, applied regularization (for logistic regression), and employed hyperparameter tuning (adjusting max depth, min samples, and entropy) for the decision tree models.

Logistic regression and decision tree models were chosen as they are well-suited for analyzing the categorical nature of the target variable (churn).

These models were analysed further using four different metrics entailing, cross validation score, confusion matrix, ROC Curve and classification Report. 

- Based on validation score, the second logistic model presentred to have the highest score.
- Based on ROC-Curve, the Logistic Second Model,emerged as the best-performing model, achieving the highest TPR and lowest FPR, indicating effective optimization for churn prediction.
- Based on confusion matrix, the second logistic model recorded the highest number of true positives, outperforming others in correctly predicting churns. However, it also recorded more false positives, indicating a tendency to overpredict churn.
- Based on Classification report the emphasis was on recall, which tells how well is our model's ability in predicting churn. In this case as well, The second logistic model presented to have the highest recall compared to the rest.

Each of these metrics are further emphasized below.

**a).Cross Validation Score**

![image](https://github.com/user-attachments/assets/42e7de7d-3832-46fa-bb0d-9863dce94d19)

According to this metric, the Second Logistic Model has the highest validation score based on recall, as the primary focus is to identify as many churners as possible. This model outperforms the others by identifying a significantly higher proportion of churners.

**b).Confusion Matrix**

![Confusion matrix](https://github.com/user-attachments/assets/f20cef90-c55c-47a8-acf6-881a509ab7fb)

**Interpretation**

Logistic Regression Models:

-The second logistic model has a higher number of True Positives (78) but also a higher False Positive rate (150). This indicates that it may incorrectly classify a higher number of non-churn customers as churn, which could be problematic, depending on the cost of false positives. The first logistic model has fewer false positives and false negatives, but its True Positives (39) are lower, which suggests it may be under-predicting churn.

Decision Tree Models:

-Both decision tree models (baseline and second model) perform similarly, with a relatively higher True Positive (60) rate and fewer False Positives compared to logistic regression. The decision tree models seem to strike a better balance between identifying churn customers correctly and avoiding false positives.

**c).Classification Report**
- For Logistic Regression:
  
![image](https://github.com/user-attachments/assets/ff6718a5-882c-4b57-ab55-b4526e686ef8)

- For Decision Tree:
  
![image](https://github.com/user-attachments/assets/638e09f5-d28d-4cf8-b3a8-b1497e236e47)

According to this metric, this is how the models perform,

- Logistic Baseline Model performs well for non-churn customers(high recall and precision for class 0)but has difficulty identifying churn.This suggests a high number of false negatives (failing to predict churn).

- Logistic Second Model improves churn prediction compared to the baseline model but at the cost of misclassifying more non-churn customers as churn (lower recall for class 0).

- Decision Tree Models (both baseline and second) perform well for non-churn customers, but their performance in detecting churn is still not optimal, with relatively low recall for churn.

**b).ROC Curve**

![ROC Curve](https://github.com/user-attachments/assets/5bdd7be6-e2ee-4a97-8425-9e1e21853871)

**Interpretation**

- Logistic Baseline Model: Performs well but is outperformed by the logistic second model, showing room for improvement in feature selection or tuning.

- Logistic Second Model: The best-performing model, achieving the highest TPR and lowest FPR, indicating effective optimization for churn prediction.

- Decision Tree Baseline Model: Provides moderate performance, but its ROC curve suggests it struggles with generalization compared to the logistic models.

- Decision Tree Second Model: Shows slight improvement over the baseline decision tree, but still lags behind the logistic models in predictive power.

**Final Model**

The second logistic regression model emerged as the best-performing model across multiple evaluation metrics. It achieved the highest validation score, indicating robust overall performance. On the ROC curve, it demonstrated effective optimization for churn prediction, with the highest True Positive Rate (TPR) and lowest False Positive Rate (FPR). The confusion matrix highlighted its strength in correctly predicting churn with the highest number of true positives, although it also showed a tendency to overpredict with increased false positives. Additionally, the classification report emphasized its superior recall, reflecting the model's strong ability to identify churn cases accurately.

Based on the analysis of the models, the second logistic regression model is the best choice for predicting customer churn at Syria Tel. While it has a slightly higher False Positive rate, its superior recall score indicates that it is more effective at identifying churners, which is the primary goal for this business problem. By capturing more churners (True Positives), the model offers a better chance to retain high-risk customers, which is more cost-effective than failing to identify churners and losing them to competitors.

Although the higher False Positive rate poses a risk of misclassifying non-churn customers as churners, the financial cost of reaching out to false positives is generally lower than the cost of not addressing actual churners. This trade-off makes this model more suitable for improving customer retention, which is crucial for SyriaTel’s profitability and long-term growth. This final model achieves the stated objective by optimizing the most critical features influencing churn prediction​,such as account details, usage metrics, customer service interactions, and geographic information. Given its potential, it should be prioritized for further tuning to optimize its accuracy and enhance customer retention strategies.


## Conclusion
- The highly affected region for churn is 408, which has the leading churn rate

- The churn rate analysis based on account length shows that long-term customers (over 14 years) have the highest churn rate, followed by short-term customers (7 years or less) with the second-highest churn rate, while mid-term customers (7-14 years) exhibit the lowest churn rate.

- The findings reveal that customers with an International Plan but no Voicemail Plan have the highest churn rate, followed by those with both plans, while customers without either plan have the third-highest churn rate, and those with only a Voicemail Plan have the lowest churn rate.

- The analysis indicates that the average number of customer service calls is relatively high for both churners and non-churners, with no statistically significant relationship between customer service calls and churn rate.

- Based on the analysis, the second logistic regression model stands out as the most effective for predicting customer churn at SyriaTel.It meets the success criteria achieving a 77% recall. While it has a slightly higher False Positive rate, its superior recall score ensures it effectively identifies churners, a critical aspect for enhancing retention strategies. The model highlights key factors influencing churn, including call charges, account length, geographic region, subscription options, and the number of calls/minutes relative to charges.

## Recommendations
- SyriaTel should conduct further research to identify the factors driving the high churn rate in the 408 region, which differs from others, and develop targeted strategies for improving customer retention.

- SyriaTel should focus on retaining long-term customers by addressing potential dissatisfaction and innovating offerings, while improving short-term customer satisfaction through better onboarding and support. Mid-term customers should be engaged with loyalty programs to maintain their retention.

- SyriaTel should focus on retaining International Plan customers, especially those without a Voicemail Plan, by offering cost-effective strategies like enhancing plan benefits, bundling services, and improving customer support.

- Since customer service calls are not significantly related to churn rate, S SyriaTel should shift focus to improving other key aspects of the customer experience, such as product quality, pricing, and service offerings, to enhance customer retention and reduce churn.

- Based on the findings, SyriaTel should prioritize further tuning and optimization of the second logistic regression model, as its superior recall score makes it more effective at identifying churners, thereby enhancing customer retention strategies and reducing churn.


## Next Steps
- Deploy the logistic regression model into SyriaTel's customer retention system. Integrate the model's predictions into real-time operations, such as CRM systems, to trigger automated retention actions like personalized offers or loyalty programs for at-risk customers.The model should also be continuously updated with new customer data to maintain its predictive power and accuracy over time.

- There is a need for a deep dive into the 408 region to gather customer feedback or detailed insights into regional challenges. Further qualitative analysis may be needed to understand if factors like service quality, local competition, or pricing are impacting retention.

- Implement a feedback loop to gather insights from customers who churn and those who stay, continuously improving the customer experience and identifying pain points that were not previously addressed. Additionally, a structured process is needed for collecting and acting on customer feedback.

## References

[SurveySENSUM].The Ultimate Guide to B2B SaaS Customer Retention: From Churn to Champion. (2023, August 24). https://www.surveysensum.com/customer-experience/saas-customer-retention#:~:text=The%20same%20study%20shows%20that,and%20addressing%20clients'%20evolving%20needs.




























