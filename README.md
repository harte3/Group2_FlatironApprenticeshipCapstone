# Group 2 Apprenticeship Capstone

## Link to dataset: https://github.com/harte3/Group2_FlatironApprenticeshipCapstone/blob/main/healthcare-dataset-stroke-data.csv

## Link to presentation: https://github.com/harte3/Group2_FlatironApprenticeshipCapstone/blob/main/Capstone_Presentation.pdf

## Link to notebook: https://github.com/harte3/Group2_FlatironApprenticeshipCapstone/blob/main/Final%20Notebook.ipynb


## Introduction

The team came up with the business problem after coming across a dataset on pateints admitted to a hospital for a suspected stroke. For many of these incidents, it is a first time occurence, so making patients aware of the factors that possibly put them at risk is important. With that being said, not all individuals have easy access to healthcare, therefore implementing a federal program to bring awareness to those who may have a higher risk can benefit indivudals regardless of their insurance or financial status. The product idea we came up with is a machine learning model that can identify whether or not patients in this dataset had a stroke or not, and of those people that are stroke positive, what factors do they have in common. We ran several types of models and decided that logistic regression best suited our business problem and analyses.



## Business Problem

This model can be marketed towards federal health organizations such as Medicaid or public hospitals to reach out to their communities. These organizations can conduct outreach programs using the outcomes from this data model to inform the public and instruct those identified as high risk to ensure they are getting regular checkups and are aware of the warning signs. In the US, many of these public health programs are underfunded and have limited availability, such as waitlists for appointments, so having a product that can inform patients is essential for public health.



## Data Set

Our dataset is from Kaggle, a public, open-source site, and includes patients admitted to the hospital for a possible stroke. The factors include gender, age, hypertension, BMI, heart disease, occupation, residence type, average glucose level, and smoking status. Our target variable is whether or not the patient had a stroke (0 or 1).



## Navigating the Repo

To fork the repo, select fork in the top right corner and fill out the desired fields such as name and description (optional), then hit create fork. This allows you to clone a local copy to conduct your own work on the notebook.

Upon opening the repo you will find the main branch. By selecting the branch drop down in the top left, you can navigate to the other members branches. Each branch other than the main has its own notebook that the pair worked on, located in a folder titled 'notebooks', as well as another folder labeled 'plots' containing images of each plot included in the notebook. The main contains a notebook that is compilation of all the members notes, as well as a pdf copy of the presentation and a csv containing the dataset.



## Exploring and Preparing the Data

The notebook begins with the importing of all the libraries necessary for creating our models and is followed by reading and viewing the dataset using Pandas and dropping an irrelevant column. Next we created a heatmap to view the correlations between the variables. Next we viewed the distribution of ages of the patients as well as comparing different factors against each other in relation to stroke outcome. We also split the data up into ranges and added it as a new column to assist with readability. We viewed the data types and decidided we had to one hot encode in order to create our models.We then split the data into testing and training as well as set up a grid search with KNN Imputer. Lastly we checked for multicollinearity to ensure our models perform without being too skewed towards a specific factor.



## Modeling

Since our data requires us to use binary classification, we used the following models, Logistic regression, K Nearest Neighbor classifier, Decision Tree Classifier, Random Forest Classifier, XGBoost, Support vector machine (SVM). We decided linear regression was the best for out data based on its scores. We also conducted feature importance to see which factors contributed the most to stroke positivity, which was age, specifically 61 and up. 



## Outcomes and Visualizations

We plotted a confusion matrix to display scores and included a bar chart that compared training accuracy, validation accuracy, and recall percentage of each model, further showing how linear regression outperformed the rest. ROC Curve and precision-recall further display model performance. We also created a decision tree which shows the disparity in gender, showing men to be at a much higher risk.



## Evaluation

We wanted to test other ways we could imrpove accuracy, one way being by implementing class weights and setting a desired recall. Class weights ensure that outliers don't throw off the model performance too much. For recall, the higher the threshold, the greater probability of possibly reducing false positives. However, if too high this can result in missing some true positives. Alternatively, too low of a threshold can result in more predicted positives and increase the odds of a false positive. At 80% and 90%, the results don't seem to change. 



## Conclusion

We decided logistic regression best suited our model and the factors that had the greatest impact on whether or not a patient had a stroke were age and hypertension, which is suprising as we inferenced that smoking status and BMI would hold more weight in the outcome. With that being said, hypertension should be taken seriously especially in conjunction with age over 60.






