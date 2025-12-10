# EECS4480 – Capstone Project  
## Title: Developing a Neural Network Model to Detect Phishing Emails with Gmail API Integration

This repository contains my EECS4480 capstone project: a BERT-based phishing email detection system that:

- Trains on multiple real-world phishing and ham email datasets  
- Evaluates robustness using adversarial text attacks (TextFooler, BAE)  
- Integrates with the **Gmail API** to classify emails directly from a live inbox  

The project is implemented in **Jupyter Notebooks** using **PyTorch**, **HuggingFace Transformers**, **TextAttack**, and the **Gmail API**.

---

## 📁 Repository Structure
```
EECS4480---Capstone-Project/
├── notebooks/
│   ├── 01_preprocess.ipynb                # Data loading & preprocessing
│   ├── 02_train_bert.ipynb                # BERT training & fine-tuning
│   ├── 03_train_with_TextAttack.ipynb     # Adversarial robustness training
│   ├── 04_analysis.ipynb                  # Evaluation, metrics, confusion matrices
│   ├── 05_eval_synthetic.ipynb            # Synthetic dataset evaluation
│   ├── 06_Gmail_integration.ipynb         # Gmail API integration & inbox predictions
│   └── ...
├── requirements.txt
└── .gitignore
```

---

## 🚀 Features

- **BERT-based classifier** for phishing vs ham  
- Supports multiple real-world datasets  
- Evaluation metrics: Accuracy, Precision, Recall, F1-Score  
- **Adversarial testing & training** (TextAttack)  
- **Gmail API integration** for live inbox predictions  

---

## 🛠️ Getting Started

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/ZackPham21/EECS4480---Capstone-Project.git
cd EECS4480---Capstone-Project
```

---

## 2️⃣ Create & Activate a Virtual Environment (Recommended)

**macOS / Linux:**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

**Windows (PowerShell):**
```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

---

## 3️⃣ Install Dependencies
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

---

## 📓 Running the Notebooks
```bash
jupyter lab
# or
jupyter notebook
```

### Notebook Execution Order (Updated)

1. **01_preprocess.ipynb** – Dataset cleaning & tokenization  
2. **02_train_bert.ipynb** – Fine-tuning BERT  
3. **03_train_with_TextAttack.ipynb** – Adversarial robustness training  
4. **04_analysis.ipynb** – Evaluation, metrics, confusion matrices  
5. **05_eval_synthetic.ipynb** – Evaluate synthetic email dataset  
6. **06_Gmail_integration.ipynb** – Connect Gmail & classify inbox emails  

---

## ✉️ Gmail API Setup

### Step 1 — Enable Gmail API  
- Open Google Cloud Console  
- Create a project  
- APIs & Services → Library  
- Enable **Gmail API**

### Step 2 — Configure OAuth Consent Screen  
- Choose **External**  
- Add test user  

### Step 3 — Create OAuth Client Credentials  
- Credentials → Create Credentials → OAuth Client ID  
- Select **Desktop App**  
- Download JSON → rename to **credentials.json**

### Step 4 — Place credentials inside `/notebooks`  

The notebook will generate `token.json` automatically after first login.

---

## 📄 License
This project is for academic use under EECS4480 Capstone guidelines.
