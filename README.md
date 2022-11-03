# UWFinTechModule14

## Overview of the Analysis

The purpose of this analysis is to use different machine learning models in order to improve an existing trading algorithm. This analysis will use the existing algorithmic trading system as a baseline performance and the adjusted trading algorithm with machine learning will be used to compare performances.


## Results

* Baseline Performance:

![cr_baseline](https://user-images.githubusercontent.com/61864923/199658229-f476c192-2f91-4688-bff8-e2e73cd512ab.png)

![svmplot](https://user-images.githubusercontent.com/61864923/199658236-c24455ec-4e68-4c29-96b0-585cfa682d9a.png)

  * Overall accuracy of 64%.
  * In predicting the '-1' or signal to sell stock short, the model was 100% accurate with a precision of 1, but has a low recall value which shows that the model is not likely to correctly sell stock short.
  * In predicting the '1' or signal to buy stock long, this model has a precision of 63% and has a recall of 100%.

Based on the graph, the model shows to have performed better than the actual returns as the strategy returns is recorded to be above actualy returns and still positive.

___

* Tuned Dataset Size Performance:

![cr_size](https://user-images.githubusercontent.com/61864923/199658301-84ec587f-5fd6-497c-9d91-f4e2ad8feab3.png)

![size_svmplot](https://user-images.githubusercontent.com/61864923/199658308-f536297d-c580-4ccf-b325-2406ab85ecbf.png)

  * Overall accuracy of 57%.
  * Original size of dataset is 3 months. The tuned size of the dataset was adjusted to 8 months
  * The precision of '1' and '-1' were both lower than the baseline performance at 57% for both '1' and '-1'.
  * Slight differences in recall and f1-score values.
 
Looking at the graph, the strategy returns was similar as actual returns for the first 3 months, but afterwards, the model does perform better but still remains a negative value.

* Tuned Window Performance:

![cr_sma](https://user-images.githubusercontent.com/61864923/199658328-1e29deb1-f618-46a7-a339-5f02ec0e1351.png)

![sma_svmplot](https://user-images.githubusercontent.com/61864923/199658333-2a09ff49-c776-4fa6-9c76-b7f6f7baf33c.png)

  * Overall accuracy of 58%.
  * Original windows for short and long are 4 and 100 days respectively. The tuned window for short and long were changed to 10 and 50 respectively.
  * Precision values of the tuned window performance is also below the baseline performance at 55% for '1' and 59% for '-1'.
  * Recall and f1-score were higher for '-1' in tuned window performance compared to the baseline performance.
 
Based on the graph, the tuned window performance had the same returns up until the last 15 days in the dataset where the model eventually performed better but still contained a negative returns.

* Logistic Regression Performance
    
![cr_lrm](https://user-images.githubusercontent.com/61864923/199658348-81c88192-516b-4bb5-8d09-67f61a960928.png)
    
![lrmplot](https://user-images.githubusercontent.com/61864923/199658365-a0002872-9100-456d-b65d-c9009ffcde8c.png)
  
  * Overall accuracy of 66%.  
  * Best precision for '-1' at 88% but low recall.
  * Similar precision, recall, and f1-score for '1' when comparing to baseline performance.

Based on the graph this model performed best. After a month the model deviated from the actual returns and maintained a higher, postive, returns.

## Summary

In conclusion, we can see that the machine learning model using logistic regression performed much better than the other learning models despite having similar values in the classification reports. However, the logistic regression model can not be the best performance that can be achieved. There are many different adjustments that can be made, whether it is using different technical analysis, window size, training dataset size, or learning model. I would recommend trying out many other combinations and learn the behavior of those changes to predict a more efficient model.

