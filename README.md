📊 Stock Price Prediction using Machine Learning
This repository contains two complete projects aimed at predicting stock closing prices using historical data and technical indicators. Both projects implement multiple regression models and allow for a comparative understanding of different modeling approaches:

🔍 Objective
The goal is to build reliable and interpretable models that can accurately predict next-day stock closing prices based on real-world historical data.

📁 Project Variants
  🔹 1. API-based Version (using yfinance)
    Data: Live stock data (e.g., AAPL) downloaded via yfinance
    Approach: Online fetching of 5 years of daily data
    Use Case: Best for real-time experimentation and updating with latest data

  🔹 2. Excel-based Version
    Data: Randomized but realistic stock price dataset (2018–2022) from Excel
    Approach: Suitable for offline training, reproducible results, and portability
    Additions: Includes XGBoost, SHAP analysis, and a model comparison heatmap

⚙️ Technologies Used
  Languages: Python
  Libraries: Pandas, NumPy, scikit-learn, Matplotlib, Seaborn, XGBoost, SHAP
  Platform: Jupyter Notebook / Google Colab

🌟 Key Insights

  🔸 Excel-based Version
    ✅ Linear Regression achieved R² = 0.962, RMSE = 13.91
    ✅ XGBoost achieved R² = 0.953, RMSE = 15.17
    📊 SHAP analysis revealed MA_10, RSI_14, and Volume as the most impactful features
    ✅ Feature engineering (e.g., lagged returns, MA, RSI) greatly improved model accuracy

  🔸 API-based Version
    ✅ Linear Regression achieved R² = 0.990, RMSE = 1.92
    📉 Decision Tree and Random Forest performed decently but underfitted the problem
    🔄 Automatically updates data via yfinance for dynamic predictions

📈 Results Comparison
Model	                 R² Score (Excel)	         RMSE (Excel)	     R² Score (API)	     RMSE (API)
Linear Regression	          0.962	                  13.91	            0.990              1.92
Decision Tree	              0.432	                  53.72	            0.865	             7.12
Random Forest	              0.187	                  64.29	            0.851	             7.49
XGBoost	                    0.953	                  15.17	              —	                 —

📂 Folder Structure
Copy
Edit
├── README.md
├── Copy_of_stock_price_prediction_.ipynb  -----excel project
├── stock_price_prediction.ipynb           -----API project
└── stock_price_prediction_dataset.xlsx    -----excel dataset

✅ How to Run
Clone the repository.
Open either notebook in Google Colab or Jupyter Notebook.
Install any required libraries (xgboost, shap) in Colab if needed.
Run cells sequentially.

📌 Notes
📦 All models were evaluated using R² and RMSE.
📉 Lower RMSE and higher R² indicate better performance.
📁 The Excel version is best suited for reproducible academic submissions.

🙌 Contributing
Contributions are welcome!
Whether it’s improving the feature set, optimizing models, or adding more visualizations — feel free to fork this repo and submit a pull request.
Would appreciate collaborations from fellow data science learners, financial analysts, or anyone interested in ML for time series.
