# Predicting-Customer-Churn-at-SyriaTel-A-Strategic-Analysis-to-Improve-Retention
This project predicts customer churn at SyriaTel, a telecommunications company, using data science and machine learning. It analyzes historical data to identify churn patterns, helping SyriaTel improve retention, reduce revenue loss, and make informed decisions through a binary classification model.

## Business Understanding 
Churn, also known as customer attrition, refers to the percentage of customers who discontinue or stop using a company’s services during a given period. For telecommunications companies like SyriaTel, churn is a critical metric because it directly impacts revenue growth and profitability. When a customer leaves, the company not only loses the revenue from that customer but also incurs higher costs in trying to acquire new customers to replace them.

Acquiring new customers is significantly more expensive than retaining existing ones, with estimates suggesting that it's up to 5 times more costly. In a highly competitive global market, telecom companies face the constant challenge of retaining customers who have various options and can easily switch providers. High churn rates increase the costs of acquiring new customers and maintaining market share, affecting a company’s ability to grow and invest in new technologies or services.

Predicting and reducing churn is not only essential for sustaining SyriaTel’s market position but also for ensuring its capacity to grow, innovate, and provide competitive services in a rapidly evolving industry.

## Problem Statement
SyriaTel, a telecommunications company, is facing a high customer churn rate, negatively impacting its revenue growth and profitability. Customer acquisition is up to five times more expensive than retaining existing customers, making this a significant financial challenge. In an increasingly competitive market with numerous alternatives for customers, high churn rates make it difficult for SyriaTel to maintain its market share, reinvest in innovation, and achieve long-term growth.

## Objectives
1. To Identify Churn Rates by Region and which region is highly affected.
2. To examine the impact of Account Length on Churn. Which customesrs are highly prone to attrition.
3. To assess the influence of subscription plans (voicemail and international plans) on churn.
4. To evaluate the impact of customer service calls on churn and determine if there is a statistically significant relationship.
5. To predict churn by focusing on the most influential features that drive customer behavior and retention patterns.

## Success Metrics
The success metric for this project would be to achieve a recall rate of at least 70%, ensuring that the model identifies a significant percentage of customers at risk of churning. This will allow the business to proactively target retention efforts, minimizing customer loss while balancing the cost of engaging non-churners. With this, SyriaTel will take timely retention actions and allocate resources more effectively to prevent churn.

## Data Understanding

This dataset was obtained from [kaggle](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset?resource=download) and contains customers' dafta from SyriaTel, a telecommunications company. It includes various features related to customer behavior, usage patterns, and service details, which are crucial for analyzing customer churn and understanding the factors that influence retention. The dataset entails 21 columns and 3333 rows. The columns are explained below:

**1. state:** Represents the state or region where the customer resides.

**2. Account length:** This represents the number of months a customer has been with the company.

**3. area code:** This is part of the customer's phone number that indicates their region.

**4. phone number:** This is a unique identifier for each customer’s phone.

**5. international plan:** Indicates whether the customer has an international calling plan. This may help identify whether international usage affects churn.

**6. voice mail plan:** Indicates whether the customer subscribes to a voicemail service.

**7. Number vmail messages:** The number of voicemail messages left by the customer.

**8. Total day minutes:** The total number of minutes a customer spends on calls during the day.

**9. Total day calls:** The total number of calls made during the day.

**10. Total day charge:** The total cost of the customer's calls during the day.

**11. Total eve calls:** The total number of calls made during the evening.

**12. Total eve charge:** The total cost of calls made during the evening.

**13. Total night minutes:** The total number of minutes spent on calls during the night.

**14. Total night calls:** The total number of calls made during the night.

**15. Total night charge:** The total cost of calls made during the night.

**16. Total intl minutes:** The total number of minutes spent on international calls.

**17. Total intl calls:** The total number of international calls made by the customer.

**18. Total intl charge:** The total cost of international calls.

**19. customer service calls:** The number of calls made by the customer to the customer service department. A high number may indicate issues or dissatisfaction.

**20. churn:** This is the target variable, indicating whether the customer has churned (True) or not (False).
















