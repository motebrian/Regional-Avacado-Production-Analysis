# Regional Avocado Production Outlook: Time Series Analysis for Eastern Africa

![image_alt](https://github.com/motebrian/Regional-Avacado-Production-Analysis/blob/298649e632905eaf161dda67d7f1ef1286296137/avo-1-2-scaled-768x512.jpg)

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://www.python.org/) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![LinkedIn](https://img.shields.io/badge/LinkedIn-Mote%20The%20Analyst-blue)](https://www.linkedin.com/in/your-profile/) [![X (Twitter)](https://img.shields.io/twitter/follow/MoteAnalyst?style=social)](https://x.com/MoteAnalyst)

## Project Overview
As a data analyst passionate about sustainable development in Eastern Africa (including my home country, Kenya), I analyzed historical avocado production data from the Food and Agriculture Organization (FAO) to uncover trends, forecast future output, and provide policy insights. This project demonstrates my expertise in time series analysis using Python, with applications for NGOs like the World Food Programme or Oxfam, focusing on food security and agricultural efficiency.

**Key Skills Demonstrated:**
- Data ingestion and cleaning with Pandas
- Time series smoothing (moving averages, LOWESS, Holt's exponential)
- Regression modeling (linear, polynomial)
- Decomposition analysis (yield vs. area harvested)
- Visualization with Matplotlib
- Deriving actionable insights for policy and decision-making

**Dataset:** Annual avocado production data from FAO (1996–2023), filtered for Eastern Africa. Source: [FAOSTAT](https://www.fao.org/faostat/en/#data).

**Motivation:** Avocado production is vital for Eastern Africa's economy and nutrition. With rising global demand, understanding trends can help NGOs optimize aid, promote sustainable farming, and address yield declines.

## Analysis Flow
The analysis is fully documented in the Jupyter notebook (`notebooks/Regional_Avocado_Production_Outlook.ipynb`). Here's the step-by-step flow:

1. **Data Loading and Preparation**
   - Import libraries: Pandas, NumPy, Matplotlib, Scikit-learn, Statsmodels.
   - Load FAO CSV data.
   - Filter for "Avocados" in "Eastern Africa" and "Production" element.
   - Create time series DataFrame with 'Year' as index and 'Value' as production volume.
   - Handle any missing values (none in this dataset).

2. **Exploratory Data Analysis (EDA)**
   - Plot raw annual production: Reveals upward trend with a sharp increase post-2015.
   - Compute and plot 3-year and 5-year moving averages to smooth noise and highlight long-term growth.

   ![Moving Averages Plot](https://github.com/motebrian/Regional-Avacado-Production-Analysis/blob/ceec1560fb481d982844351dca07296de7108ddc/EDA.jpg)

3. **Trend Modeling**
   - **Linear Regression:** Fit a simple linear model on time to quantify overall growth.
   - **Polynomial Regression (Degree 2):** Capture non-linear acceleration in recent years.
   - **LOWESS Smoothing:** Locally weighted scatterplot smoothing to detect subtle fluctuations (e.g., peaks 2008–2016).
   - **Holt's Exponential Smoothing:** Model with linear trend for forecasting; projects continued increase.

   ![Trend Comparison Plot](https://github.com/motebrian/Regional-Avacado-Production-Analysis/blob/a72e48baa3e579b2d9ef4a70e7b0a5e83600c339/Trend.jpg)

4. **Decomposition Analysis**
   - Merge production with area harvested data.
   - Calculate yield (production per area).
   - Plot decomposition: Production (upward), Area Harvested (stable until 2020 uptick), Yield (peak in 2010, then decline to near-constant levels).
   
   ![Decomposition Plot](https://github.com/motebrian/Regional-Avacado-Production-Analysis/blob/f42b2aaaf57989075ab22982b5a51ed523385347/Decomposition.jpg)

5. **Forecasting and Interpretation**
   - Use Holt's model to forecast 5–10 years ahead.
   - Key Finding: Production is rising due to expanded area, but yield efficiency is stagnating or declining.

## Key Findings
- **Upward Production Trend:** From ~65,000 tons in 1996 to over 1 million tons by 2023, with acceleration post-2015 (likely due to export demand and climate factors).
- **Smoothing Insights:** Moving averages confirm steady growth; LOWESS highlights minor cycles (2008–2016), possibly tied to weather or market events.
- **Decomposition Revelation:** While total output grows, yield per area has dropped sharply since 2010 (from ~14 to ~8 tons/ha), indicating inefficiencies in farming practices.
- **Forecast:** Holt's model predicts continued growth to 1.5–2 million tons by 2030, but only if area expansion continues—yield stagnation could limit this.

## Policy Interpretation and Recommendations
This analysis has direct implications for NGOs, governments, and farmers in Eastern Africa (e.g., Kenya, Tanzania, Ethiopia):

- **Sustainability Focus:** The yield decline suggests over-reliance on land expansion rather than productivity gains. NGOs should advocate for policies promoting improved irrigation, pest-resistant varieties, and soil management to boost yield without deforestation.
- **Food Security Impact:** Rising production supports nutrition and exports, but stagnant yields risk vulnerability to climate change. Recommend targeted interventions like farmer training programs (e.g., via USAID or FAO partnerships) to reverse the 2010–present drop.
- **Economic Opportunities:** With global avocado demand (e.g., from EU/US markets), policies should incentivize efficient farming. For instance, subsidies for precision agriculture could increase yield by 20–30%, based on similar crops in the region.
- **NGO Applications:** Use these forecasts for resource allocation—e.g., prepositioning aid in low-yield years or lobbying for sustainable land use policies to prevent environmental degradation.

These recommendations are grounded in the data: Addressing yield gaps could sustain growth amid population pressures and climate risks.

## How to Run This Project
1. Clone the repo: `git clone https://github.com/MoteAnalyst/regional-avocado-production-analysis.git`
2. Install dependencies: `pip install -r requirements.txt`
3. Open the notebook: `jupyter notebook notebooks/Regional_Avocado_Production_Outlook.ipynb`
4. Run all cells to reproduce plots and analysis.

## About Me
I'm Mote The Analyst (@MoteAnalyst on X), a data scientist from Nairobi, Kenya, specializing in producing predictive models. This project is part of my portfolio showcasing data-driven solutions for African challenges. Connect with me on [LinkedIn](https://www.linkedin.com/in/your-profile/) or [X](https://x.com/MoteAnalyst).

Feedback welcome—star the repo if you find it useful!
