## About the project -

The project gives an understanding of the explainable AI techniques Counterfactuals and Counterfactuals guided by prototypes. Unlike other feature importance techniques that only provide information on rank of the features based on importance, these techniques highlight the 'what-if' explanations and give insight on the changes in the features that would have led to a different prediction or in other words, the necessary alternations in order to get a specific prediction. The aim is to study the interpretability of the black box models through these methods for better problem solving and improve their trustworthiness.

## Interpretation -

### Counterfactuals - 

When a machine learning model is applied to real world data, along with the reason for the decision of its outcome, it is also essential to know  “what should be the change in features in order to switch the prediction”. Counterfactual explanations is a model agnostic XAI technique that provides the smallest changes that can be made to the feature values in order to change the output to the predefined output. Counterfactual explanations work best on binary datasets. They can also work on classification datasets with more than 3 target values, but the performance is not as good as it is on binary classification datasets. In other words, if X is an independent variable and Y is a dependent variable, counterfactual shows the effect on Y due to small changes in X. Also, it helps to calculate what changes need to be done in X in order to change the outcome from Y to Y'. It gives us the ‘what-if’ explanations for the model. 

The perturbed data returns multiple new instances for a different result and thus there can be many possibilities of counterfactuals. However, not all counterfactuals are attainable since the changes in values should also be feasible and practical (for eg. change in age or sex is not possible or change in the country is not feasible). 

Example on Heart Disease dataset:

The heart disease has two target values: 
0 - which signifies that the patient does not have a heart disease.
1 - which signifies that the patient does have a heart disease.
From this dataset, we have taken a specific instance where the patient has a heart disease. We generate 4 different counterfactuals, all of which show us the minimum changes that we can 
make to the feature values in order to change the condition of the patient. 

![cf](https://user-images.githubusercontent.com/72971618/110421964-7cc28400-80c4-11eb-88f4-210bd9f147aa.PNG)

- We cannot change the sex, age or the type of chest pain of a person suffering from a heart disease. Therefore, we can see that in each of the counterfactuals, we have kept those features unvaried. 
- The 4 different counterfactuals are all different ways of solving one problem, which is to change the target value from 1 to 0. 
- For example, if we look at the second counterfactual on the list, we can see that reduction of cholesterol will lead to decreasing the intensity of the heart disease. Among several other changes, it also shows that upon performing the Thallium test on the heart, there should be normal results and no defects.
- A recurring theme in all counterfactuals is the reduction of ‘ca’ from 2 to 0. ‘ca’ signifies the number of blocked vessels of heart. ca is the most important feature contributing to having a heart disease. So, from the results, we can say that the most important factor in changing the condition is to reduce the number of blocked vessels by using methods like angioplasty.

### Counterfactuals guided by Prototypes -

Counterfactual guided by prototype simply refers to the explanations that are described on the basis of a prototype i.e. a sample which is representative of the instances belonging to a class. Counterfactuals guided by prototypes is an advanced and more accurate version of counterfactuals. The counterfactuals guided by prototypes method works on black-box models.This method is a model agnostic approach to interpret results using the prototypes of classes of target variable and is faster compared to the counterfactuals. 
It is much faster than counterfactual because of its prototype approach which speeds up the search process significantly by directing the counterfactual to the prototype of a particular class. 

The counterfactual generated from making perturbations in the instance tends to the prototype that is the least far. Once the class prototype is defined (using a trained encoder or by k-d trees) for each predicted class, the closest prototype different from the original prediction class is found. Mathematically, a loss term is present L proto in its formula which helps to reduce the distance between the nearest prototype and the original instance to be explained. This Lproto loss term minimizes the distance between the nearest prototype and the counterfactual. Therefore, the perturbations then approach to the nearest prototype, thereby reducing the time. Since instead of just the loss term associated with the encoder, a special term is used which is unique to the prototype, more interpretable and meaningful outcomes are produced in much less time. The loss term pertaining to the prototype is used by the model to introduce noise and inturn check the stability of the model. 


## Datasets - 
As this technique is applicable to both image and tabular dataset, it is applied to the following datasets:
- Heart Disease Dataset
- Fashion MNIST



