# Project Summary: Used Car Price Prediction (Rusty Bargain)

In this project, we built and evaluated several machine learning models to predict used car prices using a large dataset of listings from **Rusty Bargain**, containing over 350,000 records. The dataset included a mix of numerical and categorical features.

After thorough data cleaning — including handling missing values, removing duplicates, and filtering outliers — we trained and tuned the following models:


| Model                   |  RMSE ($)          | 
|------------------------|---------------------|
| Linear Regression       | 2327.48             |
| Decision Tree (Best)    | 1825.43             | 
| Random Forest (Basic)   | 1499.19             |
| Random Forest (Tuned)   | **1535.27**         | 
| LightGBM (Basic)        | 1614.12             | 
| LightGBM (Tuned)        | 1595.54             | 
| RF(Tuned) on test dataset| **1538.19**     | 



-  **Best Model**: Tuned Random Forest (`n_estimators=80`, `max_depth=20`)  
-  **Final Test RMSE**: **1538.19 USD**

---

## Key Takeaways

- **Ensemble models** like Random Forest and LightGBM significantly outperformed linear and single-tree models.
- **Random Forest** provided the best overall accuracy on the test set.
- **LightGBM**, while slightly behind in RMSE, trained **much faster** and handled categorical data natively — making it a strong option for real-time or production use.
- Careful **validation set separation** helped avoid overfitting and gave a realistic estimate of model performance on unseen data.