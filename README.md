# --- Prediction-of-Cancer-Types-using-Gene-Expession ---
This project aims to classify cancer types using gene expression data. The following libraries are used:

- pandas
- numpy
- matplotlib
- seaborn
- sklearn
- yellowbrick

# PROBLEM STATEMENT ---

Cancer has become one of the major factors responsible for global deaths, due to late diagnoses and lack of proper treatment. It involves the abnormal and uncontrolled growth of cells inside the body, which might spread from one place to different parts. Ribonucleic acid (RNA) sequencing can detect the changes occurring inside cells and helps to analyze the transcriptome of gene expression patterns inside RNA. Machine learning techniques can assist in the prediction of cancer at an early stage, if data is available. 

## Objectives
The objective for this project is to build models and classify the different cancer types using RNA-seq gene expression data. For this purpose we implemented supervised models to classify the samples collected using the labels and compare the performance of the respective models.

## Data Description
The dataset was collected from UCI Machine Learning Repository. The rows represent the observations gene expressions of patients having different types of tumors (cancer types). The last column contains the cancer types as listed below:
- BRCA for Breast Cancer
- KIRC for Renal Cancer (Kidney Renal Clear Cell Carcinoma)
- LUAD for Lung Cancer (Lung adenocarcinoma)
- PRAD for Prostate Cancer (Prostate adenocarcinoma)
- COAD fro Colon adenocarcinoma

# Data Exploration

The first step is to import and explore the data. It was checked for missing values and analysis of the distribution of the data. Class imbalance was also checked. I noticed that although most of the columns had their mean around 0, the standard deviation of the various columns were around 0.5. Since it is required the standard deviation be 1 for normally distributed data, I concluded that the data needed to be preprocessed with a scaler before building models. This would normalize the data and improve the effectiveness of the models.

Next, I checked the counts of the different cancer types that were in the data. I noted that there were 5 classes/cancer types. Although the count of BRCA was quite high, it didn't indicate an imbalance that would throw off the effectiveness of the machine learning models. I plotted a bar chart to display the class distribution.

With the data exploration complete, I began the preprocessing of the data. I first separated the data into features and a target variable after which the classes were encoded as numeric type.
  
The labels for this data were categorical and therefore had to be converted to numeric forms, this is referred to as encoding. Machine learning models usually require input data to be in numeric forms, so I encoded the labels.

With the data encoded and ready for analysis, I split the data into training and test subsets. The training data was initially passed to the machine learning model during fitting. This enabled the model to identify patterns which can be used to make future predictions. I used the testing data to evaluate the performance of the model.

With all the tools and data in place, I set out to train and evaluate powerful machine learning models using Random Forest Classifier, pipelines, randomized search CV, PCA, ROCAUC, and performance metrics such as F1 score, precision score, recall score, classification report, confusion matrix, and ROC curve. Based on the f1 scores of the various models, the top two models are LogisticRegression(logregpipe) with f1_score of 1.0 and XGBoost(xgbpipe) with f1 score of 0.993817
XGBoost is however closely followed by SVC(svcpipe)

The journey was long and challenging, but in the end, I was able to classify the cancer types with high accuracy and precision, thus saving many lives and making the world a better place.

# Conclusion
We were able to classify the cancer types with high accuracy and precision, thus helping in early diagnosis and saving many lives.

# Note
The knowledge cut off is 2021, so the libraries and techniques may have newer version.
