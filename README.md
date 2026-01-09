Analyzing Economic and Physical Patterns in Football Players Using FIFA 23 Data


Introduction

This project investigates how player attributes and physical characteristics relate to market value in professional football using the FIFA 23 Complete Player Dataset.
Player market value reflects a complex economic mechanism driven by performance ratings, physical traits, and expectations of future success.
The goal of this study is to analyze these relationships through exploratory data analysis, statistical hypothesis testing, and supervised machine learning.

Although multiple public datasets (Football Manager and Transfermarkt) were initially considered for enrichment, inconsistencies in player naming conventions prevented reliable merging within the project timeline.
Therefore, the final analysis focuses on a single, rich dataset (FIFA 23), emphasizing methodological depth rather than dataset quantity.


Motivation

Football transfers involve substantial financial investments influenced by player ratings, physical profiles, and future performance expectations.
Understanding how these measurable characteristics relate to market value provides insight into the economic logic behind player valuation.
This project aims to determine which attributes are most strongly associated with market value and how effectively they can predict it.


Objectives

Examine the relationship between player attributes and market value

Compare the strength of association between potential, physic, and BMI with market value

Statistically test which attributes are most strongly related to market value

Apply supervised machine learning models to predict player market value

Interpret results from both statistical and machine learning perspectives


Dataset and Source
Dataset	Description	Source
FIFA 23 Complete Player Dataset	Player attributes including age, height, weight, overall, potential, physic, and market value	https://www.kaggle.com/datasets/stefanoleone992/fifa-23-complete-player-dataset


Data Preparation and Feature Engineering

The dataset was cleaned by removing missing values and invalid physical measurements.
Only numeric and measurable attributes were retained.

To enrich the dataset, additional features were engineered:

Physical Index = height × weight

Body Mass Index (BMI) = weight / height²

These features allow analysis beyond raw attributes and support deeper economic interpretation.


Exploratory Data Analysis (EDA)

EDA was conducted using:

Histograms to examine variable distributions

Scatter plots to explore relationships between player attributes and market value

A correlation heatmap to identify linear associations

EDA reveals highly skewed market value distributions, strong non-linear relationships with rating-based variables, and substantial outliers among high-value players.

Hypothesis Testing
Comparative Hypothesis Testing

To determine which player attributes are most strongly associated with market value, a comparative hypothesis testing framework was applied using Spearman correlation analysis, which is robust to skewness and outliers.

Hypothesis:
Player potential exhibits a stronger relationship with market value than physical attributes such as physic rating and BMI.

Results
Variable |	Spearman ρ	| p-value
Potential|	0.776	< 0.001
Physic|	0.412	< 0.001
BMI	|0.092	< 0.001

Results indicate that player potential has the strongest and most statistically significant relationship with market value, while physic shows a moderate association and BMI a weak association.
This suggests that football player valuation is driven primarily by expectations of future performance rather than raw physical characteristics.



Machine Learning
Model Setup

A supervised learning approach was applied to predict player market value.
The dataset was split into training and testing sets using an 80/20 split, and features were standardized.

Models Applied

Linear Regression (baseline, interpretable model)

K-Nearest Neighbors (KNN) Regression with K = 5

Model Performance
Model|	MAE (€)|	RMSE (€)|	R²
Linear Regression| 228,409|	468,423|	0.386
KNN (k=5)|	16,717|	153,781|	0.9995
Interpretation

Linear Regression captures global trends but struggles due to the highly skewed distribution of market values.
KNN achieves extremely high performance by exploiting local similarity between players, indicating strong memorization effects.
While effective within the dataset, KNN’s generalization ability beyond this data may be limited.

Limitations and Future Work

The analysis relies on a single dataset, which may reflect FIFA’s internal valuation logic.

Market value is influenced by external factors not captured in the dataset (league popularity, contracts, media exposure).

Future work may include integrating Transfermarkt or Football Manager data using improved name-matching techniques.

Additional validation using alternative seasons or cross-validation methods could improve robustness

Tools and Technologies

Python

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn

SciPy



AI Usage Disclosure

AI assistance (ChatGPT) was used for debugging, workflow structuring, and improving documentation clarity.
All analysis decisions, code execution, and interpretations were reviewed and verified by the author.

Conclusion

This project demonstrates that player potential is the dominant driver of market value within FIFA 23 data.
By combining exploratory analysis, statistical hypothesis testing, and machine learning models, the study provides a data-driven view of football player valuation.
The results highlight the importance of future performance expectations over raw physical characteristics in determining market value.




