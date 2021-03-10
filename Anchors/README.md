## Interpretation -
Anchors are the local-limit sufficient conditions of certain features at which the model gives a high precision prediction. In anchors, the features are narrowed down to certain conditions (i.e. anchors), which gives the prediction. Anchors is based on the algorithm which works for model-agnostic approach for classification models of text, image and tabular data. Anchor takes into account the global dataset and then gives the anchor feature-values. It is based on If-Then rules for finding the features of the input instance responsible for the prediction which makes it reusable and clear for which other instances it is valid.

Anchors are pretty much similar to LIME as they both provide local explanations linearly, but the problem with LIME is that it only covers the local region which might give overconfidence in the explanation and might not fit for an instance which is not trained. LIME is only able to describe a particular instance which means that, when new real world data is given as input which is unseen, it may give confusing or unfaithful explanations. This is because it only learns from a linear decision boundary that best explains the model. This is where Anchors has an advantage over LIME. Anchors generate a local region that is a better construction of the dataset to be explained. The boundaries are clear and cover the area such that it is best adapted to the model's behaviour. If the same perturbation space is given to both LIME and Anchors, the latter will build a more valid region of instances and which better describes the model’s behaviour. Moreover, their computation time is less as compared to SHAP. Thus, Anchors are a very good choice to validate the model’s behaviour and find its decision rule.


![image](https://user-images.githubusercontent.com/72971618/110590615-072ae680-819e-11eb-85ec-45d982b2084b.png)

Suppose we take an instance where the features of the person contribute to him/ her having a heart disease. We now apply the AnchorTabular method to see which features contribute significantly for such type of prediction.

The value of thalach of this person is 131 and ca is 3, therefore AnchorTabular method makes the following conclusions.
- The person's maximum heart rate is 131 (which is less than 138)
- The blood vessels coloured by fluoroscopy are 3 (greater than 1)
As the maximum heart rate of a person should be high and the blood vessels coloured by fluoroscopy should be low, the above features act as anchors for the patient and deduce that the person has a heart disease.

## Datasets - 
As this technique is applicable to both image and tabular dataset, it is applied to the following datasets:
- Heart Disease Dataset
- MNIST
