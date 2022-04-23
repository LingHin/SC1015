# SC1015 Mini Project: Medical Condition Predictor

## About

Our team's main objective was to employ machine learning models to make processing of raw medical data easier for medical personnel, by determining the relationship between 
medical conditions and presence of diseases in patients.

The dataset we have chosen was taken from Kaggle, titled [Hospital Mortality Analysis](https://www.kaggle.com/code/yashgupta24/hospital-moratality-analysis/notebook).

For a more detailed walkthrough of our project, please view our source codes in the following order:

1. Data Splitting and Data Imputation
2. Data Visualisation
3. RandomForest Model
4. Resampling and Other Models

## Contributors

- Aloysius Ng (@metalalloy) : Motivation/Problem Statement, Exploratory Data Analysis
- Lim Wei Jun, Wilson (@GodofGaren1) : Cleaning up of Data Set, MissForest, RandomForest
- Lau Ling Hin (@LingHin) : GridSearch, Observations, Upsampling
- Ng I-Shen Samuel (@samuel1234ng) : Results of re-test, Logistic Regression, Lessons Learnt

(Contributions include respective slides, script and code where applicable)

## Problem Definition

- Do any of the medical factors have correlation with any diseases?
- What models can we use to best predict this relationship?

## Variable List
- <list variable name(s), description(s), unit(s)and value labels as appropriate for each>
group；ID；outcome；age（years）；gendera；BMI；hypertensive；atrialfibrillation；CHD with no MI；diabetes；deficiencyanemias；depression；Hyperlipemia；
Renal failure；COPD；heart rate（bpm）；
Systolic blood pressure（mmHg）；Diastolic blood pressure（mmHg）；Respiratory rate（bpm）；temperature（℃）；SP O2（%）；Urine output（ml）；hematocrit（%）；
RB（m/uL）;MCH(pg);MCHC(%);MCV(fL);RDW(%);Leucocyte(K/uL);Platelets(K/uL);Neutrophils(%);Basophils(%);Lymphocyte(%);PT(Seconds);INR;NT-proBNP(pg/mL);
Creatine kinase(IU/L);Creatinine(mg/dL);Urea nitrogen(mg/dL);glucose(mEq/L);Blood potassium(mEq/L);
Blood sodium(mEq/L);Blood calcium(mg/dL);Chloride(mEq/L);Anion gap(mEq/L);Magnesium ion(mg/dL);PH;Bicarbonate(mEq/L);Lactic acid(mmol/L);PCO2(mmHg);EF(%)

## Models Used

- 1. Logistic Regression
- 2. Decision Tree
- 3. MissForest
- 4. RandomForest

## Conclusion

- Even though each variables have low correlation values with the diseases, but using all variables to train the machine learning models can return pretty good results
- When comparing the RandomForest model before and after upsampling, we noticed that the True Positive and True Negative Rate only improved marginally for the imbalance data we resampled (CHD), but for the data that the already relatively balanced (Renal Failure), the True Positive and True Negative Rate remains relatively unchanged.
- Resampling does help improve the results when the data set is very imbalance, but resampling will not help in improving the machine learning model much if the variables already have very little correlation
- Different diseases can have different Machine Learning Models that performs better. (Logistic Regression for CHD and Random Forest for Renal Failure)
- RandomForest with GridSearch helps are able to predict the chances of someone having Renal failure with 78% accuracy.
- The 5 most important factors in predicting Renal failure are creatine, heart rate, PT(prothrombin time), Bicarbornate and Platelets.
- Other diseases do have correlations with the medical factors, but their prediction accuracy using machine learning model are not as high as that of Renal failure.

## Lessons learnt

- MissForest is a good method for filling in NA values to ensure consistency in the dataset
- Logistic Regression from sklearn
- RandomForest from sklearn
- Resampling improve imbalanced data to obtain better results for machine learning models, but may not always be effective
- Learn how to obtain feature importance from RandomForest and LinearRegression.
- Learning how to use Github repositories

## References

- https://www.kaggle.com/code/yashgupta24/hospital-moratality-analysis/notebook
- https://rpubs.com/lmorgan95/MissForest#:~:text=MissForest%20is%20a%20random%20forest,then%20predicts%20the%20missing%20part.
- https://www.datacamp.com/community/tutorials/understanding-logistic-regression-python
- https://towardsdatascience.com/heres-what-i-ve-learnt-about-sklearn-resample-ab735ae1abc4
   
 
