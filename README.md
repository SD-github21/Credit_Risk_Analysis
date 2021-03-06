# Credit Risk Analysis

The purpose of the Credit Risk analysis was to apply machine learning towards predicting credit card risk. Machine learning techniques were employed to both train and evaluate the performance of six different models in order to discover the model that yielded the best metrics in identifying, classifying, and predicting high-risk applicants. The balanced accuracy score, precision, and sensitity/recall were examined and utilized to determine how each model fared against the others. 

## Resources
- Data Sources: LoanStats_2019Q1.csv 
- Software: Jupyter Notebook, Python, imbalanced-learn, scikit-learn

## Results

**(1) Random Oversampler Model**
  - The Random Oversampler model yielded a balanced accuracy score of 0.661, which means it is 66.1% accurate in predicting risk (whether low-risk or high-risk) for credit loans. 
  ![image](https://user-images.githubusercontent.com/85533099/145699918-ef68a3e1-3458-4bde-9e1a-6e1a7d71de7d.png)
  
  - The results indicate a precision score of 0.01, which is extremely low and indicates that the model demonstrated a poor level of precision with regards to how reliable it was in correctly classifying those loans that were high-risk. The model exhibited a sensitivity/recall score of 0.72, which indicates that the model seemed to do fairly well in predicting which credit loans were high-risk as it’s higher than 0.5. 
  ![image](https://user-images.githubusercontent.com/85533099/145699716-5a7e6a03-6c2d-46e4-9fe9-3e805b6f5add.png)

--------------------------------------------------------------------------------------------------------------------------------------

**(2) SMOTE Oversampling Model**
  - The SMOTE Oversampling model yielded a balanced accuracy score of 0.658, which means it is 65.8% accurate in predicting risk (whether low-risk or high-risk) for credit loans. 
  ![image](https://user-images.githubusercontent.com/85533099/145699952-4d941100-9d29-4a92-b0b6-ca000842acb1.png)


  - Similar to the above Random Oversampler model, the results indicate a precision score of 0.01, which is extremely low  and indicates that the model demonstrated a poor level of precision with regards to how reliable it was in correctly classifying those loans that were high-risk. This model exhibited a sensitivity/recall score of 0.62, which indicates that the model was fair in its ability to predict which credit loans were high-risk, as it’s higher than 0.5 but not substantially.
  ![image](https://user-images.githubusercontent.com/85533099/145699742-eb6f84a8-0732-4b1c-8a93-1e9cec702af0.png)

--------------------------------------------------------------------------------------------------------------------------------------

**(3) Cluster Centroids Undersampling Model**
  - The Cluster Centroids Undersampling model yielded a balanced accuracy score of 0.544, which means it is 54.4% accurate in predicting risk (whether low-risk or high-risk) for credit loans. 
  ![image](https://user-images.githubusercontent.com/85533099/145699970-2871052e-d576-46f7-97e0-7e00b1cd819c.png)
   
  - Similar to the above oversampling models, the results indicate a precision score of 0.01, which is extremely low  and indicates that the model demonstrated a poor level of precision with regards to how reliable it was in correctly classifying those loans that were high-risk. This model exhibited a sensitivity/recall score of 0.69, which indicates that the model seemed to do fairly well in its ability to predict which credit loans were high-risk, as it’s higher than 0.5.
  ![image](https://user-images.githubusercontent.com/85533099/145699777-801d83f7-7887-43c3-bb77-c56a692aa0fb.png)

--------------------------------------------------------------------------------------------------------------------------------------

**(4) SMOTEENN Model - Combination of Oversampling and Undersampling**
  - The SMOTEENN model yielded a balanced accuracy score of 0.645, which means it is 64.5% accurate in predicting risk (whether low-risk or high-risk) for credit loans. 
  ![image](https://user-images.githubusercontent.com/85533099/145699983-4d22cb8c-2596-49ab-82e0-858a684c5dde.png)

  - Similar to the above oversampling and undersampling models, the results indicate a precision score of 0.01, which is extremely low and indicates that the model demonstrated a poor level of precision with regards to how reliable it was in correctly classifying those loans that were high-risk. This model exhibited a sensitivity/recall score of 0.72, which indicates that the model seemed to do fairly well in its ability to predict which credit loans were high-risk, as it’s higher than 0.5.
  ![image](https://user-images.githubusercontent.com/85533099/145699837-b5756c52-aa6e-4b0a-8ba7-2cd7099bc03c.png)

--------------------------------------------------------------------------------------------------------------------------------------

**(5) Balanced Random Forest Classifier**
  - The Balanced Random Forest Classifier model yielded a balanced accuracy score of 0.789, which means it is 78.9% accurate in predicting risk (whether low-risk or high-risk) for credit loans. 
  ![image](https://user-images.githubusercontent.com/85533099/145699994-c3d2d637-639b-490f-a89a-14e65af509e8.png)

  - Similar to the above resampling models, the results indicate a precision score of 0.03, which is extremely low  and indicates that the model demonstrated a poor level of precision with regards to how reliable it was in correctly classifying those loans that were high-risk. This model exhibited a sensitivity/recall score of 0.70, which indicates that the model was fair in its ability to predict which credit loans were high-risk, as it’s higher than 0.5.
  ![image](https://user-images.githubusercontent.com/85533099/145699861-dbe0a75f-634f-430e-88c8-60ef09c815ac.png)

--------------------------------------------------------------------------------------------------------------------------------------

**(6) Easy Ensemble AdaBoost Classifier**
  - The Easy Ensemble AdaBoost Classifier model yielded a balanced accuracy score of 0.932, which means it is 93.2% accurate in predicting risk (whether low-risk or high-risk) for credit loans. 
  ![image](https://user-images.githubusercontent.com/85533099/145700003-e6f79e63-3531-4a2f-84b9-7658873c2c66.png)

  - Similar to the above resampling and ensemble classifier models, the results indicate a precision score of 0.09, which is extremely low and indicates that the model demonstrated a poor level of precision with regards to how reliable it was in correctly classifying those loans that were high-risk. This model exhibited a sensitivity/recall score of 0.92, which indicates that the model performed extremely well in its ability to predict which credit loans were high-risk, as it’s substantially higher than 0.5.
  ![image](https://user-images.githubusercontent.com/85533099/145699896-93c0e170-6049-449a-95ac-93fb7f16933a.png)

--------------------------------------------------------------------------------------------------------------------------------------

## Summary
As the results indicate, the balanced accuracy scores ranged from 54.4% to 93.2%, indicating average to high accuracy. All six of the models demonstrated poor precision, as evidenced by scores ranging from 0.01 to 0.09 and moderate to high sensitivity/recall ranging from 0.62 to 0.92. In evaluating all of the models, the Easy Ensemble AdaBoost Classifier model yielded the best classification report with a precision score of 0.09, a high sensitivity/recall score of 0.92 and a balanced accuracy score of 93.2%. Sensitivity/recall would likely be the most important metric in this context as we would want to be able to accurately predict those loan applications that are high-risk in order to avoid scenarios where individuals were granted loans but later defaulted on those loans. However, even still, it is recommended that none of the models be used for predicting credit risk because of the extremely poor precision rates across all models. We would ideally want to find a model where precision rate was at least within reasonable bounds even if it were lower than the sensitivity/recall rate and scores of less than 0.1 seem negligible. One potential avenue of exploration would be to reduce the number of features included in the models and re-evaluate their performance to determine if a more suitable result is obtained for precision.   
