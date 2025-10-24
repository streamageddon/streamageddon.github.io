# streamageddon.github.io

## What is it?

Streamageddon is our Data Science project which aims to find similarities between artist who boycotted Spotify as well as possibly predict whether an artist is likely to boycott Spotify in the future. The reason to conduct this project is to raise awareness about Spotify's questionable practices such as its CEO investing money into war drones or not paying their artists.

## How did we approach this problem?

We collected data about ~100 artists who boycotted Spotify recently or in the last few years. Then we collected data about other artists who did not leave and used machine learning techniques to make the algorithm distunguish between the two. We based our prediction on multiple factors, such as artist's followers count, popularity rate and genres they perform. You can read more about technical details in our tech report! (add link to the report later)

## And the results are...

Studying our datasets, we spotted a few interesting details. First, the distribution of genres between two groups of artists was different. Between artists who boycotted, there is a significant shift towards folk and alternative artists. You can see the difference in the plots below.

...well, our prediction results did not turn out so great. Our model was good at predicting if an artist wouldn't boycott, but the accuracy of classification artists who actually left was very low (f1-score 0.13), meaning that our model was heavily biased towards artists who did not boycott. There is a number of possible reasons for that.

### Problems and limitations

One reason that comes to mind is the size of our dataset. It is true that a lot of artists were leaving Spotify lately, but still not enough to get a reliable analysis. About a hundred entries in a dataset is not nearly enough to draw trustworthy conclusions about a group, and this is why our model might have struggled. There were many entries in the negative dataset (those who did not leave), and our model did its best to learn patterns of the negative class, but did not have enough information about the positive class even using techniques that address imbalanced datasets.

