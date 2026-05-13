# 🧠 Fake News Detection System

> Detecting misinformation using Machine Learning, Deep Learning & Google Fact Check API

![Python](https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-1.57-red?style=for-the-badge&logo=streamlit)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.21-orange?style=for-the-badge&logo=tensorflow)
![Scikit-Learn](https://img.shields.io/badge/ScikitLearn-Latest-green?style=for-the-badge&logo=scikit-learn)
![HuggingFace](https://img.shields.io/badge/🤗%20Hugging%20Face-Spaces-yellow?style=for-the-badge)

---

## 🌐 Live Demo

> 🔗 **[Click here to try the app]([YOUR_HUGGINGFACE_LINK_HERE](https://huggingface.co/spaces/kevalchuhan76/fake-news-detector))
>
> _(If the app shows "Starting...", wait 60 seconds — it wakes up automatically)_

---

## 📌 Project Overview

This project is an end-to-end **Fake News Detection Web Application** built as part of a Machine Learning assignment. It scrapes real-world fact-check data from [PolitiFact](https://www.politifact.com/), trains multiple ML and Deep Learning models, and deploys them in an interactive web app where users can enter any news statement and get an instant verdict.

---

## 🗂️ Dataset

- **Source:** Scraped from [PolitiFact.com](https://www.politifact.com/factchecks/list/)
- **Total Records:** ~2900+ fact-checked statements
- **Features:** `authors`, `dates`, `statements`, `sources`, `targets`
- **Target:** Binary classification — `1 = Real`, `0 = Fake`
- **Class Distribution:** Highly imbalanced → handled with SMOTE

---

## 🔍 Exploratory Data Analysis (EDA)

- ✅ Missing value detection & removal
- ✅ Duplicate detection & removal
- ✅ Class distribution visualization
- ✅ Text length & word count analysis
- ✅ WordCloud for most common words
- ✅ Real vs Fake word comparison
- ✅ Correlation heatmap
- ✅ Outlier detection via boxplot

---

## ⚙️ Data Preprocessing

- Lowercasing & punctuation removal
- Stopword removal using NLTK
- TF-IDF Vectorization (for ML models)
- Keras Tokenizer + Padding (for Deep Learning models)
- SMOTE applied to handle class imbalance

---

## 🤖 Models Trained

| Model | Type | Description |
|-------|------|-------------|
| Best ML Model | Traditional ML | Trained inside sklearn Pipeline with TF-IDF |
| ANN | Deep Learning | Artificial Neural Network using Keras |
| RNN | Deep Learning | Recurrent Neural Network using Keras |

### 🗳️ Final Verdict Logic

A **majority voting system** is used:

- If 2 or more models say **Fake** → ❌ Fake
- If 2 or more models say **Real** → ✅ Real

---

## 🌐 Google Fact Check API

The app queries the **Google Fact Check Tools API** in real-time to cross-verify claims against trusted fact-check sources.

---

## 🖥️ Web Application

Built with **Streamlit** and deployed on **Hugging Face Spaces**.

### Features

- 📰 Enter any news statement
- 🧠 Get predictions from ML, ANN, and RNN models
- 🗳️ Final majority-vote verdict
- 🌐 Cross-check with Google Fact Check API
- 🎨 Dark-themed user interface

---

## 📁 Project Structure

```bash
fake-news-detector/
│
├── app.py
├── requirements.txt
├── Dockerfile
├── best_ml_model.pkl
├── tokenizer.pkl
├── ann_model.h5
├── rnn_model.h5
└── README.md
```

---

## 🚀 How to Run Locally

```bash
git clone https://github.com/YOUR_USERNAME/fake-news-detector.git

cd fake-news-detector

pip install -r requirements.txt

streamlit run app.py
```

---

## 📦 Dependencies

```txt
streamlit
joblib
tensorflow==2.21.0
scikit-learn
requests
numpy
nltk
imbalanced-learn
```

---

## 🧪 Sample Test Cases

| Statement | Expected Result |
|---------|----------------|
| Vaccines contain microchips | ❌ Fake |
| Government launched new education policy | ✅ Real |
| The earth is flat | ❌ Fake |

---

## 👨‍💻 Author

Keval Chouhan
🎓 M.Tech Data Science Student

- GitHub: https://github.com/kevalchuhan/fake-news-detection
- Hugging Face: https://huggingface.co/spaces/kevalchuhan76/fake-news-detector

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 🙏 Acknowledgements

- PolitiFact for fact-check data
- Hugging Face Spaces for hosting
- Google Fact Check Tools API
- Streamlit framework
- Scikit-Learn & TensorFlow
