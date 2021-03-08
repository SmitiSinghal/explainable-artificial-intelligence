## About the project -

The project gives an understanding of the explainable AI technique Contrastive Explanation Method(CEM). It is a model agnostic method which reveals the black box behaviour by informing about the the features that should be compulsorily presnt and the ones that must be necessarily absent to maintain the original prediction. In other words, it mentions how the absence of certain features or presnce of specif features may result to a different prediction than the original target class. Our aim is to unfold the model using this method in order to gather such information for better understanding of the the AI systems.

## Installation -

It is a part of alibi package. You can simply run: pip install alibi
Import the required package: import CEM

The method is applied to both classification and regresssion datasets.


## Interpretation -

It is the first method that gives the explanations of both what should be minimally present and what should be necessarily absent from the instance to be explained in order to maintain the original prediction class. In other words, the method finds the features like important pixels in an image that should be sufficiently present to predict the same class as on the original instance as well as identifies a minimal set of features that is enough to differentiate it from the nearest different class.

The 2 kinds of explanations can be defined as follows:

Pertinent Positives (PP): The Pertinent Positives explanation finds the features that are necessary for the model to predict the same output class as the predicted class. For example, this includes the important pixels of an image, the features having a high feature weight, etc. In MNIST we change the features from 1's to 0's until the most minimal outline of the number is present that is sufficient to predict the number. PP works similar to Anchors.

Pertinent Negatives (PN): The Pertinent Negatives explanation finds the features that should be minimally and sufficiently absent from an instance whilst maintaining the original output class. PN works similar to Counterfactuals. To get a PN, changes are made such as changing the value of pixels from 0's to 1's in MNIST such that the prediction flips to a different outcome.

In order to create interpretable PP’s and PN’s, feature-wise perturbation needs to be done in a meaningful way.

Using CEM, we can improve the accuracy of the machine learning model by looking at cases of misclassified instances and then working on them using the explanations provided by CEM.

## Datasets - 
The technique is applied to the following datasets:
- Heart Disease Dataset
- The Iris Dataset
- MNIST
- Fashion MNIST


