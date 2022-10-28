# Credit_Risk_Analysis
___________________________________________
## Overview/Purpose
The purpose of this analysis was to use supervised machine learning on a LendingClub credit card dataset in order to help identify credit card applicants that are considered a high-risk applicant. The prediction of credit risk is very important to lenders because the more accurate they can be, the less often they lend credit that cannot be repaid.  The machine learning models below use various strategies to predict high risk applicants so that the lenders have a tool to use to save time and money, as better performing models will lead to less high risk loans being given to applicants. 
___________________________________________
## Results:

  ### Naive Random Oversampling
  - Balanced Accuracy Score: 0.631
  - Precision Score (high-risk, low-risk): 0.01, 1.00
  - Recall Score (high-risk, low-risk):    0.57, 0.69
  - Overall, this model isn't super accurate (63%). For identifying high risk credit applicants, a higher accuracy score should be achieved in order to make financially sound decisions on loans. The precision score (0.01) and recall score (0.57) were both moderately low, which supports using a different model for this dataset.  

![naive_over](/images/naive_over.png)

  ### SMOTE Oversampling
  - Balanced Accuracy Score: 0.627
  - Precision Score (high-risk, low-risk): 0.01, 1.00
  - Recall Score (high-risk, low-risk):    0.61, 0.64
  - This SMOTE model performed very similar to the first model.  The accuracy score was not very high (63%) and the precision and recall scores are low for the finances that are on the line with these credit loans. 
  
![SMOTE_over](/images/SMOTE_over.png)

  ### Cluster Centroids Undersampling
  - Balanced Accuracy Score: 0.530
  - Precision Score (high-risk, low-risk): 0.01, 1.00
  - Recall Score (high-risk, low-risk):    0.61, 0.45
  - This Cluster Centroids Undersampling model seemed to perform the worst out of the models tested so far.  It has the lowest accuracy score of 53% and the precision score and recall score of identifying the high risk applicants are both very low. I do not recommend using this model for the given dataset. 
  
![clust_cent_under](/images/clust_cent_under.png)

  ### SMOTEENN Combination Sampling
  - Balanced Accuracy Score: 0.635
  - Precision Score (high-risk, low-risk): 0.01, 1.00
  - Recall Score (high-risk, low-risk):    0.71, 0.56
  - This model shows a slightly better accuracy (64%) than the previous 3 models, but it still is not performing as well as one would hope. It has a low precision score (0.01) and an average recall score (0.71) for identifying the high risk applicants. The model has a slight edge on the others thus far, but it does have quite a few flaws. 
 
![SMOTEENN](/images/SMOTEENN.png)

  ### Ensemble - Balanced Random Forest Classifier
  - Balanced Accuracy Score: 0.788
  - Precision Score (high-risk, low-risk): 0.04, 1.00
  - Recall Score (high-risk, low-risk):    0.67, 0.91
  - This Balanced Random Forest Classifier model performed much better than the previous models. The accuracy is much higher with this model, at 78%. This model is the most accurate so far, and it also has the highest precision score for high risk applicants so far. The recall score (0.67) could be much higher, as this is a major issue with the model. All in all, this model is fairly strong compared to the previous ones used, but should be more specific to prevent so many false positives. 
 
![balancedRF](/images/balancedRF.png)

![sorted_featuresRF](/images/sorted_featuresRF.png)

  ### Ensemble - Easy Ensemble AdaBoost Classifier
  - Balanced Accuracy Score: 0.925
  - Precision Score (high-risk, low-risk): 0.07, 1.00
  - Recall Score (high-risk, low-risk):    0.91, 0.94
  - This is the best model by far. It is accurate at a rate of 93% and has the highest precision and recall scores for identifying high risk applicants by a longshot over the other models. It has a few flaws, but it would still make the best predicions for the job. 
  
![easy_ensemble](/images/easy_ensemble.png)
___________________________________________
## Summary
All in all, the 4 models that involved over-, under-, and combination sampling of the dataset all had a low accuracy (all below 0.635). The 2 ensemble classifier models were much more accurate, but the Easy Ensemble AdaBoost Classifier was the best model due to accuracy and also having the highest precision score and recall score for identifying the high risk applicants. 

The model that I would recommend is the Easy Ensemble AdaBoost Classifier.  This model has the highest accuracy score (0.925) and also has the highest precision and recall for the high credit risk applicants (0.07, 0.91).  It is important to note though that this model does predict a lot of high risk applicants that are actually low risk.  This is due to the small subset of high risk applicants in the data. Even though the model predicts a lot of high risk applicants, it is better than the other way around. If the model were to predict more low risk applicants than true, there would be high risk applicants receiving credit loans that might be riskier than they realize. 
