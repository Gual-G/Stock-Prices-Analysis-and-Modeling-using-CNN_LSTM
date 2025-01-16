# Stock-Prices-Analysis-and-Modeling-using-CNN_LSTM
### Summary for README: Stock Analysis and Prediction Using CNN-LSTM Models

This project analyzes stock data from four major tech companies (Apple, Google, Microsoft, Amazon) and predicts the closing price of Amazon stock using a hybrid CNN-LSTM model. Below is an overview of the workflow and key components:

---

### **Workflow Overview**
#### 1. **Data Collection**
   - Stock data for Apple, Google, Microsoft, and Amazon was downloaded using Yahoo Finance API (`yfinance` library).
   - Data includes fields such as Open, High, Low, Close, Adjusted Close, and Volume.

#### 2. **Exploratory Data Analysis**
   - **Closing Price Trends**: Visualized historical adjusted closing prices for the four stocks.
   - **Moving Averages**: Computed and plotted 10-day, 20-day, and 50-day moving averages to observe trends.
   - **Correlation Analysis**: Used pairplots and heatmaps to explore relationships between stock returns.

#### 3. **Model Implementation**
   - A hybrid **CNN-LSTM model** was implemented for time-series forecasting.
   - Model architecture:
     - **Conv1D layers**: Extract local patterns from the stock time series.
     - **Bidirectional LSTMs**: Capture sequential dependencies and trends.
     - **Dense layers**: Final layers for regression output.
   - The model was trained with scaled and reshaped data for better convergence.

#### 4. **Model Evaluation**
   - Predictions for Amazon stock were compared to actual values.
   - **Performance Metrics**:
     - Root Mean Square Error (RMSE): ~2.98
     - Confusion Matrix: Provided insights into classification-based performance.
     - Accuracy: 51%, Precision: ~59.4%, Recall: ~63.3%, F1 Score: ~61.3%.

#### 5. **Visualizations**
   - Graphical representation of:
     - Training vs. validation data.
     - Predicted vs. actual stock prices.
     - Confusion matrix (heatmap) to illustrate classification performance.

#### 6. **Key Insights**
   - The model captures upward trends (positive class) more effectively, reflected in the relatively high recall.
   - However, its overall accuracy and ability to distinguish between decreasing and increasing prices remain limited, requiring further refinement.

#### 7. **Future Enhancements**
   - Explore hyperparameter tuning for improved performance.
   - Consider alternative models like Transformers or GRU for comparison.
   - Use additional data features (e.g., news sentiment, macroeconomic indicators) to enhance prediction accuracy.

---

### **Technologies and Libraries**
- Python (Pandas, NumPy, Matplotlib, Seaborn)
- TensorFlow/Keras (CNN, LSTM implementation)
- Yahoo Finance API (`yfinance`) for data acquisition
- Scikit-learn for evaluation metrics and preprocessing

---

This project demonstrates an end-to-end approach for stock analysis and time-series prediction, with opportunities for further optimization and real-world application.
