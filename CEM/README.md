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

### About Heart Disease dataset :

Heart disease is among the biggest causes of deaths in the entire world. Prediction of a heart disease is one of the most important area
in the healthcare sector. Heart disease refers to blockage or narrowing down of blood vessels, which can lead to chest pain or heart attack. The Heart Disease Cleveland UC Irvine dataset is based on prediction if a person has heart disease or not based on 13 attributes. It is re-processed from the original dataset having 76 features. In the following, we describe 13 features briefly:

1. age: An integer value signifying the age of an individual.

2. sex : 0 for female, 1 for male.

3. cp: cp stands for the Chest Pain Type and ranges from 0-3 depending upon the symptoms experienced by a patient. 
According to the symptoms experienced, chest pain types are classified in the following ways:
(a) 0 - Typical Angina: Experiencing all three symptoms
(b) 1 - Atypical Angina: Experiencing any two symptoms
(c) 2 - Non-Anginal Pain: Experiencing any one symptom
(d) 3 - Asymptomatic Pain: Experiencing none of the symptoms mentioned above
If cp is high, less exercise should be performed and sugar and cholesterol level of the body should be maintained

4. trestbps: trestbps shows the resting blood pressure calculated in units of millimeters in mercury (mmHg). The ideal blood pressure is 90/60mmHg to 120/80mmHg. High blood pressure is considered to be anything above 140/90mmHg.

5. chol: chol represents the cholesterol levels of an individual. A high cholesterol level can lead to blockage of heart vessels. Ideally, cholesterol levels should be below 170mg/Dl for healthy adults. 

6. fbs: fbs represents Fasting Blood Sugar levels of a patient, by gauging the amount of glucose present in the blood. A blood sugar level below 100mmol/L is considered to be normal.
(a) 1 signifies that the patient has a blood sugar level in excess of 120mmol/L
(b) 0 signifies that the patient has a blood sugar level lower than 120mmol/L

7. restecg: restecg depicts the electrocardiograph results of a patient. restecg
ranges between 0-2.
(a) 0 - Normal results in ECG
(b) 1 - The ECG Results have a ST-T wave abnormality
(c) 2 - The ECG Results show a probable or definite left ventricular hypertrophy by Estes’ criteria

8. thalach: thalach shows the maximum heart rate of an individual using a Thallium Test. 

9. exang: exang is a feature that reveals whether a patient has exercise induced angina (signified by 1) or not (signified by 0). 

10. oldpeak: oldpeak is the amount of depression of the ST Wave in the case of a patient having a value of 1 in restecg (ST-T Wave abnormality found in ECG Results). 

11. slope: slope is also concerned with the ST Wave in ECG Results.
(a) 0 signifies an upward slope in the ST Wave
(b) 1 signifies that the ST Wave is flat
(c) 2 signifies a downward slope in the ST Wave

12. ca: The heart has 3 main vessels responsible for blood flow. An angiography is carried out and because of the dye, the unblocked vessels show up on a X-Ray. Ideally, three vessels should be visible on the X-Ray as this would mean that none of the vessels are blocked. 

13. thal: thal denotes the results of Thallium test of an individual.
(a) 0 denotes that the results were normal.
(b) 1 denotes a fixed defect.
(c) 2 denotes a reversible defect.
Here, defect symbolises an obstruction in optimum blood flow. 

Figure depicts example instances of the heart disease dataset.
