# Credit_Risk_Analysis
___________________________________________
## Overview/Purpose
___________________________________________
## Results:

  ### Naive Random Oversampling
  - Balanced Accuracy Score: 0.631
  - Precision Score (high-risk, low-risk): 0.01, 1.00
  - Recall Score (high-risk, low-risk):    0.57, 0.69

![naive_over](/images/naive_over.png)

  ### SMOTE Oversampling
  - Balanced Accuracy Score: 0.627
  - Precision Score (high-risk, low-risk): 0.01, 1.00
  - Recall Score (high-risk, low-risk):    0.61, 0.64
 
![SMOTE_over](/images/SMOTE_over.png)

  ### Cluster Centroids Undersampling
  - Balanced Accuracy Score: 0.530
  - Precision Score (high-risk, low-risk): 0.01, 1.00
  - Recall Score (high-risk, low-risk):    0.61, 0.45
  
![clust_cent_under](/images/clust_cent_under.png)

  ### SMOTEENN Combination Sampling
  - Balanced Accuracy Score: 0.635
  - Precision Score (high-risk, low-risk): 0.01, 1.00
  - Recall Score (high-risk, low-risk):    0.71, 0.56
  
![SMOTEENN](/images/SMOTEENN.png)

  ### Ensemble - Balanced Random Forest Classifier
  - Balanced Accuracy Score: 0.788
  - Precision Score (high-risk, low-risk): 0.04, 1.00
  - Recall Score (high-risk, low-risk):    0.67, 0.91
  
![balancedRF](/images/balancedRF.png)

![sorted_featuresRF](/images/sorted_featuresRF.png)

  ### Ensemble - Easy Ensemble AdaBoost Classifier
  - Balanced Accuracy Score: 0.925
  - Precision Score (high-risk, low-risk): 0.07, 1.00
  - Recall Score (high-risk, low-risk):    0.91, 0.94
  
![easy_ensemble](/images/easy_ensemble.png)
___________________________________________
## Summary
