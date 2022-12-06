# California-Housing-Prices
This dataset is based on data from 1990 California census.
## Looking at the Big Picture
The data pertains to the houses found in a given California district and some summary stats about them based on the 1990 census data.<br>The columns are as follows, their names are pretty self explanitory:

longitude

latitude

housingmedianage

total_rooms

total_bedrooms

population

households

median_income

median_house_value

ocean_proximity

This includes metrics for each block group in California.  
Block groups are the smallest geographical unit for which the US Census Bureau publishes sample data (a block group typically has a population of 600 to 3,000 people). 
We will just call them “districts” for short.
## Our Aim:
Is to bulid a model that should learn from this data and be able to predict the median housing price in any district, given by any other metrics. 

## The Objective in Business terms.
   - The model’s output (a prediction of a district’s median housing price) will be fed to another Machine Learning system along with many other signals.
   - This downstream system will determine whether it is worth investing in a given area or not. Getting this right is critical, as it directly affects revenue.

## The current solution before Using machine learning:
The district housing prices are currently estimated manually by experts, teams gathers up-to-date information about a district, and when they cannot get the median housing price, they estimate it using complex rules.<br>
This is costly and time-consuming, and their estimates are not great; in cases where they manage to find out the actual median housing price, they often realize that their estimates were off by more than 20%. <br>
This is why the company thinks that it would be useful to train a model to predict a district’s median housing price given other data about that district.<br>
The census data looks like a great dataset to exploit for this purpose, since it includes the median housing prices of thousands of districts, as well as other data.

## Frame of the problem
It is clearly a typical **supervised learning task** since we are given labeled training examples (each instance comes with the expected output, i.e., the district’s median housing price).<br>
Moreover, it is also a typical **regression task**, since we are asked to predict a value. More specifically, this is a multiple regression problem since the system will use multiple features to make a prediction.<br>
It is also a univariate regression problem since we are only trying to predict a single value for each district.

## Selecting Preformance Measure
A typical performance measure for regression problems is the Root Mean Square Error (RMSE). <br> 
It gives an idea of how much error the system typically makes in its predictions, with a higher weight for
large errors.
