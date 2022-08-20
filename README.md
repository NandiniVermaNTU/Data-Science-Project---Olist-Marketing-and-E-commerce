# Data-Science-Project-Olist-Marketing-and-E-commerce
Using the Brazilian Olist Marketing and E-commerce dataset, sales trends were analysed and revenue was evaluated for 2016, 2017 and 2018. Data was also explored to suggest marketing strategies for subsequent increase in future sales and revenue. 

## Data Visualisation and Analysis
- Box plots were used to analyse payment values to discern the average order amount. The box plots represented the median, quartiles (25th and 75th) and the outliers. An instance is shown below:
![image](https://user-images.githubusercontent.com/77065857/185730230-c100e2b0-5461-49eb-85c7-946ee0f9651e.png) 
- Bar graphs were used to visualise monthly revenue. Months with the highest and lowest sales were and the categories with the maximum sales plus the corresponding revenue generated by that category in that month was also figured out. An instance is shown below:
![image](https://user-images.githubusercontent.com/77065857/185730148-5369f8e8-21aa-4ea6-a30e-a07b3b66f01f.png)
![image](https://user-images.githubusercontent.com/77065857/185730203-c507e36a-b5d7-47b8-af0a-47401356681c.png)
- Weekly sales analysis surprisingly showed lesser sales during the weekend.
- Hourly sales analysis shows high sales from 9 am to 11 pm. Working hours in Brazil are roughly between 8 am to 6 pm.
- Positive correlation was observed between the number of photos available for a product and its sales especially in categories like female fashion.


## Data Preparation
- Data is clenaed by removing rows with null values.
- Grouped rows and columns from different data frames having a common variable.

## Machine Learning
- The aim is to predict future revenue by analysing past revenue. 
- For monthly revenue prediction, we have used the model called _Prophet_ designed by Facebook. This model can capture seasonal variations very well (good for sales data as they are expected to have sales variations), the user does not need to specify any parameters (the model itself decides its parameter).
- The other alternative we looked into was _auto ARIMA_ which does not work well with seasonal variations. If we used ARIMA, we would have to specify the parameters correctly.
- Time series data for 2017 was analysed. X-axis showed the months in the year while the Y-axis denoted the respective revenue for that month. An instance is shown below: 
![image](https://user-images.githubusercontent.com/77065857/185730125-3544555b-9665-4502-8dfb-f0729662ef29.png)
- We trained the model to learn from 2017 data as for 2016 and 2018, there were some months with missing revenues. 2017 had revenue data for all months.
- We predicted the sales revenue for 2017 using the available 2017 data and it predicted exactly the same data it learnt from. This was done to crosscheck the efficiency and functioning of the model. 
- Predictions were made for 2018 as follows:
![image](https://user-images.githubusercontent.com/77065857/185730459-e64fab6a-85e1-44e7-bea9-a8957e7ac246.png)
- Since the model had limited data to learn from, the prediction of monthly revenue for 2018 had some discrepancies when compared with the actual revenue data of 2018. 
![image](https://user-images.githubusercontent.com/77065857/185730521-05eaeca2-2287-4590-a5a8-b0cb30bccd93.png)

## RFM Analysis

- RFM analysis is a data driven customer behavior segmentation technique. RFM stands for recency, frequency, and monetary value. The idea is to segment customers based on when their last purchase was, how often they've purchased in the past, and how much they've spent overall.

- We used the elbow method to find the ideal number of clusters for segmentation. It groups the customers on the basis of their previous purchase transactions i.e., how recently, how often, and how much did a customer buy. RFM filters customers into various groups for the purpose of better service. A higher score is better. A score of 444 shows that the customer is loyal and is the best score.

![image](https://user-images.githubusercontent.com/77065857/185730641-59ad126f-0fae-4ff6-ba2b-393d336a3307.png)
This plot gives us a clear understanding of the count of customers in each category.The arrow points towards 444 which consists of the most loyal customers.



