# MS0003 Mini Project - World Energy Usage

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
- Not sure whether to extrapolate or don't use that column for comparison

- Some countries don't have all the data in some years - e.g. Micronesia data stops at 2019

- Some countries like Iceland have missing data in 2021 which I dropped, is it reasonable to do so?


Binary Clustering (developed or developing countries) - identify relevant year, add HDI as metrics

- Different years have different missing data - hard to select a specific year to do our clustering so we took 2021 as a reference year but it still contains some data that we are not sure whether to extrapolate or drop them

- Is it better to just take the clustering of developed or developing countries from readily available datasets online?

- Even external data has missing data for some countries so we used older years (i.e. 2018)



Clustering - cluster based on ____ to see how to tackle each cluster (taxing them or just giving them grants etc.)