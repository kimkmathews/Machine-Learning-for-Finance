## NSE Stock Market Movement Prediction

This project is focused on developing a model to predict stock market movements for stocks listed on the National Stock Exchange of India (NSE). This is an initial effort, and further model tuning and exploration are planned.

### Functionality

The current code performs the following actions:

1. **Data Acquisition:** Downloads historical stock price data from Yahoo Finance for a specified stock symbol and date range.
2. **Feature Engineering:** Creates new features based on technical indicators and prior closing prices. Some examples include:
    * Moving Averages (EMA, MA)
    * Percentage Change
    * Volume Changes
3. **Target Variable Definition:** Defines the target variable as an indicator of whether the closing price in 10 days will be 5% higher than the current closing price.
4. **Model Training and Evaluation:**
    * Splits the data into training and testing sets.
    * Trains a Logistic Regression model (with the option to use a Random Forest Classifier).
    * Evaluates the model's performance using metrics like accuracy, precision, recall, F1 score, and ROC AUC score.
    * Generates confusion matrices to visualize model performance.
5. **Prediction on Validation Data:** Makes predictions on a separate validation set of data and stores the results along with the actual closing prices and target values.

**Please note:** This is a starting point, and the current model may not be optimized for accurate predictions.

### Future Work

* Explore and implement additional machine learning models (e.g., XGBoost, Support Vector Machines) for potential performance improvements.
* Conduct hyperparameter tuning to optimize the chosen model(s).
* Integrate feature selection techniques to identify the most relevant features for prediction.
* Backtesting the model on historical data to assess its effectiveness.
* Implement a framework for real-time stock price prediction and trade signal generation.

### How to Use

1. Clone this repository.
2. Ensure you have the required libraries installed (`pandas`, `numpy`, `sklearn`, `yfinance`, `matplotlib`, `seaborn`).
3. In the `logistic_prediction.py` file, edit the `df_stocks.csv` file path to point to your CSV file containing stock symbols (one symbol per line).
4. Run the script using `python logistic_prediction.py`.

The script will generate two CSV files:
  * `model_result.csv`: Contains prediction details (symbol, accuracy, precision, recall, ROC score) for each stock symbol.
  * `model_details.csv`: Stores detailed results for the validation set, including predicted vs. actual closing prices and target values.

I hope this explanation is helpful! Feel free to reach out if you have any questions.

**Disclaimer:** This project is for educational purposes only and does not provide financial advice. Any investment decisions made based on the results of this model should be done at your own risk.
