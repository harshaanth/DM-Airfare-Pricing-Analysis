# Airfare Pricing Analysis

This project is divided into two main parts: Exploratory Data Analysis (EDA) and Modeling. The analysis focuses on understanding the factors that influence airfare prices on various routes across the United States using data from the third quarter of 1996.

## Project Overview

The dataset includes information on 638 air routes, capturing various factors such as distance, passenger count, and whether a route is served by a discount airline like Southwest. The project aims to explore these factors through data visualization and build predictive models to forecast airfares.

## Part 1: Exploratory Data Analysis (EDA)

### Dataset

The dataset consists of the following variables:

### Numerical Variables
- **New**: Indicator if the route is new
- **Distance**: Distance between two airports (in miles)
- **Pax**: Number of passengers on the route
- **Coupon**: Number of coupons (stops) required

### Categorical Variables
- **Vacation**: Whether the route is to a vacation destination (Yes/No)
- **Sw**: Whether the route is served by Southwest Airlines (Yes/No)
- **Slot**: Whether there is a slot control at the airport (Yes/No)
- **Gate**: Whether there is a gate constraint at the airport (Yes/No)

### Dependent Variable
- **Fare**: The airfare for the route

### Analysis Steps

#### 1. Data Exploration
- **Missing Values**: Identified and removed rows with missing values in `sw`, `distance`, `coupon`, and `fare` due to their small number.
- **Numerical Data Exploration**: Created histograms and boxplots for numerical variables using Tableau to identify outliers.
- **Categorical Data Exploration**: Analyzed categorical variables using boxplots in Tableau to observe their impact on airfare.

#### 2. Correlation and Trends
- **Scatter Plots with Trend Lines**: Generated scatter plots to explore relationships between `fare` and other numerical variables.
  - **Fare vs. Coupon**: Positive correlation; more stops generally lead to higher fares.
  - **Fare vs. Distance**: Positive correlation; longer distances typically result in higher fares.
  - **Fare vs. Pax**: Negative correlation; more passengers generally lead to lower fares.

#### 3. Categorical Variable Analysis
- **Box Plots**: Examined the relationship between `fare` and categorical variables.
  - **Congestion**: Higher fares were observed when there were airport congestion issues.
  - **Southwest Airlines**: Fares were lower on routes served by Southwest Airlines.
  - **Vacation Routes**: Vacation routes tended to have lower fares.

## Part 2: Modeling

### Modeling Overview

After conducting the EDA, the next step involved building predictive models to forecast airfares based on the variables identified. This section of the project focuses on applying statistical and machine learning techniques to model the relationship between the independent variables and airfare.

### Modeling Process

#### 1. Model Selection
- **Linear Regression**: Chosen as the baseline model due to the continuous nature of the dependent variable (fare). It was used to understand the direct relationship between each independent variable and airfare.
- **Multiple Regression Analysis**: Conducted to account for the impact of multiple variables simultaneously, providing a more comprehensive understanding of how these factors interact to influence airfare.

#### 2. Feature Engineering
- **Interaction Terms**: Created interaction terms between variables such as `distance` and `pax` to explore how combinations of factors affect airfare.
- **Categorical Variables**: Encoded categorical variables using dummy variables to include them in the regression models.

#### 3. Model Evaluation
- **R-Squared**: Evaluated the models using R-squared to determine the proportion of variance in airfare that is predictable from the independent variables.
- **Adjusted R-Squared**: Used adjusted R-squared to account for the number of predictors in the model and prevent overfitting.
- **P-Values**: Analyzed p-values to identify statistically significant predictors of airfare.

### Key Findings
- **Distance and Fare**: Confirmed a strong positive correlation between distance and fare. Longer routes generally result in higher airfares.
- **Passenger Count (Pax)**: Found that higher passenger numbers on a route typically lead to lower fares, likely due to economies of scale.
- **Southwest Airlines**: The presence of Southwest Airlines on a route significantly reduces fare, consistent with its low-cost business model.
- **Vacation Routes**: Routes to vacation destinations tend to have lower fares, possibly due to competitive pricing in these markets.

## Conclusion

This project provided valuable insights into the factors that affect airfare pricing. The EDA phase helped identify key trends and relationships, while the modeling phase provided a framework for predicting airfare based on these factors.
