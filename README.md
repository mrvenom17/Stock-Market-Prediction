# 📈 Stock Trading Alert System (ML + Notifications)

A Python-based automated trading assistant that:
- Collects stock data
- Applies technical indicators
- Trains an LSTM model to forecast price trends
- Performs backtesting to evaluate strategies
- Sends alerts via desktop notifications and Twilio SMS

> ⚠️ This is a **prototype project**. It doesn't place real trades but evaluates strategy and notifies you.

---

## 🚀 Features

- ⏱️ Runs hourly using `schedule`
- 🔔 Alerts on desktop using `plyer`
- 📲 SMS alerts via Twilio
- 📊 LSTM-based prediction model (TensorFlow/Keras)
- 📈 Includes major technical indicators (RSI, EMA, MACD, ADX, etc.)
- 🧾 Backtest logic with tax calculation

---

## 🧠 Requirements

- Python 3.7+
- Install dependencies:

```bash
pip install -r requirements.txt
```

⚙️ Configuration
Edit the following values in the script:
twilio_phone_number = "your_twilio_phone_number"
your_phone_number = "your_phone_number"
client = Client("your_twilio_account_sid", "your_twilio_auth_token")


🧩 Functions
trade_logic()
Main logic that:
Gets chart data
Calculates indicators
Trains an LSTM model
Backtests the result
Sends an alert with profit/tax estimate
send_alert(message)
Sends desktop notifications via plyer.
create_lstm_model()
Returns a compiled LSTM model for prediction with:
input_shape = (None, 10)  # 10 input features expected

📅 Scheduling
The task is run every hour using:
schedule.every().hour.do(trade_logic)
You can adjust the interval to your preference.

🛠️ TODO
 Implement actual get_chart_data, calculate_indicators, train_ml_model, backtest functions
 Add error handling for data-fetching and model prediction
 Save predictions and backtesting results for analysis
 Optionally, integrate with a brokerage API for paper/live trading

