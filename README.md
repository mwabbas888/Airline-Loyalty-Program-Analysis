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
* Passenger volumes (`PSJ Volume`)
* Airmiles redeemed (`AirMiles Redeemed`)
* Flight routes (`Route at sector level`)
* Cabin Classes (`Cabin Code (group)`)
* Pricing options (`Price Option`)
* Month of Departure Date (`Month of Departure Date`)

The datasets enabled immediate application of analytical techniques, allowing for direct investigation into performance metrics and trend identification without requiring initial data cleaning or extensive preprocessing.

---

## Key Findings & Visualizations

The analytical phase involved extensive univariate, bivariate, and multivariate analysis to systematically extract insights and identify performance drivers across both loyalty schemes.

### 1. Overall Performance & Seasonal Trends

**Monthly Airmiles Redeemed by Cabin Class - Horizon vs Equator:**
*Insight:* This time-series visualization presents the aggregate monthly Airmiles redemption volumes, disaggregated by specific cabin classes for both Horizon and Equator alliances.
* **Horizon is the Market Leader in Redemptions:** Across almost every cabin class, Horizon Alliance consistently demonstrates a significantly higher volume of Airmiles being redeemed compared to Equator Alliance. This indicates Horizon's larger, more engaged, or higher-earning loyalty member base.
* **Differentiated Cabin Class Strategies:** Horizon shows exceptional strength in its premium cabins ('Gold', 'Deluxe', 'Executive'), where the redemption volume gap with Equator is widest, suggesting effective encouragement for premium travel. Equator is more competitive in mid-to-lower tiers ('Premier', 'Silver') with more stable redemption volumes, pointing to a strategy focused on broader member engagement.
* **Clear Seasonality Drives Behavior:** Both alliances exhibit clear seasonal peaks, notably during typical summer travel periods (June-August) and year-end holidays (December). This confirms that reward travel aligns with standard consumer travel patterns, with noticeable dips in early and autumn months.
<img src="./visualizations/Monthly_Airmiles_Redeemed.jpg" alt="Monthly Airmiles Redeemed by Cabin Class - Horizon vs Equator"/>

### 2. Passenger Behaviour and Redemption Efficiency

**Airmiles Per Passenger vs. PSJ Volume (Horizon Alliance):**
*Insight:* This scatter plot specifically for Horizon Alliance reveals the relationship between the efficiency of Airmiles redemption per passenger and the overall Passenger Journey Segment (PSJ) volume. Segmented by cabin class, it helps identify which cabin/volume combinations yield higher or lower Airmiles burn per passenger within the Horizon scheme.
* **Consistent Cabin Tiers:** The plot shows distinct horizontal bands, confirming that each cabin class maintains a relatively stable range of mileage costs per passenger, indicating a consistent reward pricing structure.
<img src="./visualizations/Horizon_Alliance_Scatter.jpg" alt="Horizon Alliance - Airmiles per passenger vs PSJ volume by Cabin Class"/>

**Airmiles Per Passenger vs. PSJ Volume (Equator Alliance):**
*Insight:* Focusing on Equator Alliance, this scatter plot illustrates the relationship between Airmiles redeemed per passenger and PSJ volume for its distinct set of cabin classes. This allows for an isolated assessment of redemption efficiency and volume distribution within the Equator scheme.
* **Value Drives Volume:** A clear inverse relationship is observed: redemptions with lower Airmiles costs per passenger tend to correlate with significantly higher passenger volumes, confirming that lower prices stimulate higher demand.
<img src="./visualizations/Equator_Alliance_Scatter.jpg" alt="Equator Alliance - Airmiles per passenger vs PSJ volume by Cabin Class"/>

### 3. Route Concentration & Strategic Importance

**Route Concentration (Pareto Analysis - Horizon Alliance):**
*Insight:* A Pareto analysis for Horizon Alliance demonstrates a high concentration of Airmiles redemptions, with the **Top 5 routes accounting for approximately 50% of all Airmiles redeemed**. This highlights a significant reliance on specific premium long-haul routes, representing both a strength and a potential area of risk concentration.
* **"Vital Few" Routes:** The analysis clearly demonstrates the 80/20 principle: a small number of routes account for a very large percentage (over 70% for the top 20 shown) of all Airmiles redeemed across both alliances. These routes are strategically critical.
<img src="./visualizations/Horizon_Alliance_Pareto.jpg" alt="Horizon Alliance - Route Concentration Pareto Chart"/>

**Route Concentration (Pareto Analysis - Equator Alliance):**
*Insight:* The Pareto analysis for Equator Alliance indicates a **more distributed redemption pattern across a broader range of intra-Europe and Latin America routes** compared to Horizon. This dispersion suggests different demand dynamics compared to Horizon, although high redemptions on certain long-haul routes for Equator suggest opportunities for optimizing value given.
<img src="./visualizations/Equator_Alliance_Pareto.jpg" alt="Equator Alliance - Route Concentration Pareto Chart"/>

### 4. Temporal Demand Patterns on Key Routes

**PSJ Volume by Top 12 Horizon Routes and Month-Year (Heatmap Analysis):**
*Insight:* This detailed heatmap focuses exclusively on the **12 most popular routes by PSJ volume within Horizon Alliance**. It visually depicts monthly passenger volume distribution across these key routes, clearly identifying seasonal peaks and troughs, which is crucial for targeted capacity and pricing strategies.
* **Route-Specific Peak Seasons:** The heatmaps reveal that while overall trends show summer/winter peaks, the intensity and timing of these peaks vary significantly on a per-route basis. This indicates that some routes may have consistent year-round demand, while others are highly seasonal.
<img src="./visualizations/Horizon_Alliance_Heatmap.png" alt="Heatmap of PSJ Volume by Top 12 Horizon Routes and Month-Year"/>

**PSJ Volume by Top 12 Equator Routes and Month-Year (Heatmap Analysis):**
*Insight:* This heatmap specifically analyzes the **12 most popular routes by PSJ volume within Equator Alliance**. It provides a granular view of monthly passenger volume across these key routes, revealing specific demand patterns that differ from Horizon and informing distinct operational and marketing strategies.
<img src="./visualizations/Equator_Alliance_Heatmap.png" alt="Heatmap of PSJ Volume by Top 12 Equator Routes and Month-Year"/>

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

### Cross-Alliance Strategic Recommendations:
* **Leverage Seasonality for Demand Smoothing:** Utilize identified seasonal trends for targeted promotional campaigns (e.g., "bonus miles" or reduced mileage costs during off-peak months like February, October) to help smooth demand and optimize less popular flights. Conversely, ensure high reward seat availability during peak seasons to maximize member satisfaction.
* **Protect and Diversify "Vital Few" Routes:** The top-performing routes are critical assets. Any negative changes (e.g., increasing mileage costs) should be approached with extreme caution due to their disproportionate impact on loyalty. Consider using less popular routes for aggressive promotions to shift demand and highlight the value of the broader network.
* **Implement Dynamic Reward Pricing:** Leverage the observed inverse relationship between cost per passenger and volume. Introduce limited-time, lower-mileage redemption options for specific flights with low cash bookings to stimulate demand from the loyalty member base.

### Horizon Alliance Specific Recommendations:

1.  **Dynamic Pricing Review for Short European Routes:** Conduct a reassessment of Airmiles costs during off-peak seasons to optimize yield and incentivize demand more effectively.
2.  **Targeted Promotion of Long-Haul Upgrades:** Implement focused campaigns offering upgrade incentives on key long-haul routes to drive higher-value redemptions and enhance revenue per passenger.
3.  **Seasonal Demand Management through Flexible Pricing:** Introduce flexible Airmiles pricing models, adjusted monthly, to efficiently manage demand fluctuations and maximize scheme profitability throughout the year.

### Equator Alliance Specific Recommendations:

1.  **Upselling Strategy for Business Class:** Develop and offer targeted incentives for upgrades from complete fares to business class, capitalizing on existing demand patterns to increase average transaction value.
2.  **Strategic Airmiles Pricing for Underperforming Routes:** Trial new pricing bundles or implement reduced redemption rates for low-demand routes to stimulate activity and optimize network utilization.
3.  **Personalized Member-Type Offers:** Utilize user segmentation (e.g., frequent vs. casual fliers) to tailor Airmiles promotions, enhancing relevance and engagement for diverse customer groups.

---

## Technical Details

* **Language:** Python
* **Libraries:** Pandas for robust data manipulation, Matplotlib and Seaborn for advanced data visualization capabilities.
* **Datasets:**
    * `horizon_alliance_data.xlsx`
    * `equator_alliance_data.xlsx`
* **Analysis Notebook:** `Reward_Flights_Analysis.ipynb` (contains the complete code for data loading, preprocessing, analysis, and visualization).
* **Analytical Techniques:**
    * Univariate Analysis (e.g., temporal distribution of Airmiles redemption).
    * Bivariate Analysis (e.g., cabin class performance vs. Airmiles, route concentration using Pareto principle).
    * Multivariate Analysis (e.g., heatmaps of PSJ volume across top routes and time, Airmiles per passenger segmented by cabin class).
    * Time Series Trend Identification
    * Pareto Principle Application for Route Dominance Assessment
    * Data Aggregation and Summarization
    * Derivation of Business-Centric Insights

---
