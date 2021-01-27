# TED Talk Classification

![Title Image](https://github.com/yamasjose11/ted-predictor/blob/main/images/ted1.jpg)

# Motivation and Objective

My motivation for this project is woven in my underlying passion for learning and TED Talks never fail to teach me something new. I want to explore what exactly makes a show worth watching. That is exactly what I wanted to do when choosing this project. I will be trying to use text classification to help me in doing so and in this case a binary classification.

# The Data

My dataset contains over 2,500 official Ted Talk Transcripts up to late 2017. With this, my agenda consisted of using all of the full TED Talk transcripts and the views each one received for my Natural Language Processing (NLP) Pipeline. Viral shows made it hard to use the mean as a target split and cause inbalanced issues. So I decided to make a relative split at 1 million views where this would account for the bulk majority of the views and combat any imbalanced issues. 

![Title Image](https://github.com/yamasjose11/ted-predictor/blob/main/images/target_splits.png)

# The Approach (TF-IDF and Random Forest)

I chose to vectorized all the transcripts using TF-IDF Vectorizer and went with a Random Forest Classifier for its good "off the shelf" performance. As part of using the Random Forest Classifer model I knew I was mostly focused to see how accurately the model could predict TED Talks favorability to I mainly focused on the recall score. The reason I chose to go with the recall score is because the recall score tell us, what fraction of all the Ted Talks that are originally labeled as *Favorable* are Detected as *Favorable*. I also just included the accuracy score as it is a very easy to interpret score and tell us a summarized version of how the model is performing

# The Results and Insights (Feature Importance)

(Baseline Model)
(Feature Importances)
(Tuned Model)

![Title Image](https://github.com/yamasjose11/ted-predictor/blob/main/images/project_results.png)

# Future Development

For future development I strongly believe continuing down the path of further investigating the feature importances can continue to help me improve my model by increasing recall in both classes. I would also like to build a Flask App where it can use an API call for the most recent Ted Talk and predict if the ted talk will be more favorable than its counterparts.

# Acknowledgements

A very special thank you to the instructors at Galvanize Inc., Dan Rupp and Juliana Duncan, for all of their guidance during this project. Also, thank you to my classmates Hilmi Kilickaya for his comprehensive suggestions.

# References

Temple, O., 2016. TED Talks- Complete List - dataset by owentemple. [online] Data.world. Available at: <https://data.world/owentemple/ted-talks-complete-list> [Accessed 27 January 2021].

# Contact Me 

(QR Code)
