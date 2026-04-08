# Customer Segmentation using Machine Learning

## Overview

This project performs customer segmentation using machine learning to group customers based on their behavior and attributes. These segments help businesses with targeted marketing, personalization, and strategic decision-making.

The project consists of:

* **Model Training** using a Jupyter Notebook (`Code.ipynb`)
* **Deployment** using a Streamlit app (`segmentation.py`)

---

## Project Structure

```
data/                 # Dataset used for training
models/               # Stores trained model (.pkl) files (NOT tracked in Git)
Code.ipynb            # Model training and preprocessing
segmentation.py       # Streamlit deployment script
README.md             # Documentation
.gitignore            # Ignored files
requirements.txt      # Dependencies
```

---

## Important Note on Model Files

* The `.pkl` model files are **NOT included in this repository**
* This is intentional to avoid uploading large binary files
* You must generate the model locally before running the app

### Steps to generate the model:

1. Open the notebook:

   ```bash
   jupyter notebook Code.ipynb
   ```
2. Run all cells
3. The trained model will be saved inside the `models/` folder as a `.pkl` file

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

---

## Running the Project

### Step 1: Train the Model

```bash
jupyter notebook Code.ipynb
```

* Run all cells
* Ensure `.pkl` file is created inside `models/`

---

### Step 2: Run Streamlit App

```bash
streamlit run segmentation.py
```

* The app will open automatically in your browser
* If not, go to: http://localhost:8501

---

## How It Works

1. Data preprocessing is done in the notebook
2. A clustering algorithm (typically K-Means) is trained
3. The trained model is saved as a `.pkl` file
4. The Streamlit app loads this model
5. User inputs are taken through UI
6. The model predicts the customer segment

---

## Example Model Loading (in segmentation.py)

```python
import pickle
model = pickle.load(open("models/model.pkl", "rb"))
```

---

## Dependencies

Main libraries used:

* pandas
* numpy
* scikit-learn
* streamlit
* pickle

---

## Key Features

* End-to-end ML pipeline (data → model → deployment)
* Interactive Streamlit UI
* Clean modular structure
* Easy reproducibility (via notebook)

---

## Future Improvements

* Model versioning
* Deploy on Streamlit Cloud
* Add visualization dashboards
* Improve UI/UX
* Use advanced clustering (DBSCAN, Hierarchical)

---

## Author

Hritajit Pal

---

## License

This project is for educational purposes only.
