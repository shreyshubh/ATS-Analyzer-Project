# ATS-Analyzer-Project
Intelligent ATS Resume Analyzer 🧠 An interactive Python application that scores resumes using a Bidirectional LSTM model. Features context-aware keyword analysis, model persistence, and a command-line UI.


## 🧠 AI-Powered ATS Resume Analyzer
This project is an intelligent Applicant Tracking System (ATS) that uses a neural network to analyze resumes. It classifies a resume into one of 25 job categories, provides a compatibility score for a user-chosen role, and offers actionable feedback on missing keywords.

The entire workflow, from data loading and model training to final analysis, is contained within the ATS NN.ipynb Jupyter Notebook.

## 🚀 Features
Neural Network Classifier: Utilizes a Bidirectional LSTM network built with TensorFlow/Keras to understand the context and content of a resume.

Interactive Analysis: The notebook prompts the user to select a job category and provide their resume for real-time analysis.

Intelligent Keyword Analysis: Provides context-aware feedback by identifying technical skills and keywords specific to the target job category that are missing from the resume.

Model Persistence: The trained model is automatically saved after the first run, allowing for instant analysis in subsequent uses without retraining.

Robust Training: Implements EarlyStopping to prevent model overfitting and ensure the most accurate version of the model is used.

## 🛠️ Technology Stack
Backend: Python

Machine Learning: TensorFlow, Keras, Scikit-learn

Data Handling: Pandas, NumPy

Development Environment: Jupyter Notebook

## 📋 How to Set Up and Run
# 1. Prerequisites
Python 3.8+

Git

Jupyter Notebook or JupyterLab

# 2. Clone the Repository
Clone this repository to your local machine:

git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name

# 3. Install Dependencies
Install all the required Python libraries using the requirements.txt file:

pip install -r requirements.txt

# 4. Prepare the Datasets
This is a critical step. The UpdatedResumeDataSet.csv is zipped to save space. You must unzip it before running the notebook.

Find the UpdatedResumeDataSet.zip file in the project folder.

Unzip it. The folder should now contain UpdatedResumeDataSet.csv.

# 5. Launch and Run the Notebook
Start Jupyter Notebook from your terminal:

jupyter notebook

Open the ATS NN.ipynb file.

Run the cells of the notebook sequentially. The notebook will handle everything:

It will train the model (this may take several minutes on the first run).

It will save the trained model and helper files.

Finally, it will prompt you for input to analyze your resume.

### 📂 Project Structure
.
├── ATS NN.ipynb                    # The main Jupyter Notebook with all the code
├── ats_classifier_model.keras      # The saved, pre-trained model (output of the notebook)
├── job_descriptions.csv            # Dataset containing resumes and categories
├── README.md                       # This file
├── requirements.txt                # Required Python libraries
└── UpdatedResumeDataSet.zip        # The zipped job description dataset (MUST BE UNZIPPED)
epresent words as dense vectors.
* **Training Data**: The model was trained on the "Resume Dataset" from Kaggle, containing 962 resumes across 25 categories.
* **Output**: The model outputs a probability distribution across the 25 job categories, which is then used to calculate the compatibility score.
