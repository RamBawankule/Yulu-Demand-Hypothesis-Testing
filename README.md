# Yulu Bike Demand Analysis: Hypothesis Testing

![image](https://github.com/user-attachments/assets/3c97ba2d-b868-4be7-9b0b-776f90233abe)

## Project Overview

This project analyzes data from Yulu, India's leading micro-mobility service provider, to understand the factors influencing the demand for their shared electric cycles. Facing recent revenue dips, Yulu aims to identify significant variables predicting demand using statistical hypothesis testing (t-tests, ANOVA, Chi-square), enabling data-driven decisions to improve service and profitability.

## Business Problem

Yulu needs to understand which factors significantly affect the rental demand ('count') for their electric cycles. Key questions addressed through hypothesis testing include:
* Does the type of day (working day vs. non-working day) impact the number of cycles rented?
* Is the rental demand significantly different across various seasons (spring, summer, fall, winter)?
* Is the rental demand significantly different across various weather conditions?
* Is there a dependency between weather conditions and the season?
* Which factors are most crucial for predicting demand?

## Dataset

The dataset (`yulu_data.csv`) contains rental information along with associated factors:

* **datetime:** datetime of the rental
* **season:** 1:spring, 2:summer, 3:fall, 4:winter
* **holiday:** 1 if holiday, 0 otherwise
* **workingday:** 1 if neither weekend nor holiday, 0 otherwise
* **weather:** 1:Clear/Partly Cloudy, 2:Mist/Cloudy, 3:Light Precip., 4:Heavy Precip./Fog
* **temp:** Temperature in Celsius
* **atemp:** Feeling temperature in Celsius
* **humidity:** Relative humidity
* **windspeed:** Wind speed
* **casual:** Count of non-registered users rentals
* **registered:** Count of registered users rentals
* **count:** Total rentals (casual + registered) - **Dependent Variable**

## Repository Structure

```text
Yulu-Demand-Hypothesis-Testing/
├── data/
│   └── yulu_data.csv  
├── notebooks/
│   └── yulu_hypothesis_testing.ipynb   
├── reports/                      
│   └── yulu_analysis_report.pdf
├── .gitignore
├── LICENSE 
└── README.md
```
## Key Findings & Insights

* **Working Day Impact:** There is a statistically significant difference in the number of bikes rented between working days and non-working days, indicating distinct usage patterns.
* **Seasonal & Weather Influence:** Both season and weather conditions significantly affect the average number of rentals, with specific seasons (e.g., Fall) and weather types (e.g., Clear) showing higher demand (proven via ANOVA).
* **Season-Weather Link:** A statistically significant association exists between the season and the type of weather experienced, confirming their interdependence.
* **Predictive Factors:** Working day status, season, and weather are statistically significant factors influencing Yulu bike rental demand.

## Recommendations

1.  **Day-Type Strategy:** Optimize bike distribution and consider distinct promotional offers for working days versus weekends/holidays to align with differing demand levels.
2.  **Seasonal Fleet Management:** Adjust fleet size and deployment seasonally, increasing availability during peak seasons (like Fall) and potentially offering incentives during lower-demand seasons (like Spring).
3.  **Weather-Responsive Operations:** Implement weather-contingent plans, such as dynamic pricing adjustments during poor weather or ensuring maximum availability during favorable conditions; integrate weather forecasts into short-term planning.
4.  **Integrated Demand Forecasting:** Incorporate the statistically significant factors (season, weather, working day) and their interactions into demand forecasting models for improved accuracy in inventory and resource management.
   
## Tools Used

* **Programming Language:** Python
* **Libraries:** Pandas (Data Manipulation), Matplotlib & Seaborn (Visualization), NumPy, SciPy.stats (for Hypothesis Testing: t-test, ANOVA, Chi-square)
* **Environment:** Jupyter Notebook

## License
[Apache License 2.0](LICENSE)
