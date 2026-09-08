# Car Price Prediction

This project predicts the selling price of a used car using a machine learning model built in Python. The application uses a Flask web interface where users enter vehicle details and receive an estimated car price.

## Features

- Predicts used car price based on input such as:
  - year
  - kilometers driven
  - fuel type
  - seller type
  - transmission type
  - ownership history
- Uses a trained model saved in the models directory
- Runs through a simple web form in the browser

## Project Structure

- `app.py` - Flask app that loads the trained model and handles predictions
- `dataset/` - contains the car dataset used for model training
- `models/` - trained machine learning model files
- `notebooks/` - Jupyter notebooks for analysis and experimentation
- `Templates/index.html` - frontend page for user input and result display
- `requirements.txt` - Python dependencies for the project

## Tech Stack

- Python
- Flask
- pandas
- NumPy
- scikit-learn
- joblib
- Jupyter Notebook

## Setup Instructions

1. Open the project folder in your terminal.
2. Create a virtual environment:

   ```bash
   python -m venv venv
   ```

3. Activate the virtual environment:

   On Windows:

   ```bash
   venv\Scripts\activate
   ```

   On macOS/Linux:

   ```bash
   source venv/bin/activate
   ```

4. Install the required packages:

   ```bash
   pip install -r requirements.txt
   ```

## Run the Application

Start the Flask server:

```bash
python app.py
```

Then open the browser and visit:

```text
http://127.0.0.1:5000/
```

## How It Works

- The app loads a pre-trained model from the `models` folder.
- The user enters details on the home page.
- The form values are converted into the same feature structure the model expects.
- The app runs the prediction and shows the estimated price on the page.

## Notes

- The model expects the same columns used during training.
- The project includes preprocessing logic to align input data with the trained model format before prediction.
- If you retrain the model, make sure the saved model and feature order still match the app input logic.

## License

This project is for learning and demonstration purposes.
