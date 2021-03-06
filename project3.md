## Project 3, due April 18

##### Using two machine learning methods predict population values at 100 x 100 meter resolution throughout your selected country. Validate the two models using different methods presented in this class. Write a report assessing the two approaches and which of the two models was more accurate. Be sure to account for spatial variation throughout your selected location and provide substantive explanations for why those variations occurred

For this project, I chose to focus on the Philippines, specifically the regions of Davao del Norte, Davao del Sur, Davao Oriental, and Compostela Valley. The linear regression, 
random forest, and support vector machine models that I ran all performed pretty well. The linear regression and random forest models both had very similar ME, MAE, and RMSE plots. Looking at the RMSE plots for both models, it is clear that overall, the models had little error, but had very high error in a few particular localities. The 
highest root mean squared error location, seen clearly in the 3D plots, appears to be the areas near the city of Mati, although it is hard to tell exactly. The support vector
machine model, which I added as a stretch goal, does not account for spatial variation, but I did add the step of scaling the data using a simple min-max scaling function, so the RMSE is much lower, at 0.0791883. The R-squared for this model is also about 0.5, which is not that great but higher than I expected for such a simple model. Looking at the variable importance plot for the random forest model, it is clear that the NTL and DST190 variables were the most important predictors. I think this is a pretty logical result, because it makes sense that night time lights would correlate highly with population. It also follows that urban cover (dst190) would likewise correlate with higher 
centers of population. I think this is a good result because it shows that the model is correctly attributing the more important variables.

#### Linear Regression Model:

Population sums plot:

<img src = "https://user-images.githubusercontent.com/54942759/115155197-cea7e380-a04c-11eb-8b24-c37e7a64b830.png" width = 500>

Diff sums plot:

<img src = "https://user-images.githubusercontent.com/54942759/115155316-60afec00-a04d-11eb-97cf-5b10c4151c9b.png" width = 500>

Mean Error:

<img src = "https://user-images.githubusercontent.com/54942759/115155055-1c701c00-a04c-11eb-99fc-c0d1576f873c.png" width = 500>

Mean Absolute Error:

<img src = "https://user-images.githubusercontent.com/54942759/115155083-3f9acb80-a04c-11eb-8bfd-40336b084a56.png" width = 500>

Root Mean Squared Error (3D):

<img src = "https://user-images.githubusercontent.com/54942759/115155124-796bd200-a04c-11eb-94a5-027219608881.png" width = 500>

Cell stats (diff sums): 6016931

#### Random Forest Model:

Population sums plot:

<img src = "https://user-images.githubusercontent.com/54942759/115155496-31e64580-a04e-11eb-89a3-de98fce34500.png" width=500>

Diff sums plot:

<img src = "https://user-images.githubusercontent.com/54942759/115155510-432f5200-a04e-11eb-9b3b-a6a733cc3608.png" width = 500>

Variable importance plot:

<img src="https://user-images.githubusercontent.com/54942759/115155539-7540b400-a04e-11eb-9b06-1d8270068b9c.png" width = 500>

RF Mean Error:

<img src = "https://user-images.githubusercontent.com/54942759/115155701-0adc4380-a04f-11eb-8f4c-ae66898fcf44.png" width = 500>

RF Mean Absolute Error:

<img src = "https://user-images.githubusercontent.com/54942759/115155716-1c255000-a04f-11eb-9d75-4515fd32569d.png" width = 500>

RF Root Mean Squared Error (3D):

<img src="https://user-images.githubusercontent.com/54942759/115155656-f0a26580-a04e-11eb-984f-360f04dcc80c.png" width=500>

Cell stats (diff sums): 5721193

#### Stretch goal: Support Vector Machine model

Source: https://www.kaggle.com/thapelomola/svm-with-caret

For this model, I attempted to examine the effect of dependent variables on sum.pop15. Obviously this is a different approach than the linear regression and random forest models above because it does not incorporate the geospatial element. The R-squared for this model is 0.5085856, which is not terrible but not very good either. The RMSE is  0.0791883 and the MAE is 0.03668218. 

```
library(caret)
library(MLmetrics)
data_split <- initial_split(data, prop = 4/5)
data_train <- training(data_split)
data_test <- testing(data_split)

TrainCtrl1 <- trainControl(method = "repeatedcv", number = 5,repeats=5,verbose = FALSE)
set.seed(512) 
SVMgrid <- expand.grid(sigma = c(0.025), C = c(2))

X <- data_train[,-10]
X_scaled <- (X-min(X))/(max(X)-min(X))
Y <- data_train$sum.pop15 
Y_scaled <- (Y-min(Y))/(max(Y)-min(Y))
x_test <- data_test[,-10]
x_test_scaled <-(x_test-min(x_test))/(max(x_test)-min(x_test))
y_test <- data_test$sum.pop15 
y_test_scaled <- (y_test-min(y_test))/(max(y_test)-min(y_test))

modelSvmRRB <- train(X_scaled, Y_scaled, method="svmRadial", trControl=TrainCtrl1,tuneGrid = SVMgrid,preProc = c("scale","YeoJohnson"), verbose=FALSE)
PredictedTest <- predict(modelSvmRRB,x_test_scaled)
Accuracy(PredictedTest, y_test_scaled)
```

Output: 

 ```
 >>>modelSvmRRB
Support Vector Machines with Radial Basis Function Kernel 

741 samples
 12 predictor

Pre-processing: scaled (12), Yeo-Johnson transformation (12) 
Resampling: Cross-Validated (5 fold, repeated 5 times) 
Summary of sample sizes: 593, 593, 593, 592, 593, 593, ... 
Resampling results:

  RMSE        Rsquared   MAE       
  0.07918833  0.5085856  0.03668218

Tuning parameter 'sigma' was held constant at a value of 0.025
Tuning parameter 'C' was held constant at a value of 2
```

SVM Model Mean Error Plot:

<img src = "https://user-images.githubusercontent.com/54942759/115250742-de303680-a0f7-11eb-9786-d48a5033a525.png" width = 500>

SVM Mean Absolute Error Plot:


<img src = "https://user-images.githubusercontent.com/54942759/115251323-6f071200-a0f8-11eb-8f1f-abccff5cc538.png" width = 500>


SVM Root Mean Squared Error Plot (3D):

<img src = "https://user-images.githubusercontent.com/54942759/115251064-29e2e000-a0f8-11eb-9736-dfa295cfe01c.png" width = 500>







