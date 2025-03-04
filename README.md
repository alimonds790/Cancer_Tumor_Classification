# Cancer Tumor Classification

## Brief Problem Statement:
This project aims to develop a classification model that accurately distinguishes between malignant and benign tumours using the UCI Breast Cancer Wisconsin (Diagnostic) dataset. This dataset contains features computed from fine needle aspirate images of breast masses. By leveraging these features, the model aims to support early and reliable breast cancer diagnosis, ultimately improving patient outcomes through timely treatment.



## Dataset: 
name: Breast Cancer Wisconsin (Diagnostic)  
data_url: https://archive.ics.uci.edu/static/public/17/data.csv  
abstract: Diagnostic Wisconsin Breast Cancer Database.  
area: Health and Medicine  
characteristics: ['Multivariate']  
num_instances: 569  
num_features: 30  

Features are computed from a digitized image of a fine needle aspirate (FNA) of a breast mass.  They describe the characteristics of the cell nuclei present in the image.  
the data inspects 1-4 features for each cell over 1-3 separating planes.


### Learnings and Takeaways
1. Handling Multicollinearity
We observed high multicollinearity between the radius, perimeter, and area features. This makes sense because the perimeter is a linear transformation of the radius, and the area is a quadratic transformation of the radius. To address this, we decided to drop the perimeter and area features and keep the radius. This step helped in reducing multicollinearity, leading to more stable and interpretable models.

2. Model Evaluation Metrics
Choosing the right evaluation metrics is crucial for assessing model performance. For cancer detection, recall (sensitivity) and F1 score are particularly important. Recall ensures that most actual cancer cases are detected, minimizing false negatives. The F1 score provides a balance between precision and recall, which is useful when both false positives and false negatives are important. In our project, focusing on these metrics helped us better understand the trade-offs and effectiveness of our models.

## Potential Improvement
- **Hyperparameter Tuning**: While we performed some hyperparameter tuning using GridSearchCV, further tuning with a more extensive parameter grid or using techniques like RandomizedSearchCV could potentially improve model performance.
- **Feature Engineering**: Additional feature engineering, such as creating interaction terms or polynomial features, could help capture more complex relationships in the data and improve model accuracy, but might require some domain Knowledge.
- **Ensemble Methods**: Exploring other ensemble methods, such as Gradient Boosting Machines (GBM) or stacking multiple models, could enhance the robustness and accuracy of our predictions.
- **Using Multiple Models and comparing results**
     


## Guide:

1. Download repo
2. Install any requirements from the 'requirements.txt' file that you might have missing or not up to date
3. Run notebook

## References:

1. Wolberg, W., Mangasarian, O., Street, N., & Street, W. (1993). Breast Cancer Wisconsin (Diagnostic) [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5DW2B.
2. Koehrsen, W. (2019, December 10). Hyperparameter Tuning the random Forest in Python - TDS Archive - Medium. Medium. https://medium.com/towards-data-science/hyperparameter-tuning-the-random-forest-in-python-using-scikit-learn-28d2aa77dd74
