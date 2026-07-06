# 📩 SMS Spam Detection using Recurrent Neural Network (RNN)

An AI-powered SMS Spam Detection application built using **Python, TensorFlow, Keras, and Streamlit**. The application classifies SMS messages as **Spam** or **Ham (Not Spam)** using a **Many-to-One Recurrent Neural Network (RNN)** trained on the SMS Spam Collection dataset.

---

## 📌 Project Overview

Spam messages are a common problem in digital communication. This project uses a Recurrent Neural Network (RNN) to automatically classify incoming SMS messages into:

- 🚨 Spam
- ✅ Ham (Legitimate Message)

The application includes a simple and interactive **Streamlit web interface** where users can enter any SMS and instantly receive the predicted class along with the model's confidence score.

---

## 🚀 Features

- SMS Spam/Ham classification
- Text preprocessing and cleaning
- Tokenization using Keras Tokenizer
- Sequence padding for fixed-length input
- Recurrent Neural Network (SimpleRNN)
- Binary classification using Sigmoid activation
- Automatic model training (first run only)
- Model and tokenizer saved for future predictions
- Interactive Streamlit web application
- Prediction confidence score
- Model evaluation using:
  - Accuracy
  - Confusion Matrix
  - Classification Report

---

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- Streamlit
- Pandas
- NumPy
- Scikit-learn
- Pickle
- Regular Expressions (re)

---

## 📂 Project Structure

```
SMS-Spam-Detection/
│
├── app.py                 # Main Streamlit application
├── spam.csv               # SMS Spam Collection dataset
├── spam_model.keras       # Trained RNN model (generated after training)
├── tokenizer.pkl          # Saved tokenizer
├── requirements.txt
├── README.md
```

---

## 🧠 Model Architecture

```
Embedding Layer
        ↓
SimpleRNN Layer
        ↓
Dense Layer (ReLU)
        ↓
Output Layer (Sigmoid)
```

### Model Details

- Embedding Dimension: **32**
- RNN Units: **128**
- Hidden Dense Layer: **32 neurons**
- Output Layer: **1 neuron (Sigmoid)**
- Loss Function: **Binary Crossentropy**
- Optimizer: **Adam**
- Batch Size: **32**
- Epochs: **10**

---

## 📊 Dataset

This project uses the **SMS Spam Collection Dataset**.

Each record contains:

- **v1** → Label (`spam` / `ham`)
- **v2** → SMS Message

Example:

| Label | Message |
|--------|---------|
| ham | Hi, are we meeting today? |
| spam | Congratulations! You have won ₹10,000. Claim now! |

---

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/your-username/SMS-Spam-Detection.git

cd SMS-Spam-Detection
```

---

### Create Virtual Environment (Recommended)

```bash
python -m venv .venv
```

Activate

Windows

```bash
.venv\Scripts\activate
```

Linux / macOS

```bash
source .venv/bin/activate
```

---

### Install Dependencies

```bash
pip install -r requirements.txt
```

Or install manually

```bash
pip install tensorflow streamlit pandas numpy scikit-learn
```

---

## ▶️ Run the Application

```bash
streamlit run app.py
```

or

```bash
python -m streamlit run app.py
```

The application will open automatically in your browser.

---

## 📈 Training Process

When the application runs for the first time:

1. Loads the dataset
2. Cleans the text
3. Converts labels into binary values
4. Tokenizes SMS messages
5. Pads sequences
6. Splits data into training and testing sets
7. Trains the RNN model
8. Saves:
   - `spam_model.keras`
   - `tokenizer.pkl`

On future runs, the saved model is loaded directly without retraining.

---

## 📝 Text Preprocessing

The following preprocessing steps are applied:

- Convert text to lowercase
- Remove special characters
- Remove extra spaces
- Tokenize words
- Convert text into sequences
- Pad sequences to a fixed length

---

## 📊 Evaluation Metrics

After training, the model is evaluated using:

- Test Accuracy
- Confusion Matrix
- Classification Report
  - Precision
  - Recall
  - F1-score

---

## 💻 User Interface

The Streamlit application allows users to:

- Enter any SMS message
- Predict whether it is Spam or Ham
- View prediction confidence

Example:

```
Input:

Congratulations! You've won ₹50,000.
Click here to claim.

Prediction:

🚨 Spam

Confidence:

99.43%
```

---

## 📌 Sample Spam Messages

```
Congratulations! You have won ₹50,000 cash.
Click here to claim your prize.
```

```
URGENT!
Your bank account has been suspended.
Verify immediately.
```

```
Win a FREE iPhone today.
Limited offer.
```

---

## 📌 Sample Ham Messages

```
Hi, I'll reach home by 7 PM.
```

```
Can we meet tomorrow morning?
```

```
Happy Birthday! Have a great day.
```

---

## 🔮 Future Enhancements

- LSTM and GRU model comparison
- Bidirectional RNN implementation
- Email spam detection
- Multilingual spam detection
- REST API using FastAPI
- Docker deployment
- Cloud deployment (Streamlit Cloud)

---

## 📚 Learning Outcomes

This project demonstrates:

- Natural Language Processing basics
- Text preprocessing
- Tokenization
- Sequence padding
- Recurrent Neural Networks
- Binary classification
- Model persistence
- Streamlit application development

---

## 👩‍💻 Author

**Siri Reddy Gopu**

B.Tech – Data Science

GitHub: https://github.com/SiriReddy-006

LinkedIn: https://www.linkedin.com/in/siri-reddy-gopu-720557289

---

## ⭐ If you found this project helpful, consider giving it a Star on GitHub.
