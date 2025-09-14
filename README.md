Project Details

Project title: Predictive Model Based Power Price Tagging Under Deregulated Environment
Topic: Time Series Forecasting and Optimization in Energy Markets

Final Project: Predictive Model Based Power Price Tagging
Project Overview

Objective: Develop a predictive framework that combines time series forecasting with Genetic Algorithm optimization to forecast electricity market prices (Market Clearing Price – MCP) and minimize generation cost through Economic Load Dispatch (ELD).

This project focuses on forecasting electricity prices in deregulated power markets, where prices are determined by supply-demand dynamics and change rapidly. Using ARIMA, SARIMA, and LSTM models, the project predicts MCP values with high accuracy. Alongside, a Genetic Algorithm (GA) is implemented to optimize generator allocation, ensuring minimum production cost. By integrating forecasts and optimization results, the project proposes a dynamic price tagging mechanism that reflects both market trends and economic efficiency.

Key Steps in the Project
Dataset and Preprocessing

The dataset consisted of historical electricity market prices and demand information. Preprocessing steps included:

Cleaning missing or inconsistent records.

Normalizing input values for model stability.

Splitting into training and testing sets for fair evaluation.

This ensured high-quality data for both time series forecasting and ELD optimization.

Exploratory Data Analysis (EDA)

EDA was conducted to understand the dataset’s characteristics:

Trend Analysis: Electricity prices exhibited clear temporal trends with peaks and troughs.

Seasonality Detection: Daily and weekly seasonal cycles were observed, making SARIMA suitable.

Volatility Analysis: Sudden spikes in MCP highlighted the need for robust models like LSTM.

Key Visualizations:

Line plots of historical MCP values.

Seasonal decomposition plots.

Box plots showing daily/weekly price variation.

Primary/Machine Learning & Optimization Analysis
Time Series Forecasting Models

Three forecasting techniques were chosen:

ARIMA (AutoRegressive Integrated Moving Average):

Effective for capturing linear temporal dependencies.

Provided a strong statistical baseline.

SARIMA (Seasonal ARIMA):

Extended ARIMA to model daily/weekly cycles.

Captured seasonal effects better than ARIMA.

LSTM (Long Short-Term Memory):

Deep learning model designed for sequential data.

Captured nonlinear dynamics and long-term dependencies in electricity prices.

Why these techniques?

ARIMA provided interpretability.

SARIMA addressed seasonality.

LSTM outperformed statistical methods in accuracy by learning complex patterns.

Example Forecast Output (Next 6 Hours):

[49.8, 50.1, 50.4, 51.0, 50.7, 50.9]

Economic Load Dispatch with Genetic Algorithm

The ELD problem involves allocating power among multiple generators such that total cost is minimized while meeting demand.

Genetic Algorithm Approach:

Chromosome: Represents power allocation to generators.

Fitness Function: Inverse of total generation cost.

Operators: Selection, crossover, mutation applied to evolve optimal allocation.

Example GA Output:

Optimal Allocation: {GenA: 500 MW, GenB: 400 MW, GenC: 300 MW}
Minimum Cost: 25,630.50


Visualization: GA convergence plot showing cost reduction over generations.

Integration – Price Tagging Framework

The final framework integrates forecasts and GA optimization:

Forecast MCP using ARIMA, SARIMA, or LSTM.

Run GA to minimize generation cost for given demand.

Combine results into dynamic electricity price tags.

Sample Tagged Prices (Next 6 Hours):

[52.1, 52.4, 52.7, 53.0, 52.8, 53.2]

Results

ARIMA: R² ≈ 0.77 – solid baseline.

SARIMA: Improved accuracy by modeling seasonality.

LSTM: Best performing model with R² ≈ 0.88, RMSE ≈ 2.9.

Genetic Algorithm: Reduced generation cost significantly versus naive allocation.

Visualizations Included:

Forecast comparison plots (ARIMA vs SARIMA vs LSTM).

GA convergence curve.

Price tagging trend line.

Insights and Conclusions

Forecasting Insight: LSTM captured complex non-linear dependencies better than statistical models.

Optimization Insight: GA provided cost-effective generator allocations while satisfying demand constraints.

Integrated Framework: By merging forecasts with optimized dispatch, the project created an adaptive pricing mechanism, enhancing competitiveness in deregulated power markets.

Key Takeaways:

Statistical and deep learning models complement each other in time series forecasting.

Genetic Algorithms are effective in solving nonlinear optimization like ELD.

Dynamic price tagging ensures prices align with both market dynamics and economic efficiency.

Project Structure
├── data/                 # Historical MCP and demand datasets
├── notebooks/            # ARIMA, SARIMA, and LSTM experiments
├── models/               # Trained models
├── ga_code/              # Genetic Algorithm implementation
├── results/              # Forecasts, GA plots, tagged prices
└── README.md             # Project documentation

Final Thoughts

This project bridges time series forecasting and optimization to address real challenges in deregulated electricity markets. The hybrid framework demonstrates how predictive analytics and evolutionary algorithms can enhance decision-making, improve bidding strategies, and optimize operational costs.
