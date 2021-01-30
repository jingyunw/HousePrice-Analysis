# King County House Price Analysis
Author: [JingYun (Jonna) Wang](/jingyunwang24@gmail.com)
<img src="images/house sale.png">

##  Overview
This project uses exploratory data analysis and linear regression modeling to predict the house sale price in King County, Washington. The data contains various information on houses sold between May 2014 and May 2015. Homebuyers can use my model to predict the house price by providing certain parameter values.

##  Business Problem
Working for a real estate agency, my job is to create a multiple linear regression model for homebuyers to predict the house price and provide recommendations for them to determine the purchasing month, location preference based on budget, understand features used for modeling, and the top features have great impact on house price.
***
### Question to consider:
<b>Q1</b>. What is the best month to purchase a house?<br>
<b>Q2</b>. Which region (on real map) in King County should homebuyers look first based on their budget?<br>
<b>Q3</b>. What features help predict house price?<br>
<b>Q4</b>. What are the top features that have stronger relationship with house price?

## Data
The dataset acquired from [GitHub](https://github.com/learn-co-curriculum/dsc-phase-2-project/tree/main/data) contains house sale price in King County, Washington. It combines various house information including `price` (target variable), sale date, building year, area, room, quality, surroundings, city, and location coordinates. Each house has a unique identifier.

## Methods
This project use multiple linear regression modeling to predict house price and train test split to evaluate machine learning performance.

## Results
<b>Q1</b>. What is the best month to purchase a house?<br>
- Feburary has the lowest avgerage house sale price (guess hard to sell during cold winter?)
- April has the highest average house sale price (guess families need to move before school starts?)
<img src="images/price vs month.png">

<b>Q2</b>. Which region (on real map) in King County should homebuyers looking for based on their budget?<br>
| Group  | Range |
| :---: | :---: |
| A  | > $750,000  |
| B  | $600,000 ~ $750,000  |
| C  | $450,000 ~ $600,000  |
| D  | $300,000 ~ $450,000  |
| E  | < $300,000  |

- Higher price houses (Group A and B) are more likely to be found in the north region
- Middle price houses (Group C) are more scattered which spread widely in King County
- Lower price houses (Group D and E) are more likely to be found in the south region
<img src="images/Price Map.png">

<b>Q3</b>. What features help predict house price?<br>
- area of living space (sqft_living)
- area of lot space (sqft_lot)
- room ratio (rm_ratio)  
- house age (age)
- house grade (gd)
- basement 
- renovation (rev)
- waterfront view (waterfront)
- city

<b>Q4</b>. What are the top features that have stronger relationship with house price?
1. <b>sqft_living</b>: bigger the living area, higher the house price

2. <b>grade</b>: the construction material and level of craftmanship relate to the grading of the house thus higher grade, better quality
<img src="images/grade difference.png">

3. <b>waterfront</b>: geography location make waterfront important (not every city has a water nearby) 
<img src="images/waterfront difference.png">

4. <b>city</b>: The top 3 cities are Medina, Mercer Island, and Bellevue
<img src="images/city difference.png">

The top 3 cities locate in the center of the North region with water nearby (Lake Washington).
<img src="images/City Name Map.png">

## Model Evaluation
|   | Basic Model | Model 3 |
| :---: | :---: | :---: |
| # of features | 4 | 36|
|Train R2  | 0.537 | 0.774 |
|Test R2  | 0.529 | 0.765 |
| Train RMSE  | 252724.942 | 0.250 |
|  Test RMSE  | 245604.251 | 0.253 |

## Conclusions
Among analyze 21243 house data, a multiple linear regression model was built based on 36 features include: sqft_living,  sqft_lot, rm_ratio, age, grade, city, waterfront, basement, and renovated. Homebuyers can use my model to predict the house price with given parameter values<br>
***
Some recommendation for potential homebuyers are:
- <b>Feburay</b> is the best month for potential homebuyers to purchase houses with lowest sale price<br>
- North regions are more likely to find a higher price house and south regions are more likely to find a lower price house. Homebuyers can use my price distrbution map to determine the searching area based on budget. 
- There are many features can help predict house price. Some of those features have great impact on house price
- The <b>top features</b> that have strong relationship with house price are: <b>sqft_living, grade, waterfront, and city</b>

## Future Work
Further analysis can be explored on the following to provide additional insights and improve the performance of the model.
- <b>School Ranking</b>: Education resource and school quality are highly correlated which should determine the wealthiness of the city thus impact house price.
- <b>Nearby Feature</b>: Transportation, dinning, grocery stores, and recreation area accessbility can also affect house price
- <b>Market Fluctuation</b>: Acquiring data beyond May 2015 can better understand market trend and price growth/decline. Potential homebuyers may also consider re-selling the house for getting profit

## For More Information
See the full analysis and modeling in the jupyter notebook and presentation.<br>
For additional information please contact, JingYun (Jonna) Wang at jingyunwang24@gmail.com