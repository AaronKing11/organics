# Organic Product Sales Analysis

## Overview

This project aims to develop a predictive model to identify customers likely to purchase organic products from a supermarket. By analyzing the data from the supermarket's loyalty program, we aim to understand key factors influencing organic product purchases and provide actionable recommendations for increasing organic product sales.

## Business Problem

The supermarket's management seeks to:
1. Identify customers most likely to purchase organic products.
2. Develop a customer profile for organic product buyers.
3. Assess whether these customers are more profitable than others.

## Data Description

The dataset used contains customer information from the supermarket's loyalty program. It includes 13 variables such as:
- **DemAffl**: Affluence grade (Interval)
- **DemAge**: Customer's age (Interval)
- **DemGender**: Gender of the customer (Nominal)
- **TargetBuy**: Whether the customer purchased organic products (Binary)

The dataset has over 22,000 observations, with some missing values that were addressed through data cleaning techniques.

## Methodology

### Exploratory Data Analysis (EDA)
We performed an initial analysis to identify key insights:
- Younger customers (under 40) are more likely to purchase organic products.
- Higher affluence correlates with a higher likelihood of buying organic products.
- Gender analysis showed that customers with unknown gender are less likely to buy organic products.

### Model Development
We created four models:
1. **Decision Tree (Max depth = 25)**
2. **Decision Tree (Max depth = 20)**
3. **Random Forest**
4. **Gradient Boosting**

Each model was evaluated based on accuracy, precision, recall, and AUC.

### Final Model
The **Gradient Boosting model** was chosen as the final model, as it outperformed the others in three of the four metrics.

## Key Findings
- **Affluence and Age**: Customers with higher affluence and younger age are more likely to buy organic products.
- **Gender Impact**: Customers with unknown gender are less likely to buy organic products.
- **Region**: Urban affluent neighborhoods show the highest potential for organic product sales.

## Example Customer Profile
- **Example Buyer**: A young, affluent customer in their 30s, living in an upscale urban neighborhood, likely with young children.

## Recommendations
- **Target Younger, Affluent Customers**: Focus marketing campaigns on customers aged under 40 with higher affluence.
- **Expand Availability in Affluent Urban Regions**: These areas present the highest sales potential.
- **Personalized Promotions**: Use coupons and special promotions to engage potential organic product buyers.
- **Address Gender Data Issues**: Investigate and address the barriers for customers with unknown gender information.

## Technical Appendix
### Data Preparation
- Missing values were handled by dropping rows with missing data, leaving 16,408 observations.
- Dummy variables were created for categorical variables.

### Model Specifications
- **Decision Tree #1**: Max depth = 25, Min samples = 80, ccp = 0.001
- **Decision Tree #2**: Max depth = 20, Min samples = 10, ccp = 0.001
- **Random Forest**: 150 estimators, Max depth = 50, Min samples = 30
- **Gradient Boosting**: 100 estimators, learning rate = 0.1, Max depth = 3

### Evaluation Metrics
- The Gradient Boosting model showed the highest performance in three of the four evaluation metrics, making it the best choice for the final model.

### Exploratory Data Analysis (EDA)
We performed an initial analysis to identify key insights:
- Younger customers (under 40) are more likely to purchase organic products.
- Higher affluence correlates with a higher likelihood of buying organic products.
- Gender analysis showed that customers with unknown gender are less likely to purchase organic foods.
