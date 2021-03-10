## Interpretation -
Integrated Gradients, also known as Path-Integrated Gradients or Axiomatic Attribution for Deep Networks is an XAI technique that gives an importance value to each feature of the input using the gradients of the model output. It is a local method that helps explain each individual prediction. Integrated Gradients is a method that is simple to implement and is applicable for various datasets such as text datasets, image datasets and structured data as well as models like regression and classification models. This method shows us the specific attributions of the feature inputs that are positive attributions and negative attributions. 
 
1. Positive attributions: Positive attributions are attributions that contributed or influenced the model to make the decision it did. For example, in the Fashion MNIST dataset, if we take the image of a shoe, then the positive attributions are the pixels of the image which make a positive influence to the model predicting that it is a shoe. It can be various specific pixels showing some unique features of a shoe such as laces, sole, etc. 
 
2. Negative attributions: Negative attributions are attributions that contributed or influenced the model against making the decision that it eventually did. For example, in the Fashion MNIST dataset, if we take the image of a shoe, then the negative attributions are the pixels of the image which go against the model predicting it as a shoe. For example, the sole of a shoe might be mixed as a flip flop. This would make the model think that the clothing item in the image is not a shoe. 
 
This method has various applications and is primarily used to check where the model is making mistakes so that amendments can be made in order to improve the accuracy of the model. In this way, it can help a developer in debugging as well as makes the model more transparent for the users. 

![ig](https://user-images.githubusercontent.com/72971618/110587865-34759580-819a-11eb-88db-aa952ad086f7.PNG)

Explaining the two examples shown above:
 
We have taken an example on the dataset of Fashion MNIST, which consists of 70,000 grayscale 28x28 images of different clothing items. The label consists of 10 classes, which denotes different kinds of clothing items such as shirt, hoodies, shoes and jeans. 
 
1st Example: It is an image of a shoe. The attributions section shows a melange of positive and negative attributions together. As we can see from the bar on the right side, green signifies positive attributions and purple signifies negative attributions. The shoe is unique compared to other clothing items, and hence, it has a lot more positive attributes than negatives. The lining, collar and back part of the shoe are the main pixels that influence the decision of the model. On the other hand, the negative attributions are negligible for this particular instance. 
 
2nd Example: It is an image of a shirt where there is an equal number of positive and negative attributions. The pixels around the collar and the sleeves are the biggest positive attributions. However, the middle portion of the shirt can be mistaken to be a part of a pair of jeans or trousers. Therefore, due to this ambiguity, they are the negative attributions for the prediction. All in all, we can say that when the positive attributions outweigh the negative attributions, the model makes the correct prediction. 
