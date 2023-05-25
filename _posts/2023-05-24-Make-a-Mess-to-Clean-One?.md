# Make a Mess to Clean One?

Remember how i talked about Question 2 seeming simple enough, i was kinda right at wrong.

## It's actually Quicker but you can't really see it!

Being a student that is currently taking COMP4702 (Machine Learning) at UQ I have been learning the standard practices for how one approaches developing a machine learning model and i have to say

Question 2! the multi classfication problem. it seemed simple enough, I was wrong - very wrong.

## Find my Bird!

to attempt to complete my question 2 i decided to get the notebook *00-what-is-a-bird* working. I felt like this example was simiar enough to what i needed to do for question 2, get images, train a model, tune the model and use this model on our training set. 

In my journey to get this question working little did i know what lurked around the corner, the search errors. 

## .fpx?
using the search function had provided me several errors, the occansional time out, the search function not working because it didn't seem to recognize the search function that was literally defined the line above. Thanks to [this](https://lovellbrian.github.io/2023/05/16/Bug.html) post on brians blog i was able to resolve my issues!

That was until i had reached an error that would plauge me for hours, the **.fpx** file type error (this was taken form the ed post i had made):

![](/images/fpx_pain.png "why")


While this error was extremely fustrating at first, thanks to it i understood how alot of this notebook works:
  - the error does not actually occur when *search_images_ddg* is called but rather when the image is being resized. 
  - *search_images_ddg* will retrieve a range of image file types, not strictly JPEG's
  - running this piece of code for two different directories can end up with them having a large amount of images being identical in both
 
I did learn some other things but i'll keep them for my next blog post which will detail my process for question 2. I have to say that i have found alot of this to be interesting

and it tends to parallel some of the practices and theory from my machine learning course: *COMP4702*. while similar they approach certain aspects of developing your model differently which i find very interesting. 

Beside all of this i have to say resolving this issue took a lot longer than i liked, i literally deleted the image file and ran it the next day - Good bye .fpx!

I think its kind of becoming a traditon to leave a meme at the end of my post so i will keep doing so:
![](/images/burning_meme.jpg "It Really be like that")


---
Adios!
