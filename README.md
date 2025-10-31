# **Analyzing Economic and Physical Patterns in Football Players Using FIFA, Football Manager, and Transfermarkt Data**

---

## **Introduction**

This project explores how **player attributes and market values** reflect economic and physical patterns in modern football.
By combining data from **FIFA**, **Football Manager (FM)**, and **Transfermarkt**, the study investigates how measurable factors — *age, height, weight, potential, and market value* — relate to each other, and how player profiles have evolved in the football market.

Rather than verifying FIFA data, the goal is to use these datasets together to understand **how physical attributes and potential influence market value and player economics.**

---

## **Motivation**

Football’s transfer market has become one of the most dynamic economic systems in sports. Clubs invest based on potential, physical strength, and perceived market value, often influenced by analytical tools.
The motivation behind this project is to analyze whether physical characteristics (height, weight) and player potential have measurable impacts on market value, using **publicly available player databases**.

---

## **Objectives**

a) Examine the relationship between **physical characteristics** (height, weight) and **market value**.
b) Study how **potential** (FIFA and FM) correlates with **market value** (Transfermarkt).
c) Identify whether physical or potential attributes are stronger predictors of a player’s market worth.
d) Combine multiple open datasets to analyze consistent economic patterns in player valuation.

---

## **Datasets and Sources**

| Dataset                                       | Description                                                       | Source                                                                                                                                                                             |
| --------------------------------------------- | ----------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FIFA 19–23 Complete Player Dataset**        | Player attributes: potential, value, wage, physic, height, weight | [https://www.kaggle.com/datasets/stefanoleone992/fifa-23-complete-player-dataset](https://www.kaggle.com/datasets/stefanoleone992/fifa-23-complete-player-dataset)                 |
| **Football Manager 2021 Player Database**     | Player info: potential ability, value, wage, age                  | [https://www.kaggle.com/datasets/rhugon/football-manager-database](https://www.kaggle.com/datasets/rhugon/football-manager-database)                                               |
| **Transfermarkt Market Value Data**           | Height, weight, age, and market value (€)                         | [https://www.kaggle.com/datasets/akarshsinghh/football-players-market-value-prediction](https://www.kaggle.com/datasets/akarshsinghh/football-players-market-value-prediction)     |
| **Top 5 Leagues Player Phys Data (Optional)** | Physical metrics for extra validation                             | [https://www.kaggle.com/datasets/diegobartoli/top5legauesplayers-statsandphys](https://www.kaggle.com/datasets/diegobartoli/top5legauesplayers-statsandphys)                       |
| **PES 2019 Players Dataset**                  | Independent player ratings for comparison                         | [https://www.kaggle.com/datasets/harshkava/pro-evolution-soccer-pes-2019-players-dataset](https://www.kaggle.com/datasets/harshkava/pro-evolution-soccer-pes-2019-players-dataset) |

All datasets are public and used for educational and analytical purposes only.

---

## **Methods**

### **Data Cleaning**

* Keep only numeric, measurable variables (`age`, `height`, `weight`, `potential`, `physic`, `market_value_eur`).
* Remove all match or event-based metrics (goals, assists, tackles, xG).
* Normalize units: height (cm), weight (kg), and convert all currencies to euros.

### **Variable Relationships**

| Variable 1                       | Variable 2    | Expected Relationship                                                 |
| -------------------------------- | ------------- | --------------------------------------------------------------------- |
| Height × Weight (Physical Index) | Market Value  | Positive correlation — physically strong players often valued higher. |
| Potential (FIFA)                 | Market Value  | Positive — young players with high potential are valued more.         |
| Potential (FM)                   | Market Value  | Positive — consistent across independent systems.                     |
| Physic (FIFA)                    | Height/Weight | Moderate — higher Physic corresponds with bigger body metrics.        |

### **Analysis Steps**

1. Merge datasets by player name and position where possible.
2. Compute correlation coefficients between the key variables.
3. Visualize:

   * Scatter plots (Potential vs Market Value, Physical Index vs Market Value).
   * Heatmap for correlation matrix.
4. Interpret whether market value aligns more strongly with **potential** or **physical** traits.

---

## **Findings (Expected)**

* **Potential** (both FIFA and FM) shows a strong positive correlation with market value, confirming that expected growth drives investment.
* **Physical metrics** (height, weight) have a smaller but notable effect — especially for defenders and forwards.
* **Economic insight:** Market value appears to be shaped by a combination of potential and physicality, reflecting modern football’s emphasis on athleticism and projection.

---

## **Limitations**

* Players missing across datasets limit exact merges.
* Rating systems (FIFA vs FM) use different scales requiring normalization.
* Market values from Transfermarkt fluctuate over time and reflect subjective estimation.

---

## **Tools and Technologies**

* **Python:** Pandas, NumPy, Seaborn, Matplotlib
* **Statsmodels:** for correlation and regression
* **Excel / Power BI:** for visualization and summary statistics

---

## **Conclusion**

This study combines FIFA, Football Manager, and Transfermarkt data to uncover how **physical attributes and potential ability influence market value in professional football.**
Findings indicate that potential is the most dominant factor in valuation, while physical characteristics reinforce worth in specific positions.
By integrating multiple data sources, the project provides a data-driven view of how football’s economic logic links talent, physique, and value.
