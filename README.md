# MS0003 Mini Project - World Energy Usage

__Approach__

1. Filter countries based on continents - look at a broad overview rather than specific countries
2. Filter columns based on: null values, relevancy to renewables_share_energy
3. Use the columns generated to plot ExponentialSmoothing and ARIMA model.
4. See if the net zero by 2050 can be achieved

__Extra__
- Need to improve column selection using RandomForest or GradientBoosting to find the more important features + include more columns
- ARIMA - backtesting on previous dataset, would rather use simplier model if it does not result in 
- make sure data is normalised
- show linear regression as a baseline
- can explore risk-reward ratios in stock markets   

------------------------------------------------------------------------------------------------------------

__Feedback__
- Animation for choropleth for trend across the year to show what we have done so far
    - For story-telling -> Magnitude of the problem (which countries have more emissions)
    - Take the role of an advisor

- From renewable enrgy trend - SA leading the trend for renewables
    - Policies that make them do it right
    - Something that UN can implement for other nation

- Shared Socioeconomic Pathway (scenarios of projected socioeconomic global changes up to 2100)
    - ARIMA model - forecast for 2050 (continent data - explain why we did not use country data)
    - ARIMA - time-forecast, SARIMA - seasonal-forecast
    - Most likely to hit or not hit the target?
    - Drop 2020 cause black swan
    - Show auto-regression plot

- What can we do from the lessons learnt above^?
    - Such as adopt policies from South America

__New Flow__

1. Data Cleaning
    - Remove absolute values for columns
    - Use continent data for time-series forecasting
        - countries always change (e.g. Venezuela)
    **- Compare correlation using Granger causality test**

2. EDA
    - show renewable enrgy trend across CONTINENTS (can show fossil_cons_change_pct AND greenhouse gas emissions)
        - show via choropleth
    - explain that SA is leading the renewable energy
        - trend for south american countries (renewable share)

3. **ML**
    - we use renewable energy share as the main variable  - focus on renewables energy usage at end of 2050
    1. Exponential smoothing
    2. SARIMA model

4. Conclusion
    - whether we hit 0 fossil fuel by 2050
    - what countries' policy we can learn from
        - smoking

__Stance of the United Nations__

United Nations (UN) has been actively working towards reducing non-renewable energy and fossil fuel usage, as part of its efforts to mitigate climate change and promote sustainable development. The UN has set various targets and initiatives to promote the use of renewable energy sources and reduce dependence on fossil fuels.

For example, the UN's 2030 Agenda for Sustainable Development includes a goal to ensure access to affordable, reliable, sustainable, and modern energy for all (Goal 7). This goal includes targets to increase the share of renewable energy in the global energy mix and improve energy efficiency.

Additionally, the UN Framework Convention on Climate Change (UNFCCC) is an international treaty aimed at mitigating greenhouse gas emissions and addressing climate change. The UNFCCC includes various mechanisms, such as the Kyoto Protocol and the Paris Agreement, which aim to reduce greenhouse gas emissions from various sectors, including energy production.