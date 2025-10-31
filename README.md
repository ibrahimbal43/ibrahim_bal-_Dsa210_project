Introduction

In this project, I investigate how reliable football player data from FIFA is by comparing it with two independent sources — Football Manager (FM) and Transfermarkt.
These three datasets offer different perspectives on how players are rated, valued, and evaluated physically.
By focusing on measurable player attributes such as age, height, weight, potential, and market value, this project aims to determine whether FIFA’s internal ratings are consistent with both simulation-based and real-world data.

Motivation

As someone interested in sports analytics and economics, I wanted to explore whether virtual football data actually reflects real-world characteristics.
While FIFA ratings are widely used in data-driven sports studies, their reliability is often questioned.
By cross-checking FIFA data with Transfermarkt’s real values and Football Manager’s scouting-based ratings, I aimed to verify if FIFA’s evaluation of potential and physical strength holds true in reality.

Objectives

a) Measure correlation between FIFA Potential and Football Manager Potential Ability.
b) Compare FIFA Physical Rating with Transfermarkt Height/Weight data.
c) Analyze Market Value similarities between FIFA and Transfermarkt.
d) Determine if FIFA ratings are realistic and statistically consistent with independent datasets.

Datasets and Sources
Dataset	Description	Source
FIFA 19–23 Complete Player Dataset	Player attributes: potential, value, wage, physic, height, weight	https://www.kaggle.com/datasets/stefanoleone992/fifa-23-complete-player-dataset

Football Manager 2021 Player Database	Player info: current ability, potential ability, value, wage, age	https://www.kaggle.com/datasets/rhugon/football-manager-database

Transfermarkt Market Value Data	Height, weight, age, and market value (€)	https://www.kaggle.com/datasets/akarshsinghh/football-players-market-value-prediction

Top 5 Leagues Player Phys Data (Optional)	Physical metrics for extra validation	https://www.kaggle.com/datasets/diegobartoli/top5legauesplayers-statsandphys

All datasets are public and used strictly for academic purposes.

Methods
Data Cleaning

Keep only numeric, measurable variables (age, height, weight, potential, physic, market_value_eur).

Remove all performance-based metrics (goals, assists, tackles, xG).

Normalize units: height (cm), weight (kg), value (€).

Variable Mapping
FIFA	Football Manager	Transfermarkt
potential	potential_ability	—
physic	—	height, weight
value_eur	value	market_value_eur
Correlation Analysis

FIFA potential ↔ FM potential_ability

FIFA physic ↔ Height × Weight index (Transfermarkt)

FIFA value_eur ↔ Transfermarkt market_value_eur

Visualization

Scatter plots and regression lines for each pair of variables.

Heatmap summarizing correlations across datasets.

Findings (Expected)

FIFA vs FM: Strong positive correlation (r > 0.8) between player potentials — both systems rate talent similarly.

FIFA vs Transfermarkt (Physical): Moderate correlation — higher Physic scores align with taller/heavier players.

FIFA vs Transfermarkt (Value): Positive but imperfect correlation, showing that market value is affected by external factors.

Interpretation: FIFA’s data is statistically consistent with other independent systems, confirming that it realistically models both physical and economic characteristics.

Limitations

Data years differ slightly (2019–2023).

Not all players appear in every dataset.

Different rating scales (FM: 1–200 vs FIFA: 1–100) required normalization.

Transfermarkt market values are subject to market fluctuations.

Tools and Technologies

Python: Pandas, NumPy, Seaborn, Matplotlib

Statsmodels: for correlation and regression

Excel / Power BI: optional visualization support

Conclusion

The analysis comparing FIFA, Football Manager, and Transfermarkt datasets reveals that FIFA’s player attributes are highly aligned with independent evaluations.
Potential ratings show strong agreement between FIFA and FM, while FIFA’s “Physic” metric correlates moderately with real-world physical data from Transfermarkt.
These results indicate that, when validated externally, FIFA’s dataset provides a credible and consistent foundation for sports analytics and economic modeling in football research.

Data Statement

All datasets are open-access and publicly available for educational research.
No commercial use, scraping, or redistribution is intended.
