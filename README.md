# Bachelor_thesis_Italy_poverty

This project was carried out as the final one of my Bachelor's degree (Bachelor of Science) in Statistics for economics and business at the University of Padova in March 2023.

Personal information:
| NAME and SURNAME | PERSONAL EMAIL |
| --- | --- |
| Sofia Noemi Crobeddu | sofianoemi.crobeddu@gmail.com | 

## PURPOSE

This project aims to analyse possible statistical methods to measure poverty in Italy, through the data of the Statistical Survey carried out by the Bank of Italy in 2020. In particular, three datasets are used among those available ones in the Bank of Italy's data archive, focusing on demographic, income, expenditure and consumption variables. A comparison is also made between this baseline survey and the one carried out by ISTAT on the consumption of Italian households, in the reference year, in order to have a more in-depth study of the subject. Poverty is treated from a unidimensional and multidimensional perspective. For the multivariate analysis it is used the Factor Analysis method with an application of the regression model, in order to find non-observed dimensions of the topic. The analysis is done with the software R.

## REPOSITORIES

The macro-repositories are:
- **data**: it contains the csv files with the original datasets. The files and repositories with data inside, are the following ones:
  - `colombia_emissions_total_CO2.csv`: contains Colombia's total emissions of CO2. These data were needed to calculate the Greenhouse Gas Emission, since they represent the numerator of this proxy sub-indicator. From FAOstat.
  - `colombia_fertilizer_use_intensity.csv`: contains Colombia's fertilizer use intensity. From FAOstat.
  - `colombia_pesticides_use_intensity.csv`: contains Colombia's pesticides use intensity. From FAOstat.
  - `colombia_value_prod_agriculture.csv`: contains Colombia's value of agricultural production. These data were needed to calculate the Greenhouse Gas Emission, since they represent the denominator of this proxy sub-indicator. From FAOstat.
  - `colombia_water_stress.csv`: contains Colombia's water stress. From FAOstat.
  - There are also two other internal repositories:
     - **water stress - World Bank**: it contains the dataset `water stress and variables - WB.csv` regarding data for water stress level for Colombia, from World Bank databases. Comapred to the dataset from FAOstat, this one contains more specific information such as "Annual freshwater withdrawals, agriculture (% of total freshwater withdrawal)", "Annual freshwater withdrawals, domestic (% of total freshwater withdrawal)", "Annual freshwater withdrawals, industry (% of total freshwater withdrawal)", "Annual freshwater withdrawals, total (billion cubic meters)", "Level of water stress: freshwater withdrawal as a proportion of available freshwater resources", "Renewable internal freshwater resources, total (billion cubic meters)", "Average precipitation in depth (mm per year)", "Population, total", "GDP per capita (constant 2015 US$)", "Population density (people per sq. km of land area)".
     - **ML_part**: it contains the dataset `data_cleaned.csv` that comes from the previous one mentioned before (`water stress and variables - WB.csv`), after renaiming columns, converting in number the observations and reindexing.
- **script**: it contains the codes for the analysis among these files:
  - `final project.R`: it contains all the analysis for the first part regarding the proxy sub-indicators, the status and trend assessment for the environmental dimension of agricultural sustainability. Regarding the second part of the project, it contains also a preliminary analysis on avocado production and its correlation with water stress, and a tentative prediction with a JAGS model (Bayesian prediction). This model didn't give good results.
  - `final project Notebook.ipynb`: it contains the second part of the analysis. Two methods to make predicion were applied, and in particular a Neural Network implemented though the deep learning library Keras from Tensorflow, and the second one based on Extrapolation approach, that is the process of projection of data beyond the years observed. The first one didn't give good results, while the second one better.
  - `model_jags.txt`: text file of the JAGS model applied to data.
