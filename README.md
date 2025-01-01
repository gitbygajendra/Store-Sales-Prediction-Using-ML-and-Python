Store Sales Prediction Using Machine Learning and Python
Abstract:
This project aims to predict sales for various retail stores based on the available dataset attributes. Predictive analytics can help us understand the factors influencing a store's sales performance, enabling accurate sales forecasting. By using various machine learning techniques, we sought to identify the best algorithm for the problem. Our approach involved implementing standard regression techniques and boosting algorithms, with the latter delivering superior results compared to regular regression models.

Introduction:
Sales prediction is a crucial aspect of business intelligence, helping businesses forecast future sales and optimize operations. It becomes challenging when data is incomplete, missing, or contains outliers. While time series methods are commonly used for sales prediction, regression techniques often yield better results. Machine learning models can help uncover patterns in sales data, enabling better predictions. Among the most effective models are tree-based algorithms, which excel in identifying complex patterns in sales dynamics.

Methodology:
The data exploration process revealed that some stores were not open on certain days, allowing us to safely remove records with closed stores or those with no sales. We identified a correlation between sales and the number of customers on any given day. By plotting trends, we confirmed that customer count was a significant factor in determining sales. Further analysis showed that sales varied depending on the day of the week, with certain days having stronger correlations with sales.

We also discovered that Easter holidays were missing from the dataset, complicating predictions for test data containing these holidays. Promotions had a noticeable impact on sales, while school holidays had little to no effect. Additionally, store type played a role in sales performance, with some types correlating more strongly with sales and customer numbers.

Given that the dataset contained both discrete features (e.g., day, week, store type, promotions) and continuous variables (e.g., sales), decision trees emerged as a natural starting point. Decision trees helped identify the most important features affecting sales, with customer count and average sales per customer standing out. We then explored ensemble methods, including Adaboost and Random Forest, which improved performance by 0.0608 and 0.0599 on the validation set, respectively. Notably, Random Forest showed reduced variance compared to Adaboost. Finally, we used XGBoost, a gradient boosting model, which provided the best results on the dataset.

Results:
Adaboost sometimes outperformed Random Forest, showing better scores and variance. However, XGBoost produced the most accurate results, with its feature selection differing from other models. Features like average sales per month or day of the week did not significantly improve predictions, likely due to overfitting when extrapolating data not present in the test set. Nonetheless, using XGBoost enabled us to make reliable sales predictions for the stores.

This approach demonstrates the effectiveness of machine learning in predicting retail sales, with XGBoost proving to be the most reliable algorithm for the given dataset.
