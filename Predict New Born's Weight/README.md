# PREDICTING NEW BORN'S WEIGHT

#### I am quoting from the WebMD article:
“A new baby's gender, name, time of birth, and birth weight are nice information for a birth
announcement, but birth weight is especially important for an obstetrician. A large size at delivery has
long been associated with an increased risk of injuries to a newborn and its mom. So the better a doctor
can predict birth weight, the easier the delivery may be.” Ultrasound is a popular way of doing it. But here as a Data Scientist I am predicting weight of the baby before ultra sound!!!!!!


### Lets Begin: 
Lets predict the new born baby's weight using Linear Regression Implemented from scratch in python !!!!

### Dataset used: 

#### ◦ baby-weights-dataset.csv
▪ It has 131422 rows (samples) with 125 columns (variables). Each sample represent a case for a new-born. It contains 125 variables. Very last
column of it is “BWEIGHT”, that true weight of the new-born (in lbs unit). Actually, this is considered as the target variable.
#### ◦ data-description.txt
▪ We have the name of the 125 variables are actually contracted form of some sort. And, the source of the dataset did not offer me description of every single of them.
But, after studying about them, I could elaborate only few of them. Okay, this file contains few descriptions for the variables. All the rest are
mostly talking about the Mother’s medical history.
##### ◦ judge-without-label.csv
▪ This is an interesting file. It contains new samples: additional 2000 rows with 124 columns (without the BWEIGHT target column). Once again, this should be part of the
training, as there are no ground truth target labels, right? Once the training is complete with the dataset provided above, we apply your prediction algorithm to predict
BWEIGHT of these 2000 samples and show results.


