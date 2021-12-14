# Credit_Risk_Analysis
## Overview of the project
In this project, we want to see how all the factors in loan_stats csv can help predict whether someone is in a low-risk or high-risk state. One method data scientists use to solve such problems is to create models, and then evaluate and train the models they create. In this particular project, we used unbalanced learning and the scikit-learn library to build models and evaluated them using resampling methods. In the first few models, I used a random oversampler and smote algorithm to oversample the data, and used the clustercentroid algorithm to undersample the data. In the remaining models, I use a combined method to oversample and undersample the data using smoteenn. Finally, I compared two machine learning models that minimize deviations, balancedrandomforestclassifier and easyensembleclassifier.
### Results
* Results of Naive Random Oversampling: The balanced accuracy test is 65%, the precision of the high-risk is only 1% and recall is 62%. 
![image](https://github.com/YutaiLee/Credit_Risk_Analysis/blob/main/images/Random_Oversampling.png)
* Results of SMOTE Oversampling: The balanced accuracy test is 62%, the precision of the high-risk is only 1% and recall is 59%.
![image](https://github.com/YutaiLee/Credit_Risk_Analysis/blob/main/images/SMOTE_Oversampling.png)
* Results of Undersampling: The balanced accuracy score is 62.4% overall, the precision is at 99% and the recall is 66%
![image](https://github.com/YutaiLee/Credit_Risk_Analysis/blob/main/images/Undersampling.png)
* Results of Combination: The balanced accuracy score is 62.4%, the precision is 99% and the recall is 66%
![image](https://github.com/YutaiLee/Credit_Risk_Analysis/blob/main/images/Combination_Sampling.png)
* Results of Balanced Random Forest Classifier: The balanced accuracy score is 78.7%, the precision is 99% and the recall is 91%
![image](https://github.com/YutaiLee/Credit_Risk_Analysis/blob/main/images/Balanced_Random_Forest_Classifier.png)
* Results of Easy Ensemble AdaBoost Classifier: The balanced accuracy score is 92.5%, the precision is 99% and the recall is 94%
![image](https://github.com/YutaiLee/Credit_Risk_Analysis/blob/main/images/Easy_Ensemble_AdaBoost_Classifier.png)
## Summary
In the first four models, we performed under-sampling, over-sampling, and combined the two to try to determine which model can best predict which loans have the highest risk. For the next two models, we use an ensemble classifier to resample the data to try to predict which loans are high-risk or low-risk. In our first four models, our accuracy score is not as high as that of the ensemble classifier, and the recall rate in the oversampling/undersampling/mixed model is also very low. Usually in a model, a good balance between recall and accuracy needs to be struck, which is why I recommend using an ensemble classifier instead of the first four models. It seems that Easy Ensemble has the best balance among all models because it has a high accuracy score and a good balance between accuracy and recall scores.
