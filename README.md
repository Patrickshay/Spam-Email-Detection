# Spam-Email-Detection
This is spam email detection project using raw email Files

Here is a **README.md** file based on project:  

Overview
This project focuses on detecting spam emails using machine learning models.  
It preprocesses raw email data from the "Combined_Spam_Ham.zip"  file and extracts key features for classification.  
We use Word2Vec, Random Forest, SVM, and Logistic Regression to classify emails as spam or ham.

Setup & Requirements

Environment Setup
This project is designed to run in Google Colab.  
Before running the notebook, install the required libraries:

python
!pip install scikit-learn pandas matplotlib

Dataset Preparation
1. Upload the dataset "Combined_Spam_Ham.zip" to your working directory.
2. Extract the files inside "Combined_Spam_Ham".
3. Verify that the extracted emails contain raw email data.

Data Preprocessing
Step 1: Extract Features
The following key features are extracted from each email:
- File Name
- Sender
- Receiver
- Email Subject
- Body of the Email

Step 2: Data Cleaning
- Removed HTML tags, special characters, numbers, and URLs.
- Used stopwords to remove unnecessary words.
- The cleaned emails were saved in Preprocessed_emails.csv.

Step 3: Handling Imbalance
- Applied bootstrapping to increase the dataset size from 6,000 to 15,000 emails.
- Generated email_features.csv containing processed email data.

Spam Classification
Assigning Spam Labels
- Emails were labeled as:
  - 1 → Spam
  - 0 → Ham
- Labels were assigned based on **spam keywords** and manual review.

Feature Representation with Word2Vec
- Converts words into vectorized embeddings.
- Captures semantic meaning of words for better spam detection.

Model Training & Evaluation

**Models Used:**
- **Support Vector Machine (SVM)**
- **Logistic Regression**
- **Random Forest Classifier**

**Metrics for Evaluation**
- **Accuracy**
- **Precision**
- **Recall**
- **F1 Score**

The **best performing model** was selected based on these metrics.

Results & Visualization
- We visualized the **model accuracy, precision, recall, and F1 score**.
- The final spam classification **UI** was created for easy testing.

Common Issues & Fixes
**File Encoding Issues**
- **Problem**: Some emails caused encoding errors.
- **Fix**: Used errors='ignore while reading files.

**Data Parsing Challenges**
- **Problem**: Some emails had missing headers (e.g., From, To, Subject).
- **Fix**: Used **regex** to extract available information.

**Class Imbalance**
- **Problem**: More ham than spam emails caused bias.
- **Fix**: Used **stratified sampling** to balance the dataset.

Future Improvements
- Implement **deep learning models** for better accuracy.
- Improve **handling of obfuscated spam messages**.
- Develop a **browser extension** to flag spam emails in real-time.

Authors
- **Pratikshay Awadhoot**  
- **Avanti Nipunge**  
- **Myna Nereti**  

🔗 **Project Repository:** [GitHub](https://github.com/Patrickshay/Spam-Email-Detection)  

Files in This Repository
| File Name                  | Description |
|----------------------------|------------|
| `Combined_Spam_Ham.zip`   | Raw email dataset |
| `email_features.csv`      | Processed email features |
| `Preprocessed_emails.csv` | Cleaned email content |
| `Spam_Email_Detection.pptx` | Project presentation |
| `Spam_Email_Detection.pdf`  | Detailed report |
| `Project Report_Spam Email Detection.docx` | Project documentation |

How to Run the Project

1 Upload **Combined_Spam_Ham.zip** to your Google Colab directory.  
2️ Run the **Python notebook** (project_final1.ipynb).  
3️ Train and evaluate the models.  
4️ Test the **spam detection UI** using sample emails.  

**Final Thoughts**
This project successfully detects **spam emails** using **machine learning techniques**.  
Our approach leverages **feature extraction, Word2Vec, and classification models** to achieve high accuracy.  

Want to improve this project? Feel free to contribute! 

Let me know if you want any modifications! 😊
