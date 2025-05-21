
# XAI-Enhanced Early Screening for Neurodevelopmental Disorders (NDDs)

## Overview
This project provides an early screening tool for neurodevelopmental disorders (NDDs) such as Autism Spectrum Disorder (ASD), Attention-Deficit/Hyperactivity Disorder (ADHD), communication disorders, and motor disorders. The tool utilizes **Explainable Artificial Intelligence (XAI)** to enhance transparency, trust, and understanding of the model's predictions. The application is designed to support clinicians and families in making informed decisions based on accurate, interpretable predictions.

### Key Features:
- **AI-Powered Screening**: Machine learning models are trained to predict NDDs based on clinical, neuroimaging, and speech data.
- **Explainable Predictions**: SHAP (Shapley Additive Explanations) and other XAI techniques provide transparent and interpretable explanations for each prediction.
- **Multimodal Data**: Supports integration of clinical data, neuroimaging (e.g., fMRI), and speech data for a more comprehensive analysis.
- **Culturally Adapted Interface**: The user interface is designed to be multilingual and culturally sensitive, ensuring accessibility across diverse populations.

## Project Structure

The folder structure is organized as follows:

```
/XAI-NDD-Screening
│
├── /data/                          # Folder for raw and processed data
│   ├── raw_data/                   # Raw data (clinical, neuroimaging, speech, etc.)
│   ├── processed_data/             # Preprocessed data (ready for modeling)
│   └── data_description.md         # Description of the datasets and data formats
│
├── /models/                         # Folder for model-related code
│   ├── model_training.py            # Script to train models (e.g., RandomForest, CNN, etc.)
│   ├── model_explanation.py         # Script to apply SHAP, LIME, Attention for explanation
│   ├── /saved_models/               # Folder to store trained model files (e.g., .pkl, .h5)
│   └── model_evaluation.py          # Script for model evaluation and performance metrics
│
├── /notebooks/                      # Folder for Jupyter Notebooks (for experimentation)
│   ├── data_exploration.ipynb       # Data exploration and cleaning notebook
│   ├── model_training_notebook.ipynb # Notebook for training models and applying XAI
│   └── model_explanation_notebook.ipynb # Notebook for interpreting models using XAI techniques
│
├── /api/                            # Folder for the API-related code (Flask, Django, etc.)
│   ├── app.py                       # Flask API for serving the model
│   └── requirements.txt             # Dependencies for the API (Flask, scikit-learn, etc.)
│
├── /frontend/                       # Folder for the frontend UI (optional)
│   ├── /assets/                     # Folder for UI assets (images, icons, etc.)
│   ├── index.html                   # Frontend HTML file
│   ├── app.js                       # JavaScript file for interactivity
│   └── style.css                    # CSS file for styling the UI
│
├── /docs/                           # Folder for documentation
│   ├── README.md                    # Main documentation file
│   ├── installation_guide.md         # Instructions for setting up the project
│   └── usage_guide.md               # Instructions for using the XAI application
│
├── .gitignore                       # Git ignore file to exclude unnecessary files (e.g., .pyc, .log)
├── requirements.txt                 # Python dependencies (e.g., Flask, scikit-learn, shap, lime, etc.)
└── setup.py                         # Setup script for the project
```

## Installation

### Prerequisites

- **Python 3.7+**: This project is developed using Python 3.x. You can install Python from [here](https://www.python.org/downloads/).
- **Flask**: For the backend API.
- **Machine Learning Libraries**: scikit-learn, SHAP, LIME, etc.
- **Visualization**: Plotly for SHAP and model visualization.
- **Neuroimaging & Speech Analysis Libraries**: TensorFlow/Keras for deep learning models (if applicable).

### Step 1: Clone the repository
Clone this repository to your local machine:

```bash
git clone https://github.com/your-username/XAI-NDD-Screening.git
cd XAI-NDD-Screening
```

### Step 2: Create a Virtual Environment (Optional but recommended)
To create a virtual environment, run the following command:

```bash
python -m venv venv
```

Activate the virtual environment:
- On Windows: 
  ```bash
  venv\Scriptsctivate
  ```
- On macOS/Linux:
  ```bash
  source venv/bin/activate
  ```

### Step 3: Install dependencies
Install all required dependencies using `requirements.txt`:

```bash
pip install -r requirements.txt
```

### Step 4: Run the Flask API
Navigate to the `api` directory and run the Flask application:

```bash
python app.py
```

The Flask server will start, and you can access the API at `http://127.0.0.1:5000/`.

### Step 5: Access the Frontend
To view the frontend interface, open `index.html` in your browser. This will allow you to input clinical data and see predictions and explanations generated by the model.

## Usage

1. **Submit Clinical Data**: Input clinical data (age, IQ, symptom score) into the provided form.
2. **View Results**: After submission, the backend processes the data and displays the prediction (e.g., ASD, ADHD) along with a SHAP plot showing the influence of each feature on the model's decision.
3. **Interactive Explanation**: The SHAP plot shows which features had the most significant impact on the prediction.

## Future Work

- **Model Improvement**: Incorporating more data sources (e.g., genetic data, more neuroimaging modalities).
- **Multilingual Support**: Expanding the frontend to support multiple languages for broader accessibility.
- **Real-World Testing**: Testing the tool in clinical environments and adjusting based on feedback from users.

## Contributing

Feel free to open issues or contribute pull requests to improve this project. If you have any suggestions, feedback, or bug fixes, we welcome contributions!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
