# TED Talk Classification

![Title Image](https://github.com/yamasjose11/ted-predictor/blob/main/images/ted1.jpg)

# Motivation and Objective

My motivation for this project is woven in my underlying passion for learning and TED Talks never fail to teach me something new. I want to explore what exactly makes a show worth watching. That is exactly what I wanted to do when choosing this project. I will be trying to use text classification to help me in doing so and in this case a binary classification.

# The Data

My dataset contains over 2,500 official Ted Talk Transcripts up to late 2017. With this, my agenda consisted of using all of the full TED Talk transcripts and the views each one received for my Natural Language Processing (NLP) Pipeline. Viral shows made it hard to use the mean as a target split and cause inbalanced issues. So I decided to make a relative split at 1 million views where this would account for the bulk majority of the views and combat any imbalanced issues. 

<!-- Target Split EDA -->
<p align="center">
  <img width="600" height="250" src="https://github.com/yamasjose11/ted-predictor/blob/main/images/target_splits.png">
</p>

# The Approach (TF-IDF and Random Forest)

I chose to vectorized all the transcripts using TF-IDF Vectorizer and went with a Random Forest Classifier for its good "off the shelf" performance. As part of using the Random Forest Classifer model I knew I was mostly focused to see how accurately the model could predict TED Talks favorability to I mainly focused on the recall score. The reason I chose to go with the recall score is because the recall score tells us, what fraction of all the Ted Talks that are originally labeled as *Favorable* are Detected as *Favorable*. I also just included the accuracy score as it is a very easy to interpret score and tell us a summarized version of how the model is performing

# The Results and Insights (Feature Importance)

<!-- (Baseline Model) -->

When letting the model predict for itself, the biggest take away was that the model really struggled trying to classify the True Positives for Class 0, the Non-Favorable bunch.

<!-- (Feature Importances)-->

As I took on the challenge to improve the model I knew my main focus was to improve the recall score for the True Positives. I started by looking into my feature importances and trying to get an insight of the use of words that held more value in helping the model classify one from the other. 

For my feature importances in my first model I was surprised to see how many bland type of words were labeled as important, that I felt didn't hold any true meaning in classifying, so through an iterative process added to the text processing steps. After doing so I also added lemmatizing to the words to see if some features would converge using their root words. After doing so I saw some more interesting words pop up that seemed to have more linguistic meaning such as “understanding” instead of “say” and many more.

(eda feat imp 1)

<!-- (Tuned Model) -->


After further investigation I also handled the features by implementing unigrams in conjunction to some bigrams and realized in order to improve my model I can use both for better classification. Some really interesting insights when implementing bigrams was seeing some words like “Health Care” and “Every  Day”.

So after getting more insight in the feature importances I decided to plot a ROC curve and see how the performance compared between the two models from 0 to 100% -  the first model being the baseline model and the second being the tuned model. After plotting the ROC curve I got more insight in where I could further tune the model by adding a threshold value to help me improve the True Positive values.

(Add ROC CUrve eda)

With the implementation of n-grams and threshold values I was able to get a significant increase in performance and was able to increase the True Positive Values. 

<!-- Project Result EDA -->
<p align="center">
  <img width="800" height="450" src="https://github.com/yamasjose11/ted-predictor/blob/main/images/project_results.png">
</p>

# Future Development

For future development I strongly believe continuing down the path of further investigating the feature importances can continue to help me improve my model by increasing recall in both classes. I would also like to build a Flask App where it can use an API call for the most recent TED Talk posted and predict if the TED Talk will be more favorable than its counterparts.

# Acknowledgements

A very special thank you to the instructors at Galvanize Inc., Dan Rupp and Juliana Duncan, for all of their guidance during this project. Also, thank you to my  classmate and friend Hilmi Kilickaya for his comprehensive suggestions.

# References

Temple, O., 2016. TED Talks- Complete List - dataset by owentemple. [online] Data.world. Available at: <https://data.world/owentemple/ted-talks-complete-list> [Accessed 27 January 2021].

# Contact Me!

<!-- (QR Code) -->
<p align="center">
  <img width="250" height="125" src="https://github.com/yamasjose11/ted-predictor/blob/main/images/Jose_YamasQR.png">
</p>
