# Sampling Assignment

## Model Performance Comparison with Sampling Techniques

This table summarizes the performance of various machine learning models under different sampling techniques. The performance metric used is accuracy.

| Model                 | Simple Random | Systematic   | Stratified   | Cluster      | Cross-Validation |
|-----------------------|---------------|--------------|--------------|--------------|------------------|
| Logistic Regression   | 0.9348       | 0.8152       | 0.8804       | 0.9565       | 0.9227           |
| Decision Tree         | 0.9457       | 0.8913       | 0.9565       | 0.9457       | 0.9738           |
| Random Forest         | 0.9783       | 0.9565       | 0.9891       | 0.9891       | 0.9954           |
| SVM                   | 0.6413       | 0.6304       | 0.7174       | 0.8261       | 0.6749           |
| KNN                   | 0.6848       | 0.6848       | 0.6522       | 0.8587       | 0.8552           |

## Discussion

The results of this experiment provide valuable insights into how different sampling techniques affect the accuracy of various machine learning models. The five sampling techniques tested—Simple Random, Stratified, Systematic, Cluster, and Cross-validation—were applied across five different models: Random Forest, SVM (Support Vector Machine), Decision Tree, Logistic Regression, and KNN (K-Nearest Neighbors). Here’s a detailed discussion based on the observed results:

### 1.Random Forest exhibited the maximum accuracy across all sampling techniques.

Random Forest is an ensemble method that combines multiple decision trees to improve performance. This model is robust to variations in the data distribution and is less prone to overfitting, which makes it highly adaptable to different sampling strategies. Whether using simple random sampling or cross-validation, Random Forest's ensemble nature helps capture the underlying patterns effectively.

### 2.Decision Tree consistently ranked second across all sampling techniques, except in Cluster sampling, where it was close to third.

Decision Trees are relatively stable and do not require much preprocessing. They perform well with most sampling techniques due to their ability to split data based on feature values. In the case of Cluster sampling, the results might slightly degrade because the inherent structure of clusters might not align well with the decision boundaries that the tree learns, causing it to perform slightly worse than Random Forest.

### 3.Logistic Regression ranked third across all sampling techniques, except in Cluster sampling, where it ranked second.

Logistic Regression is a linear model, meaning it assumes a linear relationship between input features and the target variable. While it performs well with Stratified sampling (which preserves the class distribution), its linear nature makes it less adaptable to complex data structures, as seen in non-stratified sampling methods. However, in Cluster sampling, Logistic Regression may benefit from the more homogeneous groups formed by clusters, leading to better performance in this specific case.

### 4.KNN ranked fourth across all sampling techniques, except in Stratified sampling, where it ranked fifth.

KNN is a distance-based model that relies on local data points for classification. It tends to struggle when the data is not evenly distributed, as it can easily be influenced by outliers or sparse regions of the feature space. Stratified sampling, which ensures that class distributions are balanced, allows KNN to make better decisions, as it avoids being dominated by underrepresented classes. In cases where the data distribution is not balanced (like with Simple Random or Systematic sampling), KNN struggles the most.

### 5.SVM showed the worst performance in all cases except for Stratified sampling, where it ranked 4th.

SVM is highly sensitive to the choice of data distribution, particularly when classes are imbalanced. In cases where data is not evenly distributed across classes (such as with Simple Random, Systematic, and Cluster sampling), SVM's performance can degrade significantly. Stratified sampling, however, ensures that each class is represented proportionally, which helps the SVM maintain a balanced decision boundary and improve accuracy.

## Conclusion

In summary, Random Forest consistently provides the highest accuracy across all sampling techniques, followed by Decision Tree and Logistic Regression. SVM and KNN perform less effectively, with SVM being particularly sensitive to imbalanced data, while KNN faces challenges with data sparsity and outliers.

### Best Sampling Technique for Each Model:                     
#### Logistic Regression: Cluster with Accuracy = 0.96
#### Decision Tree: Cluster with Accuracy = 0.98
#### Random Forest: Cross-Validation with Accuracy = 1.00
#### SVM: Cluster with Accuracy = 0.98
#### KNN: Cluster with Accuracy = 0.98
