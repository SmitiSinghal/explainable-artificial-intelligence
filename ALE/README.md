## About ALE -

The notebook gives an understanding of the explainable AI technique Accumulated Local Effects (ALE). It is a model agnostic method which works on black box models and describes how the prediction is influenced by various features of the model on an average. The aim is to study how the technique helps to reveal the model's behaviour.

Installation -

It is a part of alibi package. You can simply run: pip install alibi

The method is applied to both classification and regresssion datasets.

## Interpretation -
ALE is a technique like other feature importance techniques such as PDP plots that allows us to determine the change in prediction based on certain minor changes in the features. It measures the response of the regressor to specific changes. All features are plotted using ALE values and increasing or decreasing trends are studied. This technique successfully identifies the most and the least relevant features of our dataset.

It tackles the primary drawbacks of PDP (Partial Dependence Plots). Partial Dependence Plots are one of the most popular methods for visualising the effects of each feature on the predictions for a black box model. However, PD Plots produce erroneous results when the features of the dataset are highly correlated. This is where ALE Plots come in the picture. ALE Plot is a model agnostic algorithm that provides global explanations for classification and regression models on tabular data. They are preferred over PD Plots, as they produce good results in spite of there being a correlation between features. ALE Plots are also less computationally expensive as compared to PD Plots. ALE Plots visualise the effect that each feature, isolated from all other features, has on the predictions of the model. A second order ALE plot can also show the amalgamated effects of multiple features on the output. 


## Dataset - 
Since, this technique can only be applied to Tabular Data, it is applied on -
- Heart Disease Dataset (Classification)
- Boston Housing Prices (Regression)
