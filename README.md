# Customer-Churn-Prediction-API
# Create a README file for the portfolio
with open('README.md', 'w') as f:
    f.write('''
# Customer Churn Prediction API

This project demonstrates a machine learning model deployed as a RESTful API to predict customer churn. The model predicts whether a customer is likely to churn based on their age, total purchase amount, years as a customer, and the number of sites visited.

## Features
- **Machine Learning Model**: Trained using scikit-learn.
- **RESTful API**: Built with Flask.
- **Dockerized Deployment**: Ready for containerized deployment.

## Files
- `app.py`: Flask application for the API.
- `Dockerfile`: Configuration for Docker containerization.
- `requirements.txt`: Python dependencies.
- `churn_prediction_model.pkl`: Trained machine learning model.
- `deployment_instructions.txt`: Steps for deploying the API.

## How to Use
### Local Testing
1. Install Python 3.9 and dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Run the Flask app:
   ```bash
   python app.py
   ```
3. Send POST requests to the `/predict` endpoint:
   ```bash
   curl -X POST http://127.0.0.1:5000/predict -H "Content-Type: application/json" -d '{"Age": 40, "Total_Purchase": 10000, "Years": 5, "Num_Sites": 10}'
   ```

### Docker Deployment
1. Build the Docker image:
   ```bash
   docker build -t churn-prediction-api .
   ```
2. Run the container:
   ```bash
   docker run -p 5000:5000 churn-prediction-api
   ```

### Cloud Deployment
Follow the steps in `deployment_instructions.txt` for deploying to platforms like Heroku, AWS, or Google Cloud.

## Example Prediction
Input:
```json
{
    "Age": 40,
    "Total_Purchase": 10000,
    "Years": 5,
    "Num_Sites": 10
}
```
Output:
```json
{
    "status": "success",
    "prediction": 0,
    "probability": {
        "no_churn": 0.96,
        "churn": 0.04
    }
}
```

## Portfolio Showcase
This project is ideal for showcasing skills in:
- Data Science and Machine Learning
- API Development
- Docker and Cloud Deployment

## License
This project is licensed under the MIT License.
''')

print("README.md created for portfolio.")
