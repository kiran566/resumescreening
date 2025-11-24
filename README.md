Resume Screening ML App
Overview
This project is an AI-powered Resume Screening Application that automatically classifies resumes into predefined job categories. The system uses a machine learning model trained on resume data and provides an interactive Streamlit web interface for uploading resumes in PDF, DOCX, or TXT format.
The app performs the following steps:


Extracts text from uploaded resumes.


Cleans and preprocesses the text.


Converts the text into TF-IDF features.


Uses a trained ML classifier to predict the candidate’s job category.



Features


Upload resumes in PDF, DOCX, or TXT format.


Automatic text extraction from resumes.


Preprocessing & cleaning of text for ML compatibility.


Machine learning prediction using a pre-trained classifier.


Interactive Streamlit interface for real-time predictions.


Model files stored externally (e.g., Google Drive) to handle large sizes.



Technologies Used


Python 3.x


Machine Learning: scikit-learn (SVC Classifier, TF-IDF)


Text Processing: re, PyPDF2, python-docx


Web Interface: Streamlit


File Management: gdown (for downloading model files)



Installation


Clone the repository:


git clone https://github.com/kiran566/resumescreening.git
cd resumescreening



Create a virtual environment (optional but recommended):


python -m venv venv



Activate the virtual environment:




Windows: venv\Scripts\activate


Mac/Linux: source venv/bin/activate




Install required dependencies:


pip install -r requirements.txt



Ensure the model/ folder exists. The app will automatically download clf.pkl from Google Drive if it’s missing.



Usage


Run the Streamlit app:


streamlit run app.py



Open the URL provided by Streamlit in your browser.


Upload a resume in PDF, DOCX, or TXT format.


The app will display:


Extracted text (optional).


Predicted job category.





Folder Structure
resumescreening/
│
├── app.py                  # Main Streamlit application
├── requirements.txt        # Python dependencies
├── model/                  # Folder for ML model & encoders
│   ├── clf.pkl             # Pre-trained classifier
│   ├── tfidf.pkl           # TF-IDF vectorizer
│   └── encoder.pkl         # Label encoder
├── README.md               # Project documentation


How It Works


Resume file is uploaded → text is extracted using PyPDF2 or python-docx.


Text is cleaned using regex to remove URLs, special characters, and non-ASCII symbols.


TF-IDF vectorizer converts text into numerical features.


ML classifier predicts job category.


Label encoder maps the prediction back to the human-readable category.



Deployment


The app can be deployed on Streamlit Cloud.


Once deployed, it can be accessed from any browser using the public link.


Example link: Resume Screening App



License
This project is open-source and free to use under the MIT License.

If you want, I can also make a shorter “LinkedIn-friendly README” version that’s more like a project summary rather than a technical manual — perfect for your profile.
Do you want me to do that?
