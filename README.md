# credit-risk-classification
Overview of the Analysis
In this credit risk classification analysis, cutting-edge machine learning techniques were harnessed to scrutinize an extensive historical dataset from a peer-to-peer lending services company. The aim was to construct a robust model capable of astutely discerning the creditworthiness of borrowers.

Analysis Overview: The analysis delved into a multitude of factors, encompassing:

Loan size
Interest rate
Borrower's income
Debt-to-income ratio
Number of borrower's accounts
Incidence of derogatory marks
Total debt
Dataset Handling: The dataset, containing a substantial 77,536 data points, was judiciously partitioned into training and testing subsets. The training set facilitated the creation of an initial logistic regression model, aptly designated as Logistic Regression Model 1. This model, fashioned employing the scikit-learn LogisticRegression module, was subsequently applied to the testing data to discern the risk level (low or high) of loans extended to borrowers in this subset.

The original dataset exhibited a notable class imbalance with 75,036 instances of low-risk loans and merely 2,500 instances of high-risk loans. To ameliorate this imbalance, the training data underwent a resampling procedure using the RandomOverSampler module from the imbalanced-learn library. This procedure generated an augmented dataset containing 56,277 data points for both low-risk (0) and high-risk (1) loans, maintaining fidelity to the original dataset's composition.

Model Refinement: Leveraging the resampled dataset, a refined logistic regression model, denoted as Logistic Regression Model 2, was meticulously constructed. This model aimed to accurately predict the risk classification (low or high) of loans in the testing set.

Results
Quantitative Insights:

Logistic Regression Model 1:

Precision: 93% (averaging 100% precision for low-risk loans and 87% precision for high-risk loans)
Accuracy: 94%
Recall: 95% (averaging 100% recall for low-risk loans and 89% recall for high-risk loans)
Logistic Regression Model 2:

Precision: 93% (averaging 100% precision for low-risk loans and 87% precision for high-risk loans)
Accuracy: 100%
Recall: 100% (for both low-risk and high-risk loans)
Summary
While Logistic Regression Model 2 displays a heightened ability to evade false negatives (undetected high-risk loans), a nuanced evaluation of confusion matrices exposes a slightly elevated rate of false positives (low-risk loans inaccurately classified as high-risk loans).

Given the overarching goal of the model to gauge the probability of high-risk loans, it is discernible that neither model surpasses the 90% precision threshold for high-risk predictions. Notwithstanding, Logistic Regression Model 2, endowed with fewer erroneous predictions across the testing data, emerges as the superior choice. This verdict is substantiated by the model's exceptional accuracy and recall, cementing its stature as the optimal candidate for risk assessment in this credit classification framework.
