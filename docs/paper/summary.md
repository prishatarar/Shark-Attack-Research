# Project Summary: Shark Attack Fatality Prediction

## Problem
Shark attacks are rare but high impact events. Understanding the factors that influence whether an attack becomes fatal can help improve awareness, safety measures, and research in marine environments.

This project aims to predict whether a shark attack is fatal using historical data and machine learning.

### Why The Project Matters
This project demonstrates how machine learning can extract meaningful patterns from noisy real-world data and contribute to understanding rare but critical events.

It also showcases:
- End-to-end ML pipeline design
- Feature engineering from unstructured data
- Model comparison under class imbalance
---

## Approach

## Dataset
- Source: Historical Shark attack dataset
- Contains:
  - Date
  - Year
  - Type
  - Country 
  - Area
  - Location
  - Activity
  - Name
  - Gender
  - Age
  - Injury
  - Fatal (Y/N)
  - Time
  - Species 

---

## Key Features Engineered
Total 31 features across 6 categories 
- Activity categories
  Activity_boarding
  Activity_diving
  Activity_fishing
  Activity_other
  Activity_surfing
  Activity_swimming
- Shark species classification
  Classified Species_Blue Shark
  Classified Species_Bull Shark
  Classified Species_No Shark
  Classified Species_Nurse Shark
  Classified Species_Other Species
  Classified Species_Reef Shark
  Classified Species_Tiger Shark
  Classified Species_White Shark
  Classified Species_Whitetip Shark
- Ocean 
  ocean_Arctic
  ocean_Atlantic
  ocean_Indian
  ocean_No Ocean
  ocean_Pacific
  ocean_Southern
- Sex
  Sex _Female
  Sex _Male
  Sex _Unknown
- Type 
  Type_Boating
  Type_Provoked
  Type_Sea Disaster
  Type_Unknown
  Type_Unprovoked
- Numeric/Binary Features
  Hemisphere
  is_weekend


---

## Models Used
The same set of 31 features was used across the following 6 models
- Logistic Regression
- Decision Tree
- Random Forest
- KNN
- XGBoost
- LightGBM

---

## Evaluation Metrics
I evaluated each model using sklearn.metrics classification_report package to calculate the following:
- Precision
- Recall 
- F1
- Support 
I also computed PR-AUC for each model using sklearn.metrics packages roc_auc_score. 
    
---

## Future Improvements
## Key Results
*(Update these after running your models)*

- Best Model: Logistic Regression
- PR-AUC: 0.489
- F1: 0.48
- Recall: 0.77

### Insights:

Why Logistic Regression wins 
1. The dataset is small + noisy
- Lots of missing data
- Many “Unknown” values
- Weak features
Complex models (trees, boosting) overfit or fail to generalize.

2. Signal is weak and mostly linear
For features like Activity, Species category, Ocean, Season, relationships are either simple or broad patterns.
Logistic Regression handles this better

3. All tree-based models (Random Forest, XGBoost, LightGBM):
Have:
  High precision for non-fatal
  But very low recall for fatal (0.2–0.3)
Meaning:
  They miss most fatal cases

---

## Research Output
This work resulted in a research paper:

📄 shark_attack_prediction_ml_analysis.pdf

---

## Future Work

This project helped me understand how machine learning can be used on real world data, but I also saw some limitations in the dataset.

- It would be helpful to have more environmental details like water temperature, weather, and water clarity, since these might affect shark behavior.
- Doing a modeling of shark migration patterns and blending it in with my existing model 
- Many records have shark species listed as “Unknown” or “Other,” so improving this information could help the model learn better patterns.
- Some non-fatal attacks may not be reported, so the dataset might be biased. Having more complete data would improve the model.
- The dataset does not include details about the victim, like how serious the injury was or how quickly they received medical help, which can affect whether an attack becomes fatal.
- Features like Ocean and Season are very general, so making them more detailed could improve the results.
- I would also like to compare the models more clearly using the same evaluation metrics.

Overall, better and more detailed data would help make the predictions more accurate and meaningful.


---

## Author
High School Student Research Project (AI + Oceanography)
