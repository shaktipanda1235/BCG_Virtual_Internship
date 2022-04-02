# Inspiration
* As I have worked on more than 70 datasets till now, I wanted to have a sneak-peak into industry related processes starting from client acquisition to presenting 
them with insights and findings. This project covers such step in a detailed manner where machine learning algorithms are as necessary as client communications.

## Communicating Approach
 Wrote an email describing my  thoughts and findings to AD, focusing on the data that I would need from the client and the analytical models I would use to test such hypothesis of wether price sensitivity affecting customer churn.
 # Exploratory Data Analysis
 * Some of the datatypes are not correctly denoted, it was changed to correct format. Also numerical data seems to be highly skewed.
   ![image](https://user-images.githubusercontent.com/102746816/161384208-891e0006-79e7-4b68-ab65-91269b943b5f.png)
* Its an unbalanced dataset with churning customers records make approximately 10% of total.
   ![image](https://user-images.githubusercontent.com/102746816/161384279-78c6259c-6604-4cf6-9c10-41c49d4d5ff0.png)
* Various sales channels are observed, the above plot shows last three sales channels have no churn till date.

  ![image](https://user-images.githubusercontent.com/102746816/161384427-c2328a90-1533-4db6-a789-eee5508b014e.png)
* There was no high correlation of price for customer churn directly, as we have taken sum and average of price for each customer for peak, mid-peak and off-peak prices for both energy and power. So feature engineering was necessary in our part to obtain high correlation.
#### Before proceeding to feature engineering an auto-corelation and partial auto-correlation plot were plotted to observe relation between any two months in the year.i.e Observing seasonality in price data.
# Feature Engineering

* As defining price sensitivity was a task assigned to me, I researched various definition for it and most of the cases include product as numerator. As our service is a **subscription type**, so I defined price sensitivity as **difference between month A and present month divided by present month price** .

  ![Figure](https://latex.codecogs.com/png.image?\dpi{110}&space;\bg_white&space;Sensitivity=\frac{Price_Month_1-Price_Month_2}{Price_Month_2}
