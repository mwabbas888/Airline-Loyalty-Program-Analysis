# Airline Loyalty Program: Reward Flights Performance Analysis

This repository details a data-driven analysis performed as part of a pricing executive job interview exercise. The project involved a comprehensive examination of Reward Flights data from two distinct loyalty schemes, **Horizon Alliance (BAC)** and **Equator Alliance (CIB Plus)**. The objective was to uncover critical performance insights, identify key trends, evaluate scheme effectiveness, and formulate actionable strategic recommendations.

---

## Business Objective & Project Scope

The primary objective was to demonstrate robust analytical reasoning and the ability to extract key business insights from complex datasets. The project required:
* In-depth analysis of provided Reward Flights data, encompassing metrics such as passenger volumes, Airmiles redeemed, routes, cabin classes, and pricing options.
* Identification and explanation of prominent trends, assessment of high-performing and underperforming dimensions.
* Formulation of precise, data-backed recommendations to guide strategic decision-making within the loyalty programs.

---

## Data Overview & Preparation

The analysis was conducted using two pre-structured datasets: `horizon_alliance_data.xlsx` and `equator_alliance_data.xlsx`. These datasets were provided in a ready-to-analyze format, containing historical Reward Flights data with key performance indicators over a monthly time series from January 2023 to December 2024.

**Key Data Attributes:**
* Passenger volumes
* Airmiles redeemed
* Flight routes
* Cabin Classes (Deluxe, Gold, Premier, Bronze, Executive, Pearl, Silver)
* Pricing options

The datasets enabled immediate application of analytical techniques, allowing for direct investigation into performance metrics and trend identification without requiring initial data cleaning or extensive preprocessing.

---

## Key Findings & Visualizations

The analytical phase involved extensive univariate, bivariate, and multivariate analysis to systematically extract insights and identify performance drivers across both loyalty schemes.

### Overall Redemption Volume and Cabin Class Performance

**Monthly Airmiles Redeemed by Cabin Class:**
*Insight:* This time-series visualization presents the aggregate monthly Airmiles redemption volumes, disaggregated by specific cabin classes for both Horizon and Equator alliances. It distinctly highlights the scale of Airmiles utilization and reveals monthly patterns, as well as the relative contribution of each cabin class to total redemptions over the two-year period.
<img src="./visualizations/Monthly Airmiles Redeemed by Cabin Class - Horizon vs Equator.jpg" alt="Monthly Airmiles Redeemed by Cabin Class - Horizon vs Equator"/>

**Airmiles Per Passenger vs. PSJ Volume by Cabin Class:**
*Insight:* This scatter plot provides a multivariate view of redemption efficiency, correlating Airmiles redeemed per passenger with Passenger Journey Segment (PSJ) volume, differentiated by cabin class. This analysis is crucial for understanding the economic efficiency of redemptions across different service tiers.
<img src="./visualizations/Airmiles per passenger vs PSJ volume.jpg" alt="Airmiles per passenger vs PSJ volume by Cabin Class"/>

### Horizon Alliance Performance Analysis

**Route Concentration (Pareto Analysis):**
*Insight:* A Pareto analysis reveals that for Horizon Alliance, a highly concentrated set of **Top 5 routes accounts for approximately 50% of all Airmiles redemptions**. This indicates a strong reliance on specific premium long-haul routes, a critical insight for risk assessment and strategic planning.
<img src="./visualizations/Horizon Alliance - Route Concentration.jpg" alt="Horizon Alliance - Route Concentration Pareto Chart"/>

**PSJ Volume by Route and Month-Year (Heatmap Analysis):**
*Insight:* This heatmap provides a detailed multivariate analysis of PSJ volume, showcasing month-by-month and route-by-route performance for Horizon Alliance. It clearly identifies periods of peak demand and seasonal variations, which are essential for capacity and pricing management.
<img src="./visualizations/Heatmap of PSJ Volume by Route and Month-Year (Horizon).png" alt="Heatmap of PSJ Volume by Route and Month-Year (Horizon)"/>

### Equator Alliance Performance Analysis

**Route Concentration (Pareto Analysis):**
*Insight:* For Equator Alliance, the Pareto analysis demonstrates a **more distributed redemption pattern across a wider range of intra-Europe and Latin America routes**. This dispersion suggests different demand dynamics compared to Horizon, although high redemptions on certain long-haul routes for Equator indicate a potential area for value optimization.
<img src="./visualizations/Equator Alliance - Route Concentration.jpg" alt="Equator Alliance - Route Concentration Pareto Chart"/>

**PSJ Volume by Route and Month-Year (Heatmap Analysis):**
*Insight:* This heatmap, a multivariate analysis for Equator Alliance, identifies specific monthly and route-based volume trends. The data suggests less pronounced seasonal variation compared to Horizon, informing distinct operational and marketing strategies.
<img src="./visualizations/Heatmap of PSJ Volume by Route and Month-Year (Equator).png" alt="Heatmap of PSJ Volume by Route and Month-Year (Equator)"/>

### Consolidated Key Takeaways & Recommendations

The overarching insights and strategic recommendations are summarized as follows:

<img src="./visualizations/Key Takeaways, Recommendations & Next Steps.jpg" alt="Key Takeaways, Recommendations & Next Steps Summary"/>

**Horizon Key Takeaways:**
* Airmiles redemptions are predominantly in the **Gold cabin**, particularly on major long-haul routes.
* A limited number of routes (e.g., JFK, Dubai) **dominate redemption volume**.
* Pronounced **seasonal patterns** are observed, with peak performance during summer months.

**Equator Key Takeaways:**
* Primary redemptions are in **Executive and Premier cabins**.
* **Deluxe cabin utilization is low**, with exceptions on long-haul routes.
* Exhibits **less significant seasonal variation** compared to Horizon.

---

## Actionable Recommendations

Based on the quantitative analysis, the following strategic recommendations are proposed:

### Horizon Alliance Recommendations:

1.  **Dynamic Pricing Review for Short European Routes:** Conduct a reassessment of Airmiles costs during off-peak seasons to optimize yield and incentivize demand more effectively.
2.  **Targeted Promotion of Long-Haul Upgrades:** Implement focused campaigns offering upgrade incentives on key long-haul routes to drive higher-value redemptions and enhance revenue per passenger.
3.  **Seasonal Demand Management through Flexible Pricing:** Introduce flexible Airmiles pricing models, adjusted monthly, to efficiently manage demand fluctuations and maximize scheme profitability throughout the year.

### Equator Alliance Recommendations:

1.  **Upselling Strategy for Business Class:** Develop and offer targeted incentives for upgrades from complete fares to business class, capitalizing on existing demand patterns to increase average transaction value.
2.  **Strategic Airmiles Pricing for Underperforming Routes:** Trial new pricing bundles or implement reduced redemption rates for low-demand routes to stimulate activity and optimize network utilization.
3.  **Personalized Member-Type Offers:** Leverage member segmentation (e.g., frequent vs. casual fliers) to tailor Airmiles promotions, enhancing relevance and engagement for diverse customer groups.

---

## Technical Details

* **Language:** Python
* **Libraries:** Utilized for data manipulation, statistical analysis, and advanced data visualization. (Specific libraries like Pandas, NumPy, Matplotlib, and Seaborn were used in the analysis.)
* **Datasets:**
    * `horizon_alliance_data.xlsx`
    * `equator_alliance_data.xlsx`
* **Analysis Notebook:** `Reward_Flights_Analysis.ipynb` (contains the complete code for data loading, analysis, and visualization).
* **Analytical Techniques:**
    * Univariate Analysis (e.g., distribution of Airmiles redemption over time).
    * Bivariate Analysis (e.g., cabin class performance vs. Airmiles, route concentration).
    * Multivariate Analysis (e.g., heatmaps of PSJ volume across routes and time, Airmiles per passenger segmented by cabin class).
    * Time Series Trend Identification
    * Pareto Principle Application for Route Dominance Assessment
    * Data Aggregation and Summarization
    * Derivation of Business-Centric Insights

---
