# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).



## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

----------------------------


The purpose of the analysis is to gain insights into the risk of extending a credit and determining if that decision may be a risk or not given previous information and factors.
Based on the results obtained, it is evident that although the accuracy remains consistent, the underlying approach to achieving this outcome differs.

In the case of model 1, an issue arises due to the imbalanced data distribution. During training and testing, the model exhibited better prediction performance for the '0' category, which had a sample count of 75,036, compared to the '1' category, which only had 2,500 samples. This skewed sample distribution posed challenges for the effectiveness of this model.

The significance of sample quantity in achieving accurate training and testing is well-established. Inadequate sample representation hampers model efficiency. Consequently, a transition was made to model 2, incorporating Over Sampling to address the sample distribution imbalance. This technique involves duplicating '0' and '1' instances until an equal count of 112,541 samples each is attained. This rebalanced dataset enabled more effective training and testing, preserving information that might otherwise have been lost if alternative approaches were used.

In this context, a '0' indicates a credit-worthy scenario, while issues arise when a true negative outcome emerges in the first model, totaling 102 instances. Conversely, a '1' signifies a less favorable credit option, highlighting 56 false negative occurrences in the same model.

Model 1 achieved a 99% accuracy in predicting '0' instances and a 91% accuracy in predicting '1' instances. However, the second model demonstrates a notable difference, where errors are detected but represent a mere 1% of the total due to the considerably larger sample pool. This yields an impressive 99% accuracy for both '0' and '1' predictions.

The primary challenge lies in misclassifications of '1' instances (associated with high-risk loans), indicating instances where the bank refrains from extending credit to individuals with sound credit profiles. While this prevents potential profit, it also averts losses. On the other hand, if errors were skewed towards misclassifying '0' instances, it would translate to monetary losses for the bank. In the hierarchy of priorities, the bank's preference is to forego potential gains rather than incur losses.

In summary, this approach facilitates the granting of more credits while not posing a substantial challenge to address.









