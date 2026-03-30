# Shark Attack Prediction Project

## Overview
This project analyzes historical shark attack data and builds machine learning models to predict whether an attack is fatal.

The goal is to:
- Clean and preprocess real world messy data
- Engineer meaningful features (activity, species, time, season, etc.)
- Generate plots to analyze date patterns 
- Train multiple ML models
- Evaluate model performance and compare results

---

## Research Paper (published in Curieux Journal, December 2025 issue)

📄 [Read full paper published in Curieux Journal publication, December 2025 issue (pages 405-424)](https://www.curieuxreview.com/_files/ugd/60ed3c_4b51248138e7475eaacb1362e158908c.pdf)


📄 [Paper publication copy uploaded to git](docs/paper/Research_Paper_Shark_Attacks_PrishaTarar.pdf)

### Summary
- Developed ML models to predict shark attack fatality
- Engineered domain specific features (activity, species, time, season)
- Compared multiple classifiers with PR-AUC evaluation

---

## Project Structure
```
project/
├── data/
│   └── raw/attacks_cleaned.csv
├── notebooks/
│   ├── EDA.ipynb
│   └── Model.ipynb
├── docs/
│   └── paper/
│       └── shark_attack_prediction_ml_analysis.pdf
├── requirements.txt
└── README.md
```

---

## Dataset
- Source: Shark attack dataset
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
High School ML Research Project
