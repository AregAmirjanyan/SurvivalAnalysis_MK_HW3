# Survival Analysis and Customer Lifetime Value (CLV) Modeling

## Overview
This project involves using AFT models to analyze survival patterns and predict customer churn. 
Customer Lifetime Value (CLV) is calculated to estimate the future value of customers.



## AFT Models
### Weibull AFT Model
The lambda_ coefficients represent the baseline hazard. Negative values indicate a decrease in hazard. lambda_ ID has a negative coefficient, suggesting that the baseline hazard decreases with ID.
The rho_ coefficient is the shape parameter of the Weibull distribution. A positive coefficient suggests increasing hazard.

### Log-Normal AFT Model
mu_ (Location Parameter): Positive coefficients indicate an increase in the location parameter, which means the hazard is higher
sigma_ (Scale Parameter): Represents the standard deviation of the log-normal distribution. A higher value suggests higher variability in survival times.

### Log-Logistic AFT Model
alpha_ (Shape Parameter): Positive coefficient implies increasing hazard over time.
beta_ (Scale Parameter): Reflects the degree of variability in survival times.

## Model Comparison
"custcat_E-service," "custcat_Plus service," and "custcat_Total service" have significant positive coefficients in all models, suggesting a higher hazard for these customer categories.
"income" has a small but positive coefficient in Weibull and log-normal models, indicating a slight increase in hazard with income.

## Findings
In the plot, the LogNormal model has the lowest AIC and BIC, and the highest log-likelihood value. Hence, the model fits better than the others to our data. That is why, we choose the LogNormal model as our AFT Fitter.

The significant features are: address, age, custcat_E-service, custcat_Plus service, custcat_Total service, internet_Yes, marital_Unmarried, voice_Yes, according to their p-values.


