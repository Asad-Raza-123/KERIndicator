 # Kaufman Efficiency Ratio 
Goal of Project: Create a Kaufman Efficiency Ratio Indicator used for Strategy Development and Backtesting 

Context for Project: The Kaufman Efficiency Ratio is an indicator that evaluates price patterns to determine whether the price pattern shows trend-following behavior or mean reversion behavior. 


<h2>Trend-Following Price Pattern</h2>
If the kaufman efficiency ratio returns a values near 1, then the probability of the price pattern of a given asset that is publicly traded is highly likely to be trendfollowing.
 
![Trend Following](https://github.com/user-attachments/assets/02eeef6d-7672-4546-8df1-c6e9e605cb4e)

<h2>Mean Reversion Price Pattern</h2>
If the kaufman efficiency ratio returns a values near 0, then the probability of the price pattern of a given asset that is publicly traded is highly likely to be mean reverting.
 
 ![sideways](https://github.com/user-attachments/assets/277caaca-dd59-4cbc-bec5-13d0ede2314a)


<h1>KER Formula</h1>

ER = (Change in Price over N periods) / (Sum of the absolute price changes over N periods)

<h2>Method Structure</h2>


![KER Method](https://github.com/user-attachments/assets/ea4141bc-bfa3-4778-9da0-99c8e9113d47)

data1 - a variable that is to take the closing price of a given asset price series. 

dataFrame1 - a variable that takes the asset dataframe that contains open, high, low, and close price series --> adds KER indicator 

length - a variables that takes in a num value that serves as the determinant for each set split number size through which the KER indicator is calculated. 

<br />

 


<h2>Group Splitting</h2>

![KER Code](https://github.com/user-attachments/assets/4401f69a-b11d-46a0-af03-fd4898fae438)

Purpose of Code: Splits closing price series into a groups based on the length given. 

 
<h2>Change in Price over N periods</h2>

![CalculatioNperiod](https://github.com/user-attachments/assets/cc7236f7-6c38-4b4f-bb28-ce92d3076744)

Purpose of Code: To calculate the numerator (Change in Price over N Periods) in the KER formula for each group.

<h2>Consecutive Sum Difference Calculations Retrieval</h2>

![ConsecutiveDiffCalcMeth](https://github.com/user-attachments/assets/27cef8ae-921f-4385-9262-5202f9a0b57c)

Purpose of Code: To retrieve for each group split - two consecutive numbers - for subtraction
--> Calculations used for absolute price changes over N periods calculation 


<h2></h2>


<h2>Absolute Sum Difference Calculation</h2>


 ![Sum of Consecutive Differences](https://github.com/user-attachments/assets/dee17b83-d24b-4996-b47f-4f9624aee38c)

Purpose of Code: Sums all consecutive difference calculations --> (Sum of the absolute price changes over N periods) calculated 


<h2>KER Calculation</h2>

 ![KER Calc](https://github.com/user-attachments/assets/3a91f104-e990-4961-9d5f-f2ee2c400b34)


Purpose of Code: Calculates (Change in Price over N periods) / (Sum of the absolute price changes over N periods) --> KER Calculated 

<h2>KER Output</h2>

 
![KER Indicator Output](https://github.com/user-attachments/assets/8c4808ce-4c65-4cc1-b27f-a75b8c37e576)


Output of KER indicator on a NFLX price series ranging from 2020 to 2025.






 
 
