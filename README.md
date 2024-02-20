#Bootcamp Final Project - Housing Price Regression Model (Random Forest)

**Introduction**
This project encompasses the development of a machine learning model to predict housing prices using a synthetic dataset specifically crafted for this purpose. The objective was to construct a regression model that can accurately estimate the value of a property based on various features, with a target R² score of 80 as a benchmark for performance.

**Exploratory Data Analysis (EDA)**
The initial phase of the project involved an exploratory data analysis (EDA) to understand the data's characteristics and underlying structure. Through this process, the following insights were gained:

-Price Distribution: The histogram of housing prices revealed a normal distribution, indicating no significant skewness that would require data transformation. ![Distribution of Price](/Images/distribution_of_price.png)
*Figure 1: Histogram showing the distribution of housing prices.*
![Area vs Price]((https://github.com/tomseeber/bootcamp_project_final/tree/main/Images))
*Figure 2: Scatter plot illustrating the relationship between property area and housing prices, indicating potential linearity.*

![Bathrooms vs Price]((https://github.com/tomseeber/bootcamp_project_final/tree/main/Images))
*Figure 3: Scatter plot depicting how the number of bathrooms in a property correlates with the housing prices.*

![Bedrooms vs Price]((https://github.com/tomseeber/bootcamp_project_final/tree/main/Images))
*Figure 4: Scatter plot showing the association between the number of bedrooms and housing prices.*

-Correlation Insights: A heatmap of the correlation matrix showed that certain features like 'sqft_living' and 'grade' had a strong positive correlation with the price, suggesting their significant influence on the housing prices.
![Correlation Matrix]((https://github.com/tomseeber/bootcamp_project_final/tree/main/Images/coorelation_matrix.png))
*Figure 6: Heatmap of the correlation matrix visualizing the strength and direction of the relationship between the features.*

-Feature Relationships: Scatter plots of the most correlated features against the price highlighted the existence of linear relationships, affirming the suitability of regression models for this prediction task.

-Categorical Variables: Box plots for categorical variables, if present, would show the variance in housing prices across different categories, indicating the impact of these variables on the price.

**Data Cleaning and Pre-processing**
Data cleaning and preprocessing were meticulously carried out to ensure the quality and integrity of the dataset. This process included:

-Handling Missing Values: Missing values were identified and imputed where appropriate to maintain the dataset's consistency.

-Outlier Detection: Outliers were detected through IQR score analysis and were treated to prevent them from skewing the model's predictions.

-Feature Engineering: New features were engineered to better capture the nuances of the housing market, such as creating a 'price_per_sqft' feature, which provided additional predictive power to the model.

**Model Building**
The Random Forest Regressor was selected due to its robustness and ability to model complex nonlinear relationships. This ensemble method combines multiple decision trees to produce a more accurate and stable prediction.

-Hyperparameter Optimization: The model was tuned using RandomizedSearchCV to find the optimal set of hyperparameters, ensuring the best possible balance between bias and variance.

-Feature Selection: Post hyperparameter tuning, the feature importances were evaluated, and the model was refined to include only the most significant features, which improved the model's interpretability and efficiency.

**Optimization Attempts**
To achieve the goal of an R² score of 80, several optimization strategies were employed:

-Overfitting Prevention: Techniques such as cross-validation and pruning were used to ensure that the model generalized well to unseen data.

-Model Refinement: The model was iteratively refined, using insights from each round of cross-validation to adjust the hyperparameters and feature set.

**Model Evaluation**

The model's performance was rigorously evaluated using multiple metrics:

-Final R² Score: The Random Forest model achieved a remarkable R² score of 90 on the test set, surpassing the target goal and indicating a high level of predictive accuracy.

-Cross-Validation Consistency: The cross-validation scores closely aligned with the test score, confirming the model's robustness and consistency across different data subsets.

**Conclusions**
The project met and exceeded the initial target with a final R² score of 90, demonstrating the model's strong predictive capabilities. The success of the model can be attributed to careful data preprocessing, strategic model tuning, and diligent validation practices.

Future work could explore alternative algorithms, deeper feature engineering, and the application of more advanced techniques such as neural networks or gradient boosting machines for comparison and potential performance improvements.

Technical Details
To replicate this analysis or for more technical information, please refer to the attached Jupyter notebooks which detail every step of the process, from initial data loading and cleaning to the final model training and evaluation.

