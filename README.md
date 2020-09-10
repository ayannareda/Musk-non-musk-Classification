# Musk-non-musk-Classification
The goal is to learn to predict whether new molecules will be musks or non-musks. However, the 166 features that describe these molecules depend upon the exact shape, or conformation, of the molecule. Because bonds can rotate, a single molecule can adopt many different shapes. To generate this data set, all the low-energy conformations of the molecules were generated to produce 6,598 conformations. Then, a feature vector was extracted that describes each conformation.<br />

The Dataset used here here containsa set of 102 molecules of which 39 are judged by human experts to be musks and the remaining 63 molecules are judged to be non-musks.<br />

Many-to-one relationship between feature vectors and molecules is called the "multiple instance problem". When learning a classifier for this data, the classifier should classify a molecule as "musk" if ANY of its conformations is classified as a musk. A molecule should be classified as "non-musk" if NONE of its conformations is classified as a musk.<br />

The dataset can be downloaded from https://www.kaggle.com/hashbanger/musk-dataset <br /><br />

In this project we first Load the dataset. <br /><br />

After that we apply pre-processing.<br />
Remove entry which have missing value in it.<br />
Remove columns which have correlation higher than 92%.<br /><br />

Then we split our dataset in Train and Test part. (80:20 )<br />
Then we split our fetures and labels for our data.<br /><br />

Then, we build a keras model.<br /><br />

Compile the model:-<br />
Loss = binary_crossentropy<br />
Optimizer = Adam<br /><br />

Then, we train our model on our splitted dataset.<br /><br />

After the training is done, we plot Accuracy and Loss of our model.<br />
The results are shown below :-<br />
<img src="https://github.com/gearhead0909/Musk-non-musk-Classification/blob/master/Accuracy.png" alt="alt text" width="500" height="300"><br />
<img src="https://github.com/gearhead0909/Musk-non-musk-Classification/blob/master/Loss.png" alt="alt text" width="500" height="300"><br /><br />

Accuracy of our model:-<br />
f1_score: 0.921951219512195<br />
recall: 0.9264705882352942<br />
Validation Loss: 0.06954377144575119<br />
Validation Accuracy: 0.9757575988769531<br /><br />

Save the model
