

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

This project is part of the Udacity Nanodegree Program "Become a Data Scientist". Basis of the Project is a Starbucks Dataset which simulates the purchasing behaviour of customers and how their decisions are influenced by promotions.

This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.
The basis of this project are three datasets: portifolio.json, profile.json and transcript.json.
The portfolio dataset includes general offer-information such as which channel was used to communicate with potential customers (email, mobile, social), the difficulty which represents the amount of money a customer must spend in order to receive a discount, the duration of the offer, an unique offer id, the offer type and finally the reward itself.
The profile data set provieds detailed customer data such as age, gender, income and the date, an account was created via the Starbucks app.
The transcript data set lists purchases and detailed information about when and if an offer was completed or not. An offer can be regarded as successfull, once a customer both views an offer an reaches its difficulty within the odder's duration.
In the following, I am going to build a model that predicts if a customer will respond to an offer or not based on the information provided in the data sets. I will approach this issue in several steps: First I want to get a general understanding of the data sets. The Data Understanding section (1) will be used to understand and get to know the provided data. Second, I will be clean and combine the data sets as basis for a machine learing model (2). In order to prepare and clean the data, categorical variables must be replaced by dummy variables, numercial features must be normalized, NaNs must be eliminated and the offer_id must be cleaned (transcipt data set) in order to identify a key value to merge the data frames. Once all data is cleaned, the data sets can be combined. As a consequence, each row of the new data set will provide information of the offer itself, the related customer and whether or not the offer was successful or not.
Finally, I will build a model that predicts if a customer will respond to an offer or not. I will do so by computing the accuracy and the F1-Score of a naive model as a benchmark. The accuracy measures how well the model predicts an offer is successfull or not. The F1 score can be interpreted as a weighted average of the precision and recall, where a F1 score reaches its best value at 1 and worst score at 0. This model will be used as a benachmark for the other model I will cosntruct.

Link to Medium-Post: https://felixburkhardt.medium.com/starbucks-promotional-offer-analysis-9596cced1510

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
Udacity and Starbucks

Further resources:
https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html and https://stackoverflow.com/questions/6986986/bin-size-in-matplotlib-histogram

https://stackoverflow.com/questions/6986986/bin-size-in-matplotlib-histogram

https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MinMaxScaler.html
