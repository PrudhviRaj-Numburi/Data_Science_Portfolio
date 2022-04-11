# Exploratory and Predictive Data Analysis

For this analysis, I will use the openly available data from UK Gov website, Road Safety 2019:
<br>
https://data.gov.uk/dataset/cb7ae6f0-4be6-4935-9277-47e5ce24a11f/road-safety-data

## Project Motivation:
Road safety is a pressing concern for many countries, where road crash fatalities and disabilities are gradually being recognized as a major public health concern. It is our social responsibility to be aware of our surroundings and use science and knowledge to help solve real-world problems...
<br>

According to WHO (World Health Organisation nearly 1 million people die in road accidents each year.
<br>

## Business Understanding and Analysis Questions:
<br>

To better guide us through the analysis, I have formulated the problem into the following set of questions, So we can explore it at greater depth:
- Number of accidents and how it has changed over the year?
- When do accidents usually happen?
- What is the age distribution of drivers involved in the accidents?
- How is the severity of accidents depending on Speed limit?
- Different types of propulsion vehicles?
- What is the type of road which causes road accidents?
- Different types of accident severity?
- What are the predictors for road accidents?
- What are the circumstances for casualties?
And in this analysis I have explored problem from different prospectives, yet leaving so much to uncover.

## Plots:
In this section we will answer questions related to the nature and characteristics
of accidents:
1. What is the Accidents pattern over the year?
<br>
<img align="center" width="800" height="350" src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Road_Safety_UK/Images/1.jpg?raw=true">

This simple graph visualises the accidents on monthly basis. We can quickly identify interesting trends in this time-series data. February has achieved the least accidents throughout the years. On the other hand, November accounts for the most accidents, followed by a decrease going into the holidays and New Years! Summer months reported average accidents with slight ups and downs.
<br><br>
2. Average accidents according day of the week?
<br>
<img width="600" height="350" src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Road_Safety_UK/Images/2.png">
<br>
The graph above shows the average accidents per weekday, As you can see on Friday more accidents happend compared to rest of the days. 
<br>

3. Average accidents depending on Daytime?
<br>
<img width="600" height="350" src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Road_Safety_UK/Images/5.png">
<br>
 In this case, we can see Office rush-hours, and Afternoon rush-hours are accounting for more accidents.
 <br>
 <br>
 
 4. Accident Severity:
 <br>
 <img width="500" height="400" src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Road_Safety_UK/Images/3.png">
 <br>
 As you can see there are very less fatal accidents i.e, 1.44% of total accidents and major accidents are slight accidents which is a good news somewhat..
 <br>
 <br>
 5. Does accident severity follows any trend?
 <br>
 <img width="800" height="400" src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Road_Safety_UK/Images/4.png">
 The graph depicts there is almost linear trend for Fatal accidents, Serious accidents, Slight accidents.
 <br>
 <br>
 6. Age and Sex distribution of drivers involved in the accidents:
 <br>
 <img width="700" height="400" src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Road_Safety_UK/Images/6.png">
 <br>
 In order to target road safety campaigns effectively, we must understand our targeted audience. The age distribution is centered around (21–35), highest point was for (26) years old, followed by (21s). Some strange strikes are found around (35 and 55), wonder what is causing that? And we can see Male drivers are more involved in accidents than females.
 <br>
 <br>
 7. Different types of Propulsions involved in accidents:
 <br>
 <img width="500" height="400" src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Road_Safety_UK/Images/7.png">
 Petrol vehicles are more involved in accidents
 <br>
 <br>
 8. Average Number of Casualties depending on Road type:
 <br>
 <img width="650" height="300" src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Road_Safety_UK/Images/9.png">
 <br>
 The above graph depicts more casualties taken place in Dual carriage way and Slip roads.
 <br>
 <br>
 9. Casualties depending on Speed:
 <br>
 <img width="650" height="300" src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Road_Safety_UK/Images/10.png">
 <br>
 <br>
 10. Average number of accidents depending on location (Urban/Rural):
 <br>
 <img width="500" height="450" src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Road_Safety_UK/Images/11.png">
 As it can observed that most of the accidents occurred in Urban areas.
 <br>
 <br>
 11. How are accidents related to Weather conditions?
 <pre>
 accidents.Weather_Conditions.value_counts(normalize=True)
1    0.785427
2    0.130127
9    0.029232
8    0.025896
5    0.012161
4    0.010467
7    0.003353
3    0.002996
6    0.000340
Name: Weather_Conditions, dtype: float64 
</pre>
As most of the days the Weather_Condition is "fine" (=1), most accidents will likely to be happen then.
<br>

### NOTE: More questions answered in Jupyter notebook, Please have a look 

## Modeling:
This is where we can use data science magic to tell us something we didn’t know about our data:

In this part, I have done further cleaning and preprocessing so we can use it on ML algorithm. I have used Supervised Learning algorithm to answer few questions related to dataset. Since the dataset is highly unbalanced we will focus on getting good F1 result rather than accuracy.

Since the dataset is large I have chosen Random Forest as my algorithm, It is robust to outliers and If you use a distance based algorithm and your numerical features range vary widely, the algorithm won’t work properly unless the range of all features is normalized. Tree based models, which we will use here, are not distance based and can handle varying ranges of features. Therefore scaling is not required. In order to handle imbalance in the dataset I have upsampled the data using `SMOTE`.

- What are the main factors affecting accidents?
 <img width="600" height="350" src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Road_Safety_UK/Images/8.png">
 <br>
 
 - What are the major factors affecting Caualities?
 <img width="600" height="350" src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Road_Safety_UK/Images/12.png">
 <br>
 
 - What are the predictors of Police response?
 <img width="600" height="350" src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Road_Safety_UK/Images/13.png">
 <br>
 
 ### Final Thoughts:
 
 In this analysis I have explored the problem from different prospectives, yet leaving so much to uncover. We can summarize our findings as follows:

- From the day-hour plots, we can suggest to increasing response time during rush-hours, or construct roads to divert traffic from congested areaa.
- Investigate high density points in map geolocation analysis to discover construction needs.
- From model feature importnce we can recognize dangerous junctions which cause spesific manoeuvre.
- We explored the conditions of Accidents and Casualties such as (Type of vehicle, Age of driver and location when they got in accidents, etc..), these insights are useful for policy makers to understand how accidents happen and provide solutions to limit the cause.
