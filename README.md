

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
7. sklearn.model_selection import train_test_split
8. sklearn.pipeline import Pipeline
9. sklearn.feature_extraction.text import CountVectorizer, TfidfTransformer
10. sklearn.multioutput import MultiOutputClassifier
11. sklearn.preprocessing import OneHotEncoder
12. sklearn.ensemble import GradientBoostingClassifier, RandomForestClassifier
13. sklearn.metrics import fbeta_score, make_scorer
14.  sklearn.model_selection import GridSearchCV, RandomizedSearchCV
15. sklearn.metrics import accuracy_score, f1_score

## Project Motivation<a name="motivation"></a>

The data-sets analyzed contain simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.

In this project I am building a model that predicts if a customer will respond to an offer or not based on the provided data sets. I will approach this issue in several steps: First I want to get a general understanding of the data sets. Second, I will clean and combine the data sets as basis for a machine learning model. As a consequence, each row of the new data set will provide information of the offer itself, the related customer and whether or not the offer was successful or not. Finally, I will build a model that predicts if a customer will respond to an offer or not.

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

Additionally, a Jupyter Notebook with all the relevant code is porvided
**Starbucks_Capstone_notebook-5.ipynb**

## Acknowledgement <a name="acknowledgement"></a>
Udacity and Starbucks

Further resources:
https://medium.com/airbnb-engineering/overcoming-missing-values-in-a-random-forest-classifier-7b1fc1fc03ba

https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html and https://stackoverflow.com/questions/6986986/bin-size-in-matplotlib-histogram

https://stackoverflow.com/questions/6986986/bin-size-in-matplotlib-histogram

https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MinMaxScaler.html

https://uc-r.github.io/ts_benchmarking#naive

https://www.programcreek.com/python/example/84417/sklearn.metrics.accuracy_score

https://de.wikipedia.org/wiki/Random_Forest

https://towardsai.net/p/machine-learning/why-choose-random-forest-and-not-decision-trees

https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html
