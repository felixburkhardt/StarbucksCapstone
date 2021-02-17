

### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Acknowledgement](#acknowledgement)


## Installationguide <a name="installation"></a>

The code should run with Python versions 3.*. The following libraries are necessary:


1. pandas
2. numpy
3. math
4. json
5. matplotlib
6. sklearn.tree import DecisionTreeClassifier
7. sklearn.pipeline import Pipeline
8. sklearn.feature_extraction.text import CountVectorizer, TfidfTransformer
9. sklearn.multioutput import MultiOutputClassifier
10. sklearn.preprocessing import OneHotEncoder
11. sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score, make_scorer

## Project Motivation<a name="motivation"></a>

This project is part of the Udacity Nanodegree Program "Become a Data Scientist". Basis of the Project is a Starbucks Dataset which simulates the purchasing behaviour of customers and how their decisions are influenced by promotions. The analysis aswers general questions such as:

- General analysis of offer usage by gender
- General analysis of offer usage by age
- General analysis of offer usage by income
- General analysis of offer usage by offer

Finally, a machine learning model is built. This model helps to predict order completions based on the data provided.

## File Descriptions <a name="files"></a>

The data is contained in three files:

* portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
* profile.json - demographic data for each customer
* transcript.json - records for transactions, offers received, offers viewed, and offers completed

Here is the schema and explanation of each variable in the files:

**portfolio.json**
* id (string) - offer id
* offer_type (string) - type of offer ie BOGO, discount, informational
* difficulty (int) - minimum required spend to complete an offer
* reward (int) - reward given for completing an offer
* duration (int) - time for offer to be open, in days
* channels (list of strings)

**profile.json**
* age (int) - age of the customer
* became_member_on (int) - date when customer created an app account
* gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
* id (str) - customer id
* income (float) - customer's income

**transcript.json**
* event (str) - record description (ie transaction, offer received, offer viewed, etc.)
* person (str) - customer id
* time (int) - time in hours since start of test. The data begins at time t=0
* value - (dict of strings) - either an offer id or transaction amount depending on the record

## Acknowledgement <a name="acknowledgement"></a>
Udacity and Sturbuck

Further resources:
https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html and https://stackoverflow.com/questions/6986986/bin-size-in-matplotlib-histogram

https://stackoverflow.com/questions/6986986/bin-size-in-matplotlib-histogram

https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MinMaxScaler.html
