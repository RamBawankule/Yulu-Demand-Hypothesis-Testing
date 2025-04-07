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

* **Source:** [Provide Link to Original Dataset Here if applicable]
* *(Note: The dataset file might/might not be included in the `data/` directory of this repository.)*

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

*(Summarize 3-5 major insights from your notebook, focusing on the hypothesis test results.)*
* Example: Working days show a statistically significant [increase/decrease/no difference] in the average number of cycle rentals compared to non-working days (based on t-test results).
* Example: There is a significant difference in average rental counts across different seasons (e.g., Fall highest, Spring lowest), as indicated by the ANOVA test.
* Example: Weather conditions significantly impact rental demand, with clear weather having the highest average rentals (based on ANOVA results).
* Example: There is a statistically significant association between the season and the prevailing weather conditions (based on Chi-square test).

## Recommendations

*(List 3-5 actionable recommendations based on your hypothesis test findings. Keep language clear.)*
* Example: Optimize bike availability and potentially offer targeted promotions on working days vs. weekends/holidays based on the significant difference found in rental demand.
* Example: Adjust fleet deployment and marketing campaigns seasonally, allocating more resources during peak seasons (e.g., Fall) and potentially offering incentives during lower-demand seasons (e.g., Spring).
* Example: Develop weather-contingent operational plans, such as dynamic pricing or service alerts during adverse weather (Light/Heavy Precipitation), and ensure peak availability during clear weather.
* Example: Integrate seasonal weather expectations into demand forecasting models for more accurate fleet management and resource allocation.

## Tools Used

* **Programming Language:** Python
* **Libraries:** Pandas (Data Manipulation), Matplotlib & Seaborn (Visualization), NumPy, SciPy.stats (for Hypothesis Testing: t-test, ANOVA, Chi-square)
* **Environment:** Jupyter Notebook

## License
[Apache License 2.0](LICENSE)
