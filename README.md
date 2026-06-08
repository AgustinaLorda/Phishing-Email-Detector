# 🛡️ Phishing Detection System – Email Anomaly Detection

## Collaboration & Contributors

This project was developed in collaboration between:

- **Agustina Lorda** 
  **Focus Area:** Modeling (ML Based) 

- **Adeoluwa Afolabi** 
  **Focus Area:** Development (RSE Inspired) 


Together, we built a robust, real-time email phishing detection system featuring a layered architecture, machine learning models, a user-friendly GUI, and Gmail API integration.


## ✨ Features
- GUI built with Tkinter  
- Email classification (Phishing vs. Non-Phishing)  
- Upload and train on custom CSV datasets  
- Choose model types: Logistic Regression, Random Forest, KNN  
- View confusion matrix for performance  
- Real-time predictions  
- Feature engineering and supervised model integration (Logistic Regression, Random Forest, KNN)  
- Automated email fetching via Gmail API 

## 🧰 Tech Stack

- Python
- Tkinter (GUI)
- scikit-learn
- Pandas
- Matplotlib
- BeautifulSoup
- Gmail API

## 🔑 My Contributions (Machine Learning & Feature Engineering)

This project was extended during my **Email Anomaly Detection Internship**  
(DaMADScientistCorps / Lincoln University) where I focused on the **Machine Learning layer**:

### Feature Engineering
- Extracted quantitative and technical features from emails:
  - Link counts, suspicious keyword frequency, body length  
  - Sender domain verification, unknown domain flags  
- Combined manual features with TF-IDF vectors (top 300 features)

### Model Development & Evaluation
- Trained multiple supervised models: Logistic Regression, Random Forest, KNN  
- Evaluated models using:
  - Accuracy, Precision, Recall, F1-score, ROC curves  
  - Confusion matrices for performance visualization  
- Determined supervised models significantly outperformed unsupervised approaches

### Integration & Deployment
- Serialized trained models and vectorizers (`.pk` files)  
- Integrated models into the existing GUI pipeline for real-time prediction  
- Automated Gmail email fetching with OAuth authentication  
- Enabled end-to-end email anomaly detection: fetch → feature extraction → prediction → output CSV

## 🛠 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/AgustinaLorda/Email_Anomaly_Detection.git
   cd phising_detector_app
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   venv\Scripts\activate   # Windows
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Add your Gmail API credentials:
   - Download `credentials.json` from Google Cloud Console.
   - Place it in the root directory (this file should not be pushed to GitHub).

## ▶️ Usage

1. Run the app:
   ```bash
   python phishing_detector_gui.py
   ```

2. Click **Run Full Pipeline** to fetch emails, train a model, and predict.

3. Or click **Run Prediction Only** to use existing trained models.

## 🔐 Gmail Authentication

When you click to fetch emails, a browser will open asking you to log into your Gmail account and authorize access. This uses Google OAuth2 and stores your token securely in `token.json` (excluded from Git).



