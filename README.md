# Portfolio1 & 2 Projects

## Table of Contents
- [Portfolio 1: E-commerce Dataset Analysis](#portfolio-1-e-commerce-dataset-analysis)
- [Portfolio 2: Linear Regression Models on E-commerce Sub-dataset](#portfolio-2-linear-regression-models-on-e-commerce-sub-dataset)

## Portfolio 1: E-commerce Dataset Analysis

In my first portfolio for this unit, I worked with an E-commerce dataset, which was a great starting point for me as someone with no prior IT or coding experience. Through this project, I learned various data management techniques, such as identifying and handling null values, cleaning data, and analyzing descriptive statistics.

### Descriptive Statistics

I focused on understanding the descriptive statistics from different attributes, such as:
- Target variable
- Gender
- Unique customer IDs
- Rating reviews

### Data Visualization

I learned how to visualize data through plotting and analysis. One of the challenges I embraced was creating a boxplot to represent the correlation between:
- Gender
- Helpfulness
- Category
- Ratings

### Outlier Detection and Removal

In the final part of this project, I tackled the task of detecting and removing outliers based on three specific criteria:
1. Reviews with a helpfulness score of no more than 2.
2. Users who rated fewer than 7 items.
3. Items that received fewer than 11 ratings.

I completed this process step-by-step, documenting the data at each stage and summarizing the percentage of data removed for clarity.

### Conclusion

Overall, this project helped me build a solid foundation in data analysis and visualization, and I am confident in my ability to manage and interpret data effectively.

## Portfolio 2: Linear Regression Models on E-commerce Sub-dataset

In Portfolio 2, the objective was to train linear regression models to predict users' ratings towards items using a cleaned and combined e-commerce sub-dataset. This dataset differed from the one used in the first task of analyzing an e-commerce dataset.

### Data Exploration and Preparation

The process began with data exploration and preparation, where I used functions like `head`, `describe`, and `info` to understand the dataset. I encoded categorical variables ['gender', 'category', 'review'] into numeric data using the `OrdinalEncoder` function to facilitate analysis.

### Correlation Analysis

Next, I calculated correlations between 'helpfulness', 'gender', 'category', 'review', and 'rating' using the `corr()` function. This approach revealed that all focused targets had weak negative relationships with 'rating', with 'category' showing the highest correlation and 'helpfulness' the least. This was a departure from the first portfolio, where the `groupby` function was used to examine relationships.

### Model Training and Evaluation

The dataset was then split into training and testing sets under two cases:
- **Case 1:** 10% training data
- **Case 2:** 90% training data

Linear regression models were trained using the most correlated features ['category', 'review'] and the least correlated features ['gender', 'helpfulness'], resulting in four models:
- **Model A:** Most correlated features, Case 1
- **Model B:** Least correlated features, Case 1
- **Model C:** Most correlated features, Case 2
- **Model D:** Least correlated features, Case 2

### Performance Evaluation

Performance evaluation using RMSE revealed the following results:
- **Model A:** MSE = 1.7766, RMSE = 1.3329
- **Model B:** MSE = 1.8605, RMSE = 1.3640
- **Model C:** MSE = 1.6820, RMSE = 1.2969
- **Model D:** MSE = 1.7245, RMSE = 1.3132

Graph analysis showed that models using the most correlated features generally performed better. Model C had the lowest RMSE, indicating the most accurate predictions.

### Conclusion

This portfolio demonstrated the importance of feature selection and training data size in improving model accuracy. Additionally, it included an exercise comparing two tables from the 2008 Summer Olympics, illustrating how different ranking methods can influence interpretations of success, highlighting the need for clear and neutral data presentation to avoid misleading conclusions.
