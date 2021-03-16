# Social Media Post Classification within the MediaEval 2015 dataset

## TASKS
- Data Analysis
- Algorithm Design
- Evalutation

## MODULE
Machine Learning Technologies (COMP32222)

## DESCRIPTION
This individual project was set with an aim to explore ways of automatically classifying Twitter news related content as real or fake. Within this coursework, I designed a machine learning algorithm for classifying Twitter posts from MediaEval 2015 "verifying multimedia use" challenge dataset.

The project was based on Python and Jupyter Notebook, along with the use of scikit-learn library, numpy, pandas and deep translator.
The dataset contained 14,277 training data entries and 3755 testing data entries, and each entry had the following set of features:

tweetId / tweetText / userId / imageId / username / timestamp / label

## DATA ANALYSIS
Here are some of the graphs produced throughout the data analysis.

![alt text](https://pro2-bar-s3-cdn-cf6.myportfolio.com/b7c2137b5057ea5273c14b898858e93b/ae29785b-cc3f-4eff-af97-176fcf3a62be_rw_600.png?h=9cd28964ee10114756f7316cbeee33b2 "Length of tweets") 
![alt text](https://pro2-bar-s3-cdn-cf.myportfolio.com/b7c2137b5057ea5273c14b898858e93b/87e26586-ce1c-4b38-9507-8887d8792c07_rw_600.png?h=b2afa7f078ec750b33eb5f0b86bb16f7 "Length of fake tweets") 
![alt text](https://pro2-bar-s3-cdn-cf5.myportfolio.com/b7c2137b5057ea5273c14b898858e93b/667f0dab-e42a-4fb4-a4c7-c9d959d85520_rw_600.png?h=c985a2d1a4db18b08a318399770a96cb "Length of real tweets") 
![alt text](https://pro2-bar-s3-cdn-cf1.myportfolio.com/b7c2137b5057ea5273c14b898858e93b/c2a0ae4e-81b5-4f11-a052-d2746ec45c18_rw_600.png?h=d24d70186305588e2d0f7f110f410e7a "Tweet counts by label") 

## ALGORITHM DESIGN
The algorithm design part started with the preprocessing steps taken. This task consisted of data cleaning by removing punctuation from tweets, text lowercasing, stop word removal, emoji removal as well as translation. Once the preprocessing was completed, the tweetText features were vectorized and transformed into a term frequency inverse document frequency matrices.

Considering all the constraints and the characteristics of the data, 3 starting classifiers were chosen: MultinomialNB / LinearSVC / SGDClassifier. 

## EVALUATION AND RESULT

The classifiers were evaluated and the strongest learner (MultinomialNB in this project) was chosen to further perform hyper parameter tuning through GridSearch. Additionally, other features like the imageId and username were used in an iterative process.

The best performance was achieved by using the TweetText and username feature, which resulted in an accuracy score of 89.26%.

Once the project was submitted, I received detailed feedback for them module leader highlighting the strengths of this work, mainly being the data analysis and code quality, as well as areas of improvement like additional feature selection. This project was awarded a 1st class mark of 70%.
