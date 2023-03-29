# MS0003 Mini Project - World Energy Usage

__Feedback__
- Animation for choropleth for trend across the year to show what we have done so far
    - For story-telling -> Magnitude of the problem (which countries have more emissions)
    - Take the role of an advisor

- From renewable enrgy trend - SA leading the trend for renewables
    - Policies that make them do it right
    - Something that UN can implement for other nation

- Shared Socioeconomic Pathway
    - ARIMA model - forecast for 50 (continent data - explain why we did not use country data)
    - ARIMA - time-forecast, SARIMA - seasonal-forecast
    - Most likely to hit or not hit the target?
    - Drop 2020 cause black swan
    - Show auto-regression plot

- What can we do from the lessons learnt above^?
    - Such as adopt policies from

__New Flow__

1. Data Cleaning
    - Remove columns - don't use specific energy types (coal, gas, nuclear)
    - Use continent data for time-series forecasting
        - countries always change (e.g. Venezuela)
        - use renewable_energy_per_capita / fossiL_energy_per_capita

2. EDA
    - show renewable enrgy trend across CONTINENTS (can show fossil_cons_change_pct AND greenhouse gas emissions)
        - show via choropleth
    - explain that SA is leading the renewable energy
        - trend for south american countries (renewable share)

3. ML ********
    - ARIMA model for continent renewable energy (if got time, ARIMA for fossil fuel)
    - auto-regression plot

4. Conclusion
    - whether we hit 0 fossil fuel by 2050
    - what countries' policy we can learn from
        - smoking


__Old Research Question__

The United Nations is looking to reduce carbon footprint of countries and minimize their reliance on non-renewable energy sources. In recent times, there has been a surge in usage of non-renewable energy in various countries following the relaxation of quarantine procedures.

The data science department has been tasked to identify countries that have been using non-renewable energy beyond a certain benchmark to fuel their development and determine how to regulate non-renewable energy usage through tariffs and grants to support renewable energy usage.

They have collected data on population, GDP, and various types of energy consumption from renewables to non-renewables for different countries. 

Using this data, they want to develop a model that can classify countries into developed and developing countries and then cluster them based on their renewable and non-renewable energy usage patterns. This will allow them to identify which countries are in line with their goals and enact the relevant tariffs/grants accordingly.


__Stance of the United Nations__

United Nations (UN) has been actively working towards reducing non-renewable energy and fossil fuel usage, as part of its efforts to mitigate climate change and promote sustainable development. The UN has set various targets and initiatives to promote the use of renewable energy sources and reduce dependence on fossil fuels.

For example, the UN's 2030 Agenda for Sustainable Development includes a goal to ensure access to affordable, reliable, sustainable, and modern energy for all (Goal 7). This goal includes targets to increase the share of renewable energy in the global energy mix and improve energy efficiency.

Additionally, the UN Framework Convention on Climate Change (UNFCCC) is an international treaty aimed at mitigating greenhouse gas emissions and addressing climate change. The UNFCCC includes various mechanisms, such as the Kyoto Protocol and the Paris Agreement, which aim to reduce greenhouse gas emissions from various sectors, including energy production.

__Machine Learning Approach__

Clustering countries into developing and developed countries first is a way to group countries based on their socio-economic indicators and level of development. This can be a useful step before clustering countries based on their fossil fuel to renewable energy usage because countries that are at different stages of development may have different priorities, policies, and approaches to energy use.

For example, developed countries may have already made significant progress in transitioning to renewable energy sources, while developing countries may still be heavily reliant on fossil fuels due to limited resources, technology, or infrastructure. By grouping countries into developing and developed categories, we can better understand the specific challenges and opportunities that each group faces and tailor our approach to addressing their energy needs accordingly.

The criteria used to classify countries as developing or developed may vary depending on the specific context and goals of the analysis. Common indicators used for this purpose include GDP per capita, Human Development Index (HDI), life expectancy, education levels, and other socio-economic metrics. These criteria can be used to identify countries that have similar levels of development and face similar challenges.


__Problems encountered__
Data Cleaning

- Reasonable to take percentage-base values rather than absolute values (terawatt-hours etc.)?

- Extrapolate or don't use that column for comparison? What's a reasonable threshold?

- Some countries don't have all the data in some years or missing data - e.g. Micronesia data stops at 2019 - remove them?

Binary Clustering (developed or developing countries) - identify relevant year, add HDI as metrics

- Different years have different missing data - hard to select a specific year to do our clustering so we took 2018 as a reference year but it still has some missing data that we are not sure whether to extrapolate or drop them

- Is it better to just take pre-classified data for developed or developing countries from readily available datasets online?

- Even external data has missing data for some countries so we used older years (i.e. 2018)
    - In addition, how much should we utilise external data before it seems like we are not even using original data
        - Idea was for binary clustering, create from external dataset
        - From that, in each cluster, use original dataset (but will encounter the problem of missing data again)

Clustering - cluster based on ____ to see how to tackle each cluster (taxing them or just giving them grants etc.)