# Inspiration
* As I have worked on more than 70 datasets till now, I wanted to have a sneak-peak into industry related processes starting from client acquisition to presenting 
them with insights and findings. This project covers such step in a detailed manner where machine learning algorithms are as necessary as client communications.

## Communicating Approach
 Wrote an email describing my  thoughts and findings to AD, focusing on the data that I would need from the client and the analytical models I would use to test such hypothesis of wether price sensitivity affecting customer churn.
 # Exploratory Data Analysis
 * Some of the datatypes are not correctly denoted, it was changed to correct format. Also numerical data seems to be highly skewed.
 * Its an unbalanced dataset with churning customers records make approximately 10% of total.
   ![image](https://user-images.githubusercontent.com/102746816/161384208-891e0006-79e7-4b68-ab65-91269b943b5f.png)
* Various sales channels are observed, the above plot shows last three sales channels have no churn till date.
   ![image](https://user-images.githubusercontent.com/102746816/161384279-78c6259c-6604-4cf6-9c10-41c49d4d5ff0.png)

* There was no high correlation of price for customer churn directly, as we have taken sum and average of price for each customer for peak, mid-peak and off-peak prices for both energy and power. So feature engineering was necessary in our part to obtain high correlation.
  ![image](https://user-images.githubusercontent.com/102746816/161384427-c2328a90-1533-4db6-a789-eee5508b014e.png)

#### Before proceeding to feature engineering an auto-corelation and partial auto-correlation plot were plotted to observe relation between any two months in the year.i.e Observing seasonality in price data.
# Feature Engineering

* As defining price sensitivity was a task assigned to me, I researched various definition for it and most of the cases include product as numerator. As our service is a **subscription type**, so I defined price sensitivity as **difference between month A and present month divided by present month price** .

  ![Figure](https://latex.codecogs.com/png.image?\dpi{110}&space;\bg_white&space;Sensitivity=\frac{Price(Month_1)-Price(Month_2)}{Price(Month_2)})
  
 * After several observations and analysis, I found price sensitivity defined taking Month_1 as January and Month_2 as December of previous year, had the best correlation with the churn of customer. Few of the feature engineered columns are picked from plethora of columns having the best correlation value.
 * As there were both negative sensitivites(price has decresed) and postive sensitivities(price has increased), total of 9 columns are observed separately for corelation with churn to study for both wether price increse is affecting churn or price decrese is encouraging customer to not churn.
 * A final dataset is created considering best correlated columns and modelling was done on this dataset where feature engineered columns had more say in it.
 # Model Building
 * Various models are fit with hypertuning of parameter and XGBoostClassifier was found to be best model.
 * Smote was used to improve recall value, as detection of customer churning is more important than predicting wether a customer will stay with us or not.
 # Executive Summary 
 * A final **executive summary** was created for delivering insights to client which was one page summary for all the analysis done by me.
