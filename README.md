# Machine Learning For Credit Risk Model(PD, LGD, EAD)
## I.  Intro

Approving loans without thorough scientific evaluation increases the risk of default, potentially leading to the bankruptcy of lending institutions and destabilizing the banking system. This was a key factor in the 2008 financial crisis, which severely impacted the global economy. Three components determine the extent of loss a firm incurs due to loan default:

* Probability of Default (PD)
* Exposure at Default (EAD)
* Loss given Default (LGD)
The expected loss (E-Loss) is the simple product of these three quantities:

ELoss=PD⋅EAD⋅LGD

Our focus here is on the Probability of Default (PD). In this context, we will examine the example of the German Credit dataset.
## II.  [Libraries](https://github.com/Kevin20250000000/Machine-Learning-For-Credit-Risk-Model/blob/main/Liberies)

## III. [Exploratory Data Analysis]
<img width="329" alt="Screenshot 2025-05-28 at 21 04 31" src="https://github.com/user-attachments/assets/f9e7ef7e-9b5a-4f80-b415-dbec17303597" />

In this dataset, females are slightly more likely to default; however, this should not be generalized. This pattern is clearer in the graph below.

## IV. Analysis
![image](https://github.com/user-attachments/assets/a4fcb840-1c1a-44d5-8ba3-790ee1ffb907)

![image](https://github.com/user-attachments/assets/e1c88a90-ad88-49bf-8382-01728d178076)

![image](https://github.com/user-attachments/assets/b28b8fd4-ea95-478d-bf7f-a37acb44ec9a)

![image](https://github.com/user-attachments/assets/826f8ebe-790a-4c07-9366-b5de671e27da)

![image](https://github.com/user-attachments/assets/74fc386f-6346-42cf-81bc-1c236220114c)

![image](https://github.com/user-attachments/assets/4687ff66-8dc6-48e7-b591-dfdb2366bc9a)

![image](https://github.com/user-attachments/assets/ab954ad4-1c4b-4059-8c07-83e66fbe3bab)

## V. Model Selection with Cross Validate
<img width="510" alt="Screenshot 2025-05-28 at 21 07 52" src="https://github.com/user-attachments/assets/22315c86-6369-4970-bb8d-a76b972d93f8" />


Model Evaluation on the Testing Set:

The Random Forest Classifier performs well on both training and testing scores.

SVC and Gaussian Naive Bayes exhibit less overfitting.

The Gaussian Naive Bayes Classifier has the shortest runtime.

Additionally, the Random Forest Classifier provides feature importance measures, whereas SVC only returns coefficients (coef_) with a linear kernel, which can be computationally slow.

## VI.  Conclusion

1. Machine learning–based models are highly practical for minimizing risk. An increasing number of banks adopt these models for risk analysis to reduce losses by preventing defaults. There are numerous machine learning techniques for tasks such as prediction, classification, and clustering. While our case only scratches the surface, certain considerations are crucial when applying machine learning techniques:

2. The model should be explainable. If an algorithm denies a loan application, the bank must understand the reasoning; otherwise, it may face legal challenges from the applicant. Therefore, it is often preferable to use relatively simple and interpretable models—such as logistic regression, gradient-boosted trees, or Random Forest (as in our case)—instead of more complex models like neural networks.

3. Recently, Apple’s credit card was accused of discriminating against women. Models can inherit social biases because they learn from historical data. Similarly, our model predicted that females are more likely to default, partly due to using a discrete-time hazard model, where default probability is treated as a point-in-time event. A more robust approach incorporates the evolution of feature impacts on risk over time. Such models, known as Through-the-Cycle (TTC) models, account for macroeconomic conditions, social changes, and other external factors.






