# Where are we at

So Question 2 is pretty much compeleted now, i have to say. it was a true journey but i learnt alot and seriously had some fun.

## Confusion matricies aren't confusing

Like the title suggests, i don't find confusion matricies confusing at all! infact i think a confusion matrix is the least confusion metirc. looking at one of these it is not too hard to follow:

|        | Actual Positive    | Actual Negative       |
| -------------- | -------------- | -------------- |
| Predicted Positive    | True Positive  | False Positive|
| Predicted Negative | False Negative| True Negative|

The leading diagonal tells you what was correctly identified and the other parts tell you what a certain class was misclassified as, Simple! In fact this metric is amazing at telling you the overall performance of a model beacuse these values are used to build the F1 score, this is a metric that helps us evaluate our models performance by combining the precision and recall scores of our model. specifically, it's much better than the accuracy score for cases where you are dealing with a data set tha only has small variance e.g. detecting turmors. 

## Whats worse then?

tSNE.

Stumbling across this metric i had a hard time understanding why you would choose to use this over PCA to help evaluate the performance of the model. It didn't take much digging thought, tSNE is really amazing. This metric is able to determine the what general general features are commonly linked together when a particular class is identified, it computes these relationships that exists in higher dimensions and plots them on a 2D plane for our conviniece as serperated clusters take a look below:

![](/images/tsne.jpg "tSNE")

I mean no matter how much i look at it i still dont understand how higher dimesnions can be represented like this, machine learning really is amazing.

 
For the road:

![](/images/tsne_meme.jpg "Tis Not Simple")


---
Adios!
