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

## III. Exploratory Data Analysis 
Risk	bad	good
Sex	 	 
female	35.161290	64.838710
male	27.681159	72.318841

## IV. Age and Sex Distributons
![image](https://github.com/user-attachments/assets/a4fcb840-1c1a-44d5-8ba3-790ee1ffb907)

![image](https://github.com/user-attachments/assets/e1c88a90-ad88-49bf-8382-01728d178076)

![image](https://github.com/user-attachments/assets/b28b8fd4-ea95-478d-bf7f-a37acb44ec9a)

![image](https://github.com/user-attachments/assets/826f8ebe-790a-4c07-9366-b5de671e27da)

![image](https://github.com/user-attachments/assets/74fc386f-6346-42cf-81bc-1c236220114c)

![image](https://github.com/user-attachments/assets/4687ff66-8dc6-48e7-b591-dfdb2366bc9a)

![image](https://github.com/user-attachments/assets/ab954ad4-1c4b-4059-8c07-83e66fbe3bab)

## V. Model Selection with Cross Validate
model	train_score	test_score	fit_time	score_time
0	SVC	0.825890	0.826072	0.040720	0.007020
1	DecisionTree	1.000000	0.752596	0.007312	0.003608
2	RandomForest	1.000000	0.825946	0.328167	0.021596
3	GaussianNaiveBayes	0.811976	0.810961	0.004303	0.003861

## VI.  Conclusion

1. Machine learning–based models are highly practical for minimizing risk. An increasing number of banks adopt these models for risk analysis to reduce losses by preventing defaults. There are numerous machine learning techniques for tasks such as prediction, classification, and clustering. While our case only scratches the surface, certain considerations are crucial when applying machine learning techniques:

2. The model should be explainable. If an algorithm denies a loan application, the bank must understand the reasoning; otherwise, it may face legal challenges from the applicant. Therefore, it is often preferable to use relatively simple and interpretable models—such as logistic regression, gradient-boosted trees, or Random Forest (as in our case)—instead of more complex models like neural networks.

3. Recently, Apple’s credit card was accused of discriminating against women. Models can inherit social biases because they learn from historical data. Similarly, our model predicted that females are more likely to default, partly due to using a discrete-time hazard model, where default probability is treated as a point-in-time event. A more robust approach incorporates the evolution of feature impacts on risk over time. Such models, known as Through-the-Cycle (TTC) models, account for macroeconomic conditions, social changes, and other external factors.






