# machine_learning_trading_bot
Challenge 14 of University of Denver's Fintech Bootcamp

The following analysis will show three different machine learning bots and compare the difference of performance when certain paramaters are changed.

**Base Model**

![s4l100](https://user-images.githubusercontent.com/101432134/195971387-5e2a3903-89e4-406e-a38c-0c837eb65d3d.png)

As you can see, over the course of 6 years, the base model actually performed better than actual market return with a 1.5x return compared to a 1.4x.

**Step 1: Tune the training algorithm by adjusting the size of the training dataset.**

Changing the size of the training dataset from 3 months to 6 months, we see the model outperform the actual returns with 1.8x compared to 1.6x.  All other parameteres were unchanged.

![6mobase](https://user-images.githubusercontent.com/101432134/195971644-4b19e088-499c-4011-b33b-34e4badd2990.png)

**Step 2: Tune the trading algorithm by adjusting the SMA input features.**

Keeping the 3m month time frame the same, I changed the SMA short window from 4 to 5 and the SMA long window from 100 to 120.

![2sma](https://user-images.githubusercontent.com/101432134/195972094-6bf2f909-b81f-483b-8fe9-a80690c0718e.png)

These results produce and environment that shows the actual returns (1.6x) performing better than the stragey returns (1.5x).

**Step 3: Choose the set of parameters that best improved the trading algorithm returns.**

Based on the above results, it appears by adjusting the date parameters, you will get a stronger performance for the trading algorithm.  Would not recommend changing the SMA values.

**Step 4: Logistic Regression Model**

For the last step, I used the LogisticRegression model:

![1linearregression](https://user-images.githubusercontent.com/101432134/195972558-1e186df5-1c5c-4aa1-8ba5-42e2b0747e36.png)

This LogisticRegression model appears to outperform the other models.  The best strategy is the original which gave us a SMA fast of 4, SMA slow of 100 and a 3 month time period.
