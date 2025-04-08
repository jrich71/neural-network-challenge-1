# 🧠 Student Loan Risk Prediction Using Deep Learning

This project uses a deep neural network to predict student loan credit rankings based on financial and academic indicators. The model is built using TensorFlow/Keras and trained on a dataset of anonymized student loan applications. It includes data preprocessing, model evaluation, and basic deployment for inference.

---

## 📦 Dataset

- **Source**: [student-loans.csv](https://static.bc-edx.com/ai/ail-v-1-0/m18/lms/datasets/student-loans.csv)
- **Target Variable**: `credit_ranking` (binary classification)
- **Features**: Includes variables such as income, debt, and education-related metrics

---

## 📊 Workflow

### 1. Data Preprocessing
- Load and inspect dataset
- Identify feature and target columns
- Split data into train/test sets (using `train_test_split`)
- Normalize feature values using `StandardScaler`

### 2. Model Architecture
A sequential model with:
- Input layer matching number of features
- Two hidden layers with ReLU activation:
  - Layer 1: 32 nodes
  - Layer 2: 16 nodes
- Output layer with 1 node and sigmoid activation (binary classification)

### 3. Model Training
- Loss: `binary_crossentropy`
- Optimizer: `adam`
- Metric: `accuracy`
- Epochs: 50

### 4. Evaluation
- Model tested on unseen data
- Report includes:
  - Final loss and accuracy
  - Classification report (precision, recall, F1-score)

### 5. Model Export/Deployment
- Model saved as a `.keras` file to Google Drive
- Reloaded for inference and tested on new predictions

---

## 📈 Results

- Accuracy: 74.25
- Loss: 56.21
- Sample predictions were rounded to binary labels and matched against the ground truth for evaluation.

---

## 🤖 Future Work: Recommendation System Design

This project concludes with a conceptual design for a recommendation system for student loans. Highlights in response to 3 questions include:

### 🔍 Data Requirements
- Credit score and history
- Income and projected income (e.g., by major)
- Existing debt levels

### 🧩 Filtering Strategy
- **Collaborative filtering** chosen to match students to loan options based on historical data of similar profiles.

### ⚠️ Key Challenges
1. **Privacy**: Handling sensitive financial and educational data securely.
2. **Ethics**: Avoiding biased systems that could reinforce predatory lending behavior.

---

## 🛠 Tech Stack

- Python 3
- Pandas, scikit-learn
- TensorFlow / Keras
- Google Colab for development

---

## 🙋‍♂️ Author

**Joshua E. Richardson, PhD, MS, MLIS, FAMIA**  
*Medical Informatics Researcher*  
📍 San Francisco, CA  
🔗 [LinkedIn](https://www.linkedin.com/in/jrichardson7/)

---

## 📌 License

This project is for educational use only. Please cite the original dataset source when reusing this work.