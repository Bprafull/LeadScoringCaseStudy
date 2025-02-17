# LeadScoringCaseStudy

## Details of files present in this project
1. lead_scoring_case_study.ipynb - Jupyter notebook included all the detailed data analysis
2. PPT_Lead_Scoring_Project.pdf - PPT pdf file
3. Summary_file.pdf - Summary pdf file
4. Assignment Subjective Questions.docx - Subjective Questions file

## Solution Steps Followed

1. Reading and Cleaning Data
2. EDA
3. Dummy Variables
4. Test-Train Split
5. Model Building
6. Making Prediction
7. Model Evaluation
8. Optimise Cut off (ROC Curve)
9. Prediction on Test set
10. Precision- Recall

## Goals of the Case Study
Build a logistic regression model to assign a lead score between 0 and 100 to each of the leads which can be used by the company to target potential leads. A higher score would mean that the lead is hot, i.e. is most likely to convert whereas a lower score would mean that the lead is cold and will mostly not get converted. There are some more problems presented by the company which your model should be able to adjust to if the company's requirement changes in the future so you will need to handle these as well.


## Summary
 
 Step1: Reading and Understanding Data. Read and analyses the data.  
 
• Step2: Data Cleaning:  We dropped the variables that had high percentage of NULL 
values in them. This step also included imputing the missing values as and where 
required with median values in case of numerical variables and creation of new 
classification variables in case of categorical variables. The outliers were identified 
and removed.    

• Step3: Data Analysis Then we started with the Exploratory Data Analysis of the data 
set to get a feel of how the data is oriented.  

• Step4: Creating Dummy Variables, we went on with creating dummy data for the 
categorical variables.

• Step5: Test Train Split:  The next step was to divide the data set into test and train 
sections with a proportion of 70-30% values.

• Step6: Feature Rescaling We used the Min Max Scaling to scale the original numerical 
variables. Then using the stats model we created our initial model, which would give 
us a complete statistical view of all the parameters of our model.  

• Step7: Feature selection using RFE:  Using the Recursive Feature Elimination we went 
ahead and selected the 15 top important features. Using the statistics generated, we 
recursively tried looking at the P-values in order to select the most significant values 
that should be present and dropped the insignificant values. 

• Finally, we arrived at the 11 most significant variables. The VIF’s for these variables 
were also found to be good. We then created the data frame having the converted 
probability values and we had an initial assumption that a probability value of more 
than 0.5 means 1 else 0. Based on the above assumption, we derived the Confusion 
Metrics and calculated the overall Accuracy of the model. We also calculated the 
‘Sensitivity’ and the ‘Specificity’ matrices to understand how reliable the model is. 

• Step8: Plotting the ROC Curve We then tried plotting the ROC curve for the features 
and the curve came out be pretty decent with an area coverage of 88% which further 
solidified the of the model.  

• Step9: Finding the Optimal Cutoff Point Then we plotted the probability graph for the 
‘Accuracy’, ‘Sensitivity’, and ‘Specificity’ for different probability values. The 
intersecting point of the graphs was considered as the optimal probability cutoff 
point. The cutoff point was found out to be 0.35 Based on the new value we could 
observe that close to 80% values were rightly predicted by the model. We could also 
observe the new values of the ‘accuracy=81%, ‘sensitivity=80%’, ’specificity=81%’. 
Also calculated the lead score and figured that the final predicted variables 
approximately gave a target lead prediction of 80%.
