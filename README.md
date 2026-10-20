# Sales Prediction using Python

CodeAlpha Data Science Internship | Task 4

## Problem
Predict sales from advertising spend on TV, Radio and Newspaper, and find which channel affects sales the most.

## Dataset
`Advertising.csv` has 200 records with TV, Radio, Newspaper and Sales. No missing values or duplicates.

## Approach
1. **Cleaning:** dropped the index column, standardised column names, checked missing values and duplicates.
2. **EDA:** pairplot with regression lines and correlation heatmap.
3. **Models compared:** Linear Regression, Ridge, Polynomial (degree 2) plus Ridge, Random Forest, Gradient Boosting (5-fold cross validation).
4. **Impact analysis:** coefficients per channel and a +10% spend scenario for each channel.

## Results
| Model | Test R2 | MAE | RMSE |
|---|---|---|---|
| Poly(2) + Ridge (best) | 0.987 | 0.53 | 0.64 |
| Gradient Boosting | 0.983 | 0.62 | 0.73 |
| Random Forest | 0.983 | 0.61 | 0.74 |
| Ridge | 0.899 | 1.46 | 1.78 |
| Linear | 0.899 | 1.46 | 1.78 |

## Impact of Advertising
Sales change per +1 unit of ad spend: Radio +0.19, TV +0.046, Newspaper about 0.
A 10% spend increase raises sales by about +0.62 (TV), +0.44 (Radio) and +0.01 (Newspaper).

## Business Insights
- TV and Radio drive sales. Newspaper has almost no effect.
- The polynomial model fits much better than the plain linear model, which suggests TV and Radio work better together than separately.
- Recommendation: move budget from Newspaper to TV and Radio, and track return on spend for each channel.

## How to Run
1. Install the libraries: `pip install pandas numpy scikit-learn matplotlib seaborn`
2. Open `CodeAlpha_SalesPrediction.ipynb` in Jupyter or VS Code and click Run All.
3. Keep `Advertising.csv` in the same folder.

## Tools
Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
