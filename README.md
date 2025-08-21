# ATS-Analyzer-Project
Intelligent ATS Resume Analyzer 🧠 An interactive Python application that scores resumes using a Bidirectional LSTM model. Features context-aware keyword analysis, model persistence, and a command-line UI.


# AI-Powered ATS Resume Analyzer

This project is an intelligent Applicant Tracking System (ATS) that uses a neural network to analyze resumes. It classifies a resume into one of 25 job categories, provides a compatibility score for a user-chosen role, and offers actionable feedback on missing keywords.

This is an intermediate-level machine learning project that demonstrates the end-to-end process of data preparation, model training, and building an interactive application.

---

## 🚀 Features

* **Neural Network Classifier**: Utilizes a Bidirectional LSTM network built with TensorFlow/Keras to understand the context and content of a resume.
* **Interactive UI**: A command-line interface that allows users to select a job category and input their resume in real-time.
* **Intelligent Keyword Analysis**: Provides context-aware feedback by identifying technical skills and keywords specific to the target job category that are missing from the resume.
* **Model Persistence**: The trained model is automatically saved after the first run, allowing for instant analysis in subsequent uses without retraining.
* **Robust Training**: Implements `EarlyStopping` to prevent model overfitting and ensure the most accurate version of the model is used.

---

## 🛠️ Technology Stack

* **Backend**: Python
* **Machine Learning**: TensorFlow, Keras, Scikit-learn
* **Data Handling**: Pandas, NumPy
* **Text Processing**: NLTK, PyPDF2

---

## 📋 How to Set Up and Run

### 1. Prerequisites

* Python 3.8+
* Git

### 2. Clone the Repository

Clone this repository to your local machine:
```bash
git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
cd your-repository-name
```

### 3. Install Dependencies

Install all the required Python libraries using the `requirements.txt` file:
```bash
pip install -r requirements.txt
```

### 4. Run the Application

The first time you run the script, it will train the neural network model. This may take several minutes. After training, the model will be saved as `ats_classifier_model.keras`, and future runs will be instantaneous.

```bash
python your_script_name.py
```

The application will then prompt you to:
1.  Enter the job category you are interested in.
2.  Enter the filename of your resume PDF (make sure the PDF is in the same folder).

The script will then output a full analysis report.

---

## 🧠 Model Details

The core of this project is a text classification model.

* **Architecture**: Bidirectional LSTM (Long Short-Term Memory)
* **Embeddings**: A learned embedding layer to represent words as dense vectors.
* **Training Data**: The model was trained on the "Resume Dataset" from Kaggle, containing 962 resumes across 25 categories.
* **Output**: The model outputs a probability distribution across the 25 job categories, which is then used to calculate the compatibility score.
