# ML Backend Documentation



## ML Models

### 1. Income Prediction
- **Model Type**: Regression
- **Metrics**: 
  - Mean Absolute Error (MAE)
  - R-squared (R²)

### 2. Disruption Detection
- **Model Type**: Classification
- **Algorithm**: Random Forest
- **Description**: A model that identifies potential disruptions based on historical data.

### 3. Fraud Detection
- **Model Type**: Anomaly Detection
- **Algorithms**: Isolation Forest and SIMD
- **Description**: This model detects fraudulent activities by identifying outliers in the data.

### 4. Trust Score
- **Dimensions**: 
  - Historical Claims
  - User Behavioral Analysis
  - External Factors
- **Dynamic Premium Calculation**: This involves adjusting premiums based on fluctuations in the trust score.

## Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/Jayshandhya/ShieldPay-
   ```
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Configure the environment variables as needed.

## API Endpoints

| Method | Path                   | Description                           |
|--------|------------------------|---------------------------------------|
| GET    | /api/income-prediction | Get income prediction results         |
| POST   | /api/disruption-detection | Submit data for disruption detection  |
| POST   | /api/fraud-detection   | Submit claims for fraud detection     |
| GET    | /api/trust-score       | Retrieve trust score for a user      |

## Example Claim Flow in Python
```python
import requests

# Example Claim Submission
url = "https://api.shieldpay.com/api/submit-claim"
data = {
    "claim_id": "12345",
    "amount": 1000,
    "user_id": "user_01"
}
response = requests.post(url, json=data)

print(response.json())
```

## Integration Instructions
To integrate the ML backend with your application:
1. Ensure all API keys and environment variables are set.
2. Use the provided API endpoints to interact with the ML models.

## Model Files Reference
- `income_model.pkl`: Model file for income prediction.
- `disruption_model.pkl`: Model file for disruption detection.
- `fraud_model.pkl`: Model file for fraud detection.
- `trust_score_model.pkl`: Model file for trust scoring.
