# Standardization & Outlier Effect

This repository demonstrates how different feature scaling techniques behave in the presence of outliers. It includes examples showing why standardization is important in machine learning preprocessing and how outliers can distort scaling.

---

## 📁 Project Structure

```
standarization/
├── Outlier_Affect.ipynb      # Notebook showing scaling effects
├── data/                     # (optional) datasets
├── README.md                 # Documentation
└── requirements.txt          # Dependencies (optional)
```

---

## 🧠 Key Concepts

### ✔ Why Scaling Matters
Many ML algorithms assume features are on similar scales. Without scaling:
- Gradient descent converges slower
- Distance-based models (KNN, SVM, clustering) behave poorly
- Features with large values dominate smaller ones

### ✔ Effect of Outliers
Outliers can distort scaling depending on the scaler:

| Scaler           | Outlier Sensitivity | Notes |
|-----------------|---------------------|-------|
| **StandardScaler** | High              | Uses mean & std — outliers stretch distribution |
| **MinMaxScaler**   | High              | Compresses normal values into a tiny range |
| **RobustScaler**   | Low               | Uses median & IQR — reduces outlier influence |
| **MaxAbsScaler**   | Medium            | Scales by absolute max — extreme values dominate |

> **Important:** RobustScaler does not remove outliers — it only reduces their influence.

---

## 📊 Notebook Highlights (Outlier_Affect.ipynb)

The notebook:
- Loads sample data
- Introduces artificial outliers
- Applies multiple scalers
- Visualizes results with scatter & box plots

---

## 🚀 How to Run

### 1. Clone the repo

```bash
git clone https://github.com/Karan20704/standarization.git
cd standarization
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

If no requirements file, install manually:

```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter
```

### 3. Run the notebook

```bash
jupyter notebook
```

Open:

```
Outlier_Affect.ipynb
```

---

## 📝 Use Cases

Useful for:
- ML beginners
- Data preprocessing tutorials
- Teaching scaling concepts
- Demonstrating outlier effects

---

## 📜 License

MIT License (or add your preferred license)

---

## 👨‍💻 Author

**Karan More**

Feel free to fork or contribute!
