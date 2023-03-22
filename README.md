# MS0003 Mini Project - World Energy Usage

The United Nations is looking to reduce carbon footprint of countries and minimize their reliance on non-renewable energy sources. In the wake of the COVID-19 pandemic, there has been a surge in usage of non-renewable energy in various countries following the relaxation of quarantine procedures.

The data science department has been tasked to identify countries that have been using non-renewable energy beyond a certain benchmark to fuel their development and determine how to regulate non-renewable energy usage through tariffs and grants to support renewable energy usage.

They have collected data on population, GDP, and various types of energy consumption from renewables to non-renewables for different countries. 

Using this data, they want to develop a model that can classify countries into developed and developing countries and then cluster them based on their renewable and non-renewable energy usage patterns. This will allow them to identify which countries are in line with their goals and enact the relevant tariffs/grants accordingly.

__**Outline of machine learning process:**__

**1st  : Data cleaning and preprocessing**

- Remove countries that no longer exist (Czechoslovakia etc.) - use list of current countries to compare and remove
- From given dataset:
    - gdp and population: find the earliest year where both data are available for ALL countries
    - electricity_demand, energy_cons_change_pct: other economic indicators that can be used to predict
- Import other datasets: Human Development Index (HDI)

**2nd : Classify into developed and developing countries (latest year is used: 2021)**

__Note : Classification of developed and developing countries cannot be limited to a single indicator and we use around 3-4 metrics as determinants__

- from dataset: GDP, population, energy consumption per capita (% change), 
- from other datasets: human development index

**3rd** : in each classification, compare their trends of non-renewable and renewable energy (then get data points based on the trends)

**4th** : cluster into different degrees of non-renewable and renewable energy (using datapoints from 2nd - in terms of boundary, need to be able to rationalise the boundary itself)

**5th** : extra stuff
- net_elec_imports_share_demand : can identify which countries more reliant on electricity imports and tax them accordingly

Clustering:
- Use an unsupervised machine learning algorithm such as K-Means, DBSCAN, or Hierarchical clustering to group the countries into clusters based on their energy usage patterns.
- Choose the number of clusters that provide the most meaningful and interpretable insights.

Classification:
- Use a supervised machine learning algorithm such as Logistic Regression, Random Forest, or Gradient Boosting to train a model to predict which countries are likely to transition into a renewable energy future.
- Use the clustered groups as labels to classify the countries into one of the groups.
- Evaluate the performance of the model using cross-validation and various metrics such as accuracy, precision, and recall.