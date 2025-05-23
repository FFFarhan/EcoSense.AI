# EcoSenseAI

## Overview

EcoSenseAI is an application that provides real-time air quality information and AI-powered insights. It displays air quality index (AQI) data, pollutant levels, and weather conditions to help users understand the current air quality and take necessary precautions.

## Features

- **Real-time AQI Monitoring:** Displays the current AQI value and category (Good, Moderate, Unhealthy).
- **Pollutant Levels:** Shows the levels of various air pollutants, such as PM2.5, PM10, NO2, SO2, CO, and O3.
- **AI Insights & Recommendations:** Provides AI-generated insights and recommendations for safety measures and mitigation strategies.
- **Weather Information:** Displays current weather conditions, including temperature, humidity, and precipitation.
- **Interactive Graphs:** Renders interactive graphs of AQI data over time, including observed and predicted values.

## Screenshot
![EcoSense](https://github.com/user-attachments/assets/8575b793-94c6-4ebf-bc20-8bb5aef36e2c)


## Technologies Used

- **Streamlit:** A Python library for creating interactive web applications.
- **Pandas:** A data analysis and manipulation library.
- **Scikit-learn:** A machine learning library.
- **XGBoost, Catboost:** Gradient boosting libraries
- **Altair:** A declarative visualization library.
- **Groq API:** For generating AI insights and recommendations.

## Installation

1.  Clone the repository:

    ```bash
    git clone https://github.com/Himank-Khatri/IGP-EcoSenseAI
    ```
2.  Navigate to the project directory:

    ```bash
    cd EcoSenseAI
    ```
3.  Install the dependencies:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

1.  Run the Streamlit application:

    ```bash
    streamlit run app.py
    ```
2.  Open the application in your web browser at the address displayed in the terminal (usually `http://localhost:8501`).


## Data Sources

The application uses data from the following sources:

-   `artifacts/test.csv`: AQI data.
-   `artifacts/test_pollutants.csv`: Pollutant levels data.
-   Weather API (integrated in `weather.py`): Current weather conditions.

## Model Training

The machine learning models used for AQI prediction are trained using the notebooks in the `notebook/` directory. The training process involves:

1.  Data exploration and analysis.
2.  Data preprocessing and feature engineering.
3.  Model selection and training.
4.  Model evaluation and hyperparameter tuning.
5.  Saving the trained models to the `artifacts/` directory.

# Running the ChatBot Locally

## Prerequisites
- Install **Ollama**: [https://ollama.ai](https://ollama.ai)
- Ensure your system meets the requirements for running Llama-based models.

## Steps to Run a Custom Model

### 1. Verify the Existing `Modelfile`
Ensure you already have a `modelfile1` .
Add the modelfile and the .gguf model to the same folder
Model Download - https://mega.nz/folder/cJBymZQD#LP244FLEQW5W8icQPIiwNA

### 2. Build the Model
Run the following command in the terminal:

```sh
ollama create my-custom-model -f modelfile1
```

This will create a model named `my-custom-model`.

### 3. Manage Models
- List installed models:

  ```sh
  ollama list
  ```

- If the model fails to load, check logs or rebuild it.

### 4. Run the ChatBot
Once the model is loaded, go to the chatbot, and viola, the chatbot will run locally on your own machine!


## AI Insights

The application uses the Groq API to generate AI insights and recommendations based on the current AQI, pollutant levels, and weather conditions. To use this feature, you need to set up a Groq API key.

## License

[License]
