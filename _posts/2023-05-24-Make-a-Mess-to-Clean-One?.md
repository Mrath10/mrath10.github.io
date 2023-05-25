# Make a Mess to Clean One?

Remember how i talked about Question 2 seeming simple enough, i was kinda right at wrong.

## It's actually Quicker but you can't really see it!

Being a student that is currently taking COMP4702 (Machine Learning) at UQ I have been learning the standard practices for how one approaches developing a machine learning model and i have to say it turns some of the principals on their heads, lets get into it shall we?

## You train and Tune?

I think one of the biggest hurdles in my understanding of fastai was how it handles training and testing of the model. In typical machine learing enviroments, we tend to do this in 3 stages:
  1. obtain and process input data
  2. split the data into training and testing
  3. use the training data to develop the model
  4. Test the model against the test data and evaluate its performance
  5. tune the model as needed to improve performance
 
 Seems simple enough? fastai kind of jumbles up this order and while it goes against my intuition, it works out to be alot quicker and in some cases, better. 
 
 For starters, fast ai splits the initial data into training and validation sets. like normal ML the training set it used to train the model using the following lines of code:
 
```python
learn = vision_learner(dls, resnet18, metrics=error_rate)
learn.fine_tune(3)
```

The first line for will train the model on the first set while the second will run the tune the model based on the validation set for a specified number epochs. thats steps 2-5 in one go! It is but it also is not. we just created a model based on data that has not been processed, won't his lead to all kinds of issues? if you left it as is maybe, thats why we do what comes next!

## Train Again?
As Jermey had pointed out in his second lecture for fast ai, a really efficient way to process our input data is to actually train our model first and then let it tell us what it was most uncertain about, or what it failed at. we then take a look at it and decide whether our model misclassified or it tried to make sense of well, garbage. We achieve this by using the following lines:
```python
interp.plot_top_losses(10,nrows=3,figsize=(17,15))
cleaner = ImageClassifierCleaner(learn)
cleaner
```

using top losses we can see what the model struggled with and from that we get get the following decicison matrix

|        | Model said Yes       | Model said No       |
| -------------- | -------------- | -------------- |
| I said Yes     | We Good  | Please dont plug me into the matrix|
| I said no | Skynet Scary too| What even is that|

Jokes aside (please dont hurt me my machine overlords) we used the image classifier cleaner to find what images were incorrectly identified or waste for both the training and validation set. We then retrain our model based on this new data and viola, step 1 is completed! it just took doing the rest first!
 
You really thought i wouldnt?
![](/images/clean_data.jpg "Drake Gets It")


---
Adios!
