# A machine learning model that predicted the anti-S.aureus activity levels of peptides
We used the DBAASP database (https://dbaasp.org/home) to construct a dataset for machine learning. 
Monomeric AMPs without unusual amino acids and bonds were screened out, and they also need to report the minimum inhibitory concentration (MIC) for S. aureus was reported. 
In total, 3,825 AMPs were collected and the labeled as having high activity, low activity, or no activity. 
After BorderlineSMOTE oversampling balanced the samples of each class, we randomly split the dataset into 80% training data and 20% test data. To lower the threshold of use, AutoGluon, which constructs models with a few lines of code, was used to establish the prediction models with 5-fold cross-validation was measured. We tested 18 models, of which WeightedEnsemble_L3 exhibited the best performance. The selected model achieved a receiver operating characteristic curve-area under the curve (ROC-AUC) of 0.87 on the test data. 
Using inactive peptides as an external test set, the prediction accuracy reached 98%. 

PS:The code is completely executed according to AutoGluon's reference case (https://auto.gluon.ai/stable/tutorials/tabular_prediction/index.html), no additional revisions have been conducted.
