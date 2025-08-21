🧠 AI-Powered ATS Resume Analyzer
<div align="center">

</div>

An intelligent Applicant Tracking System (ATS) that uses a neural network to analyze resumes, score them against job descriptions, and provide actionable feedback on missing keywords.

🚀 Key Features
🧠 Neural Network Classifier: Utilizes a Bidirectional LSTM network to understand the context and content of a resume, going beyond simple keyword matching.

💬 Interactive Analysis: A user-friendly command-line interface within the notebook prompts for a job category and resume file for real-time analysis.

🎯 Intelligent Keyword Feedback: Provides context-aware suggestions by identifying technical skills specific to the target job that are missing from the resume.

💾 Model Persistence: Automatically saves the trained model after the first run, allowing for instant analysis in subsequent uses without retraining.

🛡️ Robust Training: Implements EarlyStopping to prevent model overfitting and ensure the most accurate and generalized version of the model is used.

🛠️ Technology Stack
Category

Technologies

Backend

Python

ML/DL

TensorFlow, Keras, Scikit-learn

Data

Pandas, NumPy

Text/PDF

NLTK, PyPDF2

Dev Env

Jupyter Notebook

📋 How to Set Up and Run
1. Prerequisites
Python 3.8+

Git

Jupyter Notebook or JupyterLab

2. Clone the Repository
Clone this repository to your local machine:

git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name

3. Install Dependencies
Install all the required Python libraries using the requirements.txt file:

pip install -r requirements.txt

4. Prepare the Datasets
This is a critical step. The UpdatedResumeDataSet.csv is zipped to save space. You must unzip it before running the notebook.

Find the UpdatedResumeDataSet.zip file in the project folder.

Unzip it. The folder should now contain UpdatedResumeDataSet.csv.

5. Launch and Run the Notebook
Start Jupyter Notebook from your terminal:

jupyter notebook

Open the ATS NN.ipynb file.

Run the cells of the notebook sequentially. The notebook will handle everything:

It will train the model (this may take several minutes on the first run).

It will save the trained model (ats_classifier_model.keras) and helper files.

Finally, it will prompt you for input to analyze your resume.

📂 Project Structure
.
├── 📄 ATS NN.ipynb
├── 🤖 ats_classifier_model.keras
├── 📊 job_descriptions.csv
├── 📄 README.md
├── 📋 requirements.txt
└── 📦 UpdatedResumeDataSet.zip
