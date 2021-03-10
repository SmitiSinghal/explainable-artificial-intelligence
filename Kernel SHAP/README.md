## Interpretation -
The goal of SHAP is to calculate the impact of every feature on the prediction. Compared to Shapley values, Kernel SHAP gives more computationally efficient and more accurate approximation in higher dimensions. In Kernel SHAP, instead of retraining models with different permutations of features to compute the importance of each, we can use the full model that is already trained, and replace "missing features" with "samples from the data" that are estimated from a formula. This means that we equate "absent feature value" with "feature value replaced by random feature value from data". Now, this changed feature space is fitted to the linear model and the coefficients of this model act as Shapley values.
It has the capability of both local and global interpretations i.e. it is able to compute the importance of each feature on the prediction for an individual instance and for the overall model as well. The SHAP values are consistent and reliable because if a model changes so that the marginal contribution  of a feature value(which means percentage out of the total) increases or stays the same (regardless of other features), they increase or remain the same respectively. Thus, these values are mathematically more accurate and require fewer evaluations. However, it assumes the features to be independent which may sometimes give wrong results.

### Local explanation:

![image](https://user-images.githubusercontent.com/72971618/110588741-794dfc00-819b-11eb-96e7-7be5397f3b3c.png)

The base value is the average of all output values of the model on the training data(here : -0.3148). Pink values drag/push the prediction towards 1(pushes the prediction higher i.e. towards having heart disease) and the blue towards 0(pushes the prediction lower i.e. towards no disease).
The magnitude of influence is determined by the length of the features on the horizontal line. The value shown corresponding to the feature are the values of feature at the particular index(eg. 2.583 for ca). Here, the highest influence is of ca for increasing the prediction value and of sex for decreasing the value.

### Global explanation:

![image](https://user-images.githubusercontent.com/72971618/110588815-91be1680-819b-11eb-87b2-db189fe876b3.png)

The above plot visualizes the impact of features on the prediction class 1. The features are arranged such that the highest influence is of the topmost feature. Thus, ca is the feature that influences the prediction the most followed by thal and so on. 
The colour shades show the direction in which the feature impacts the prediction. For example, higher shap values of ca are shown in red colour which means high feature value. The higher the value of ca, the higher is the SHAP value i.e. more towards 1 . High value of ca indicates more chances of Heart Disease. Almost all features show this pattern. However, it is the opposite for some features: High thalach will indicate no heart disease.

## Dataset - 
Since, this technique can only be applied to Tabular Data, it is applied on Heart Disease Dataset.
