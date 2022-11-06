# Seoul-Bike-Sharing-Demand-Prediction
Seoul Bike Sharing Demand Prediction Capstone Project Linear Regression
****
Business Problem: 
Data Science Process :Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required for the stable supply of rental bikes.

***
Questions to consider:
* How do we predict the demand of the bikes at a given point of time?
* What are the factors the predict the demand of the rental bikes?
* Why are these questions important from a business perspective? 

***
**Business Understanding** : Seoul Public Bike is an unmanned rental system that can be conveniently used anywhere, anytime by anyone. This bike sharing system allows people to borrow a bike from a “dock” which then can be returned to any other dock in the city.

The system was designed to resolve issues of traffic congestion, air pollution, and high oil prices in Seoul, and to build a healthier society while enhancing the quality of life for Seoul citizens. Hence it is important to predict the demand of the bikes to ensure these are readily available to the public.

The council is unable to forecast the demand of these bikes required in the city. There is a need for a model to predict the demand of these shared bikes. The business needs this model to build a strategy to meet the demand levels, or else if not met, people may not prefer to use this mode of transport. Our project aims at predicting the demand of the rental bikes for Seoul Council.

*****

## Data Understanding

We used the data from UCI ML site. This dataset contain 8760 rows and 14 columns. 
This dataset represents number of bikes rented from Dec’17- Nov’18 for each hour. (365 days)
This contain 8760 rows and 14 columns.
Three categorical features ‘Seasons’, ‘Holiday’, & ‘Functioning Day’.
One ‘Date’ variable
Numerical type variables such as temperature, humidity, wind,  visibility, dew point temp, solar radiation, rainfall, snowfall which tells us the environmental conditions for that particular hour of the day.

*****
## Methods

Data Science Process:
We used CRISP-DM process for our project:
Business Understanding
Data Understanding
Data Prepration
Modelling the data
Interpreting the results and conclusion

***

## Results

We observed the relationship between the seasons and the rental bike count. As expected, the Winter season observed the lowest count while there were the highest numbers of bikes rented during the Summer season. 

Whereas Autumn was the second highest busiest season. 
<img width="1065" alt="image" src="https://user-images.githubusercontent.com/95839987/200171632-1d263b2e-f518-427d-8d3b-312d1560f402.png">
****
Relationship between Holidays and Rental Bike Count
It was interesting to see a low demand for the bikes on the days when it’s a Holiday in Seoul. We see a drop in the overall count of the bikes rented out on the holidays as compared to non holidays. 

The per hour average count of rented bikes on holiday days is 496 while on non holiday days is 675 which is 26% higher.

<img width="1078" alt="image" src="https://user-images.githubusercontent.com/95839987/200171660-a61e9446-b7e8-4394-868b-38947899e454.png">
*****
Holidays per hour Rental Bike Count chart
We see from the below chart
During working days the demand is high between 7am -9am. While in the afternoon we see on an average more than 1000 bikes are rented out between 4pm - 10pm. 
On the holidays, even though the overall demand is fairly low, between 2pm-8pm the maximum bikes were rented out.
<img width="1920" alt="image" src="https://user-images.githubusercontent.com/95839987/200171680-a4a5c788-59ce-482e-ac6a-21b788b38085.png">

***
Linear Regression Model:
<img width="825" alt="image" src="https://user-images.githubusercontent.com/95839987/200171693-06f46898-175d-4c16-adc4-59adf401e9b5.png">

Parameters	Results
R^2	0.665
Adj R^2	0.664
Train MSE	0.019
Test MSE	0.018
CV Mean	0.020<img width="940" alt="image" src="https://user-images.githubusercontent.com/95839987/200171701-e1ad3abe-516a-41e9-a900-b182b7600042.png">

***
## Conclusions

The most important feature of the model is the temperature for our Linear model. The demand is high during the hotter days.
Seasons and months have a strong impact on the demand for the bikes. Summer and Autumn months have higher demand. Winter is the month with the lowest demand for the bikes.
Time of the day is also important factor to consider while planning. The demand is higher during certain times of the day  during different seasons. 7am-9am and 3pm-8pm is the busiest time. 
Rainy days have a negative impact on rental bikes as we could have imagined. People dont prefer to use bikes when it’s pouring. 
Non holiday days are busier for rental bikes as compared to holidays.
***

## For More Information

Please review our full analysis in [our Jupyter Notebook](./dsc-phase1-project-template.ipynb) or our [presentation](./DS_Project_Presentation.pdf).

For any additional questions, please contact **name & email, name & email**

## Repository Structure

Describe the structure of your repository and its contents, for example:

```
├── README.md                           <- The top-level README for reviewers of this project
├── Seoul Bike Rental - Capstone Project.ipynb   <- Narrative documentation of analysis in Jupyter notebook
├── Seoul Bike Sharing Demand Prediction Project presentation.pdf         <- PDF version of project presentation
├── data                                <- Both sourced externally and generated from code
└── images                              <- Both sourced externally and generated from code
```

