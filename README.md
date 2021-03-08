# What is eXplainable AI (XAI) -
eXplainable AI or XAI in short, is basically a way to remove the ambiguity in machine learning methods and to enable transparency, so that the outcomes of black-box models can be easily understood by humans.  
# Why XAI -
With AI forming the future of all complex decision making, it is crucial to know how and why these decisions were made. Artificial Intelligence clearly enhances the speed, precision and effectiveness of human efforts. For example, AI techniques can be used to identify which transactions are likely to be fraudulent, as well as automate manually intense data management tasks in financial institutions, or it can be useful for face recognition in cameras.

However, consider an AI-powered medical diagnosis system that predicts cancer or heart disease in a patient previously diagnosed as healthy by medical experts.  Human life cannot be put to risk unless the predictions of the models are transparent and provide a legitimate reason for the result.  If an AI system provides counterintuitive advice when picking stocks or an AI autonomous vehicle drives unpredictably and causes a fatal collision despite normal road conditions, then in such cases, it’s essential to know why the model took the decisions and behaved in the way it did. This is where XAI comes into the picture. It has the potential to explain the underlying black-box processes and to provide trust in AI.

# XAI Techniques -

XAI offers practical methods to look inside the black box. The following are some of them :

1. ALE -  Accumulated Local Effects 
2. Anchors
3. CEM - Contrastive Explanation Methods 
4. LIME - Locally Interpretable Model-Agnostic Explanations
5. SHAP 
6. Integrated Gradients
7. Counterfactuals and Prototype Counterfactuals

XAI techniques can help in reducing the complexity of AI systems to a great extent by providing the understandability and explainability to the models. All the above techniques help to explain the machine learning models in some way or the other.

# Datasets used for the project -
## Tabular Data:
- Heart Disease Dataset
- The Iris Dataset
- Boston Housing Prices

## Image Data:
- MNIST 
- Fashion MNIST

## About Heart Disease dataset :

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
![dataset](https://user-images.githubusercontent.com/72971618/110315771-b85f3e80-802f-11eb-8556-3159c73f53ae.png)

# Conclusion - 

Thus, XAI is important for AI to thrive in certain sectors like healthcare. The deployment of Explainable AI basically provides interpretability of the model which is required to increase the trust in machine learning models and AI software. Using this, health practitioners can diagnose diseases and can provide the right treatment to the patients easily. For instance, consider a heart patient and a model which predicts if the person is suffering from the heart disease. In this case, Explainable AI can explain why the model categorized the person to be ill or otherwise, which would in turn increase the reliability of AI.