# Predicting house prices with machine learning methods
Fintech Bootcamp Project 2

> # Our project is a fintech tool that can be utilized by both private and public sectors to analyze current markets and predict future value within specific states. 

## Technologies
- python 3.9.13
- JupyterLab
- libraries: pandas, pathlib, numpy, sklearn, statsmodels
- visualization: matplotlib, hvplot, seaborn, scipy.stats


## Installation 
If you want to run the program yourself and/or enter different data, do the following:
1. To install the project files, go to the GitHub page for the workshop, click on the green Code button, then download the repository as a ZIP file. 
<img width="1055" alt="image" src="https://user-images.githubusercontent.com/111472420/209233539-a5dc56c0-f40e-4e6b-8c63-d8378b2b3b60.png">
2. Unpack a zip file into the directory you can operate from in JupyterLab. 
<img width="1055" alt="image" src="https://user-images.githubusercontent.com/111472420/209233613-77022fb4-56d8-4441-9fc4-321ad45a4792.png">
3. Install the required libraries via Terminal and Run the code! 
<img width="1055" alt="image" src="https://user-images.githubusercontent.com/111472420/209233677-ca2947ca-e66c-45ff-8f59-2c7d96ad0e9e.png">

## Overview
In our project we tried to predict future house prices values based on Ordinary Least Squares regression technique in order to minimize the sum of the squared errors. </br> </br>
**Input variables**: 'bed', 'zip_code', 'acre_lot', 'bath', 'house_size', 'state'. </br>
**Output variables**: 'price'. </br> </br>
During Exploratory Data Analysis(EDA), 'month' feature was removed from the data. Although 'zip-code' and 'state' obviously correlate with each other, we still use both of this features as better results were produced by the model. Same case with 'bed' and 'bath' features. <br></br>
Also, at the EDA stage outliers were detected and removed from the data. The highest plank on the price was set to $3.500.000, so that the model would provide more accurate results. </br>
<img width="580" alt="image" src="https://user-images.githubusercontent.com/111472420/209236994-2b9db744-958f-4fe6-84d5-8ec036f34ec7.png"> </br> </br>

The "state" categorical feature was encoded with OneHotEncoder. Features were normalized with StandardScaler. Output variable 'price' was transformed with log method. We split the data to Training and Testing sets with sklearn train_test_split. </br> </br>
 **First Results with training dataset** <br>
 <img width="618" alt="image" src="https://user-images.githubusercontent.com/111472420/209238066-0096e93e-9a11-4077-9a3a-24f7d8d73af4.png"> </br></br>
*R-squared score*: 48% (this statistic indicates the percentage of the variance in the dependent variable that the independent variables explain collectively) </br>
*MSE*: 23% (the average squared difference between the estimated values and the actual value) </br> </br>
<img width="621" alt="image" src="https://user-images.githubusercontent.com/111472420/209238564-fafa7048-d4e5-42d1-b5ba-069990cfb7b7.png"> </br>
<img width="594" alt="image" src="https://user-images.githubusercontent.com/111472420/209238604-ccab77a0-392b-4c78-9a31-d2c22531de05.png"> </br>

The analysis have shown that the model won't be able to accurately predict sales prices. But the distribution of residuals actually shows us that the linear model is the best fit for our purposes, so we got the best results we could. </br> </br>

**Model Evaluation** </br></br>
*R-squared score*: 45% </br>
*MSE*: 24% </br> </br>
<img width="304" alt="image" src="https://user-images.githubusercontent.com/111472420/209238832-5f424dac-b925-40a5-b45c-75edd7a68d81.png"> </br>
<img width="1078" alt="image" src="https://user-images.githubusercontent.com/111472420/209238890-afbf3268-48a0-4b8e-9c1a-a130abe5284f.png"> </br>

The analysis have shown that the model cannot accurately predict house prices. One reason is because the set of chosen features is not optimal. One way to fit this is to perform Principal component analysis (PCA) (although there seems to be a problem with encoded 'state' variable that causes the problem of multicolinearity) or to run a feature elimination method (RFE, for example). But we came to the conclusion, that it's not the question of reducing number of features, rather than adding more. </br>
Though it is common knowledge that factors such as the size, number of rooms and location affect the price, there are many other things at play. Additionally, prices are sensitive to changes in market demand and the peculiarities of each situation, such as when a property needs to be urgently sold.


## Contributors

Contributors are:

1. Galiya Khusniyarova
2. Maria Angeles Bonany
3. Christopher Swanson
4. Jorge Villacreses
